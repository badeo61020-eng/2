# カーテンレールの色だけをエンドキャップに合わせる固定プロンプト

## 用途
カーテンレールとエンドキャップの色合わせが悪い画像に対して、カーテンレール本体の色だけをエンドキャップにそろえ、その他は一切変更させたくないときの Nano Banana Pro 用プロンプトです。

## メインプロンプト
```text
この画像を補正して、カーテンレール本体の色だけをエンドキャップの色に合わせてください。エンドキャップの白い色味、明るさ、質感にそろえて、レール全体も同系統の自然な白に調整してください。

変更してよいのはカーテンレール本体の色のみです。レールの形状、太さ、カーブ、端部の構造、エンドキャップの形状や色、カーテン、壁、窓、床、家具、光、構図は一切変更しないでください。色以外の修正、追加、削除は行わないでください。

レールだけが別素材や別色に見えないようにし、エンドキャップと同じ素材の一体パーツのように自然につながる白へ整えてください。黄味やグレー感が残らないようにしつつ、真っ白に塗りつぶした不自然な見え方ではなく、素材感と立体感は残してください。接合部で色差が出ないようにし、左右とも均一にそろえてください。
```

## 補強用の一文
```text
カーテンレール本体の色味調整以外は完全に現状維持とし、他の要素には一切手を加えないでください。
```

## ネガティブプロンプト
```text
changed rail shape, changed rail thickness, changed rail curve, changed end cap color,
changed end cap shape, altered curtain, altered wall, altered window, altered floor,
altered furniture, altered lighting, altered composition, overpainted rail, flat white fill,
loss of texture, halo edge, cutout look, cartoon, illustration, blur, low detail
```
