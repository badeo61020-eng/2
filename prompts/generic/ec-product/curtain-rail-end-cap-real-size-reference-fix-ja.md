# 実サイズ参照で両端エンドキャップの大きさだけを修正するプロンプト

## 用途
参照画像に写っている実物エンドキャップのサイズ感を基準にして、生成画像内の左右エンドキャップが大きすぎる場合に、形状は一切変えず大きさだけを自然に補正したいときの Nano Banana Pro 用プロンプトです。

## メインプロンプト
```text
図1はエンドキャップ実物のサイズ参照画像、図2は補正対象画像です。図1の実物サイズ感を参考にして、図2の左右両端に付いているエンドキャップの大きさだけを自然に小さく修正してください。図2ではエンドキャップが実サイズ感より大きく見えるため、実物に近い比率へ縮小してください。

重要なのはサイズ補正のみです。エンドキャップの形状、輪郭、厚み、先端の造形、金具の構成、デザインは一切変更しないでください。別形状に作り直したり、左右反転した別パーツに置き換えたりせず、現在写っているエンドキャップそのものを同じ形のまま縮小してください。

左右のエンドキャップはカーテンレール断面に対して実物らしい比率に補正し、レール端の開口に自然に差し込まれている見え方を維持してください。先端に貼り付いたような見え方ではなく、奥行きのある自然な嵌合にしてください。左右でサイズ感と見え方の整合を取り、どちらか一方だけが不自然に大きい状態をなくしてください。

カーテンの横幅、上部ギャザーの密度、レールのカーブとの関係も自然に見えるように整えてください。ただし、レール本体の形状、太さ、カーブ、色、素材、窓、壁、床、椅子、植物、光の方向、構図は変更しないでください。編集は左右エンドキャップ周辺のサイズ補正のみに限定し、切り抜き感、浮き、輪郭ハロ、遠近感不一致のない、実写の商品写真として自然な仕上がりにしてください。
```

## 補強用の一文
```text
図1はサイズ参照専用であり、形状変更の参照には使わず、図2に写っている現在のエンドキャップ形状を完全に維持したまま、実物比率に合わせて縮小のみ行ってください。
```

## ネガティブプロンプト
```text
changed end cap shape, redesigned end cap, replaced end cap design, altered hook shape,
wrong reference usage, copied flat part from reference, oversized end cap, uneven left and right size,
detached cap, floating cap, pasted object, visible gap, shallow insertion, wrong fit,
wrong perspective, distorted plastic part, stretched part, flattened part, halo edge,
cutout look, mismatch lighting, mismatch shadow, mismatch sharpness, changed rail shape,
changed rail thickness, changed rail curve, altered curtain design, changed room layout,
extra accessories, cartoon, illustration, blur, low detail
```
