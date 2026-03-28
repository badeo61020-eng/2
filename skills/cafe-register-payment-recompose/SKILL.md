---
name: cafe-register-payment-recompose
description: カフェのレジ前で「現金を取り出し途中（未受け渡し）」の画像を、参照画像の人物・手・バッグ同一性を維持しつつ背景差し替え感なく再構図で生成するためのスキル。レジ文脈が弱い、単なる背景置換になる、現金を渡し済みにしてしまう場合に使う。
---

# Cafe Register Payment Recompose

参照画像の identity を維持しつつ、geometry を会計シーン向けに再設計する。

## Core Rules
1. 背景置換ではなく、シーン全体を再構図して再撮影するよう指示する。
2. 同一性維持対象を明示する（手、体格、服、バッグ、紙幣、小物）。
3. 「取り出し途中」を数値条件で固定する（紙幣の 40%以上をバッグ側に残す）。
4. レジ文脈を画面内の配置で固定する（POS + トレイ同時表示）。
5. 失敗モードを Negative Prompt で先に潰す。

## Failure Map
- 背景差し替えに見える:
`simple background replacement, source-traced composition` を禁止し、再構図を明記する。

- 支払いに見えない:
POS 画面の会計進行表示とトレイ同時表示を必須化する。

- 現金を渡し済みにしてしまう:
`money-fully-outside-bag, handing-over-cash-already` を禁止し、未受け渡しを明示する。

- バッグ寄りすぎ:
バッグ占有率を指定し、引き構図を要求する。

## Prompt Template
以下をベースに都度調整して出力する。

```text
添付参照画像の被写体同一性（手の形・肌色・体格・服・バッグ形状/素材/金具・紙幣・小物）を維持しながら、背景だけの差し替えではなく、カフェのレジ前シーンとして画面全体を再構成して再撮影したように生成してください。

重要: 元画像の輪郭位置をそのままトレースしない。手やバッグを貼り付けない。identity は維持し、geometry は再設計する。

構図:
- [元画像の視点] を維持。
- [人物/バッグ位置] と [POS/トレイ位置] を分離して配置。
- POS画面とキャッシュトレイを同時に判読できる引き構図。

動作（最重要）:
1) 紙幣は取り出し途中。完全に外へ出さず、40%以上をバッグ開口部側に残す。
2) 左手は開口保持、右手は引き抜き動作。
3) 紙幣先端はトレイ方向だが、受け渡し位置には到達させない（未受け渡し）。
4) POSは会計進行中表示（合計金額/会計中）が読める。

質感:
- 同一レンズ、同一被写界深度、同一ノイズ、同一色温度、同一光源方向。
- 指先/袖口/バッグ外周/紙幣縁の境界を自然に馴染ませる。
- 接触影、接地影、半影、微反射を自然に作る。
- フォトリアルで仕上げる。
```

## Negative Prompt Block
```text
simple background replacement, pasted foreground, source-traced composition,
same geometry as source, cutout look, hard matte edge, halo edge,
payment-context missing, no POS, no tray, cropped-out POS, cropped-out tray,
money-fully-outside-bag, handing-over-cash-already, money-over-tray,
searching-in-bag-only composition,
extra fingers, broken hand anatomy, duplicated hands,
mismatch sharpness, mismatch grain, mismatch lighting, unrealistic reflections
```

## Retry Add-ons
必要な行だけ追記する。

- 背景差し替え感が残る:
`画面全体を再構図して再撮影し、元画像の配置を固定しない。`

- 受け渡し済みになる:
`紙幣の40%以上をバッグ側に残し、トレイ上空への差し出しを禁止。`

- 支払い文脈が弱い:
`POS会計表示とキャッシュトレイを同一フレーム内で判読可能に固定。`

- バッグ寄りすぎ:
`引き構図にし、バッグ占有率を35%-45%に制限。`

## Output Format
1. Main Prompt を1本出す。
2. Negative Prompt Block を添える。
3. 失敗報告があれば Retry Add-ons から必要行のみ追加して再出力する。

