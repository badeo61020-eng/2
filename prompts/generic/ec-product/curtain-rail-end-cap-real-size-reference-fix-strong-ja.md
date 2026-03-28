# 実サイズ参照で両端エンドキャップを明確に縮小する強化プロンプト

## 用途
参照画像に写っている実物エンドキャップのサイズ感を基準にして、生成画像内の左右エンドキャップが明らかに大きすぎる場合に、形状は変えずサイズだけをはっきり小さく補正したいときの Nano Banana Pro 用プロンプトです。

## メインプロンプト
```text
図1はエンドキャップ実物のサイズ参照画像、図2は補正対象画像です。図1の実物サイズ感を参考にして、図2の左右両端に付いているエンドキャップを、現在よりはっきり小さくしてください。軽い微調整ではなく、エンドキャップの過大感が消えるまで明確に縮小してください。仕上がりを見たときに、補正前より小さくなったことが明確に分かる状態にしてください。

重要なのはサイズ補正のみです。エンドキャップの形状、輪郭、厚み、先端の造形、金具の構成、デザインは変更しないでください。別形状に作り直したり、左右反転した別パーツに置き換えたりせず、現在写っているエンドキャップそのものを同じ形のまま縮小してください。

縮小の基準は、エンドキャップがカーテンレール端部の太さと自然に釣り合って見えること、端部パーツだけが悪目立ちしないこと、レール端から大きく張り出して見えないことです。図3のミリ表記は厳密な数値変換ではなく、実物はもっと小さい部材であるというサイズ感の基準として使ってください。図2のエンドキャップが現在の見え方より一段小さく見えるまで補正してください。

エンドキャップはレール端の開口に正しく差し込まれている見え方を維持し、先端に貼り付いたような見え方ではなく、奥行きのある自然な嵌合にしてください。左右でサイズ感と見え方の整合を取り、どちらか一方だけが不自然に大きい状態をなくしてください。

カーテンの横幅、上部ギャザーの密度、レールのカーブとの関係も自然に見えるように整えてください。ただし、レール本体の形状、太さ、カーブ、色、素材、窓、壁、床、椅子、植物、光の方向、構図は変更しないでください。編集は左右エンドキャップ周辺のサイズ補正のみに限定し、切り抜き感、浮き、輪郭ハロ、遠近感不一致のない、実写の商品写真として自然な仕上がりにしてください。
```

## 補強用の一文
```text
図1はサイズ参照専用であり、図2に写っている現在のエンドキャップ形状を完全に維持したまま、軽い調整ではなく、過大感が消えるまで明確に縮小してください。
```

## ネガティブプロンプト
```text
changed end cap shape, redesigned end cap, replaced end cap design, altered hook shape,
oversized end cap, still too large, uneven left and right size, detached cap, floating cap,
pasted object, visible gap, wrong fit, wrong perspective, distorted plastic part, stretched part,
flattened part, halo edge, cutout look, mismatch lighting, mismatch shadow, mismatch sharpness,
changed rail shape, changed rail thickness, changed rail curve, altered curtain design,
changed room layout, extra accessories, cartoon, illustration, blur, low detail
```
