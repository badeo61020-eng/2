# 両端エンドキャップのサイズ・収まりを強く補正する統合プロンプト

## 用途
エンドキャップが大きすぎる、レール端部からはみ出している、収まりが浅い、といった問題をまとめて補正したいときの Nano Banana Pro 用プロンプトです。形状は変えず、サイズだけを明確に縮小し、レール端部に自然に収める用途を想定しています。

## メインプロンプト
```text
この画像の左右両端に付いているエンドキャップは、現在明らかに大きすぎるため、現在よりはっきり小さくしてください。軽い微調整ではなく、過大感が消えるまで明確に縮小してください。補正後は、端部パーツだけが悪目立ちせず、カーテンレール端部の太さと自然に釣り合って見えるサイズにしてください。

重要なのはサイズ補正のみです。エンドキャップの形状、輪郭、厚み、先端の造形、金具の構成、デザインは変更しないでください。別形状に作り直したり、別パーツに置き換えたりせず、現在写っているエンドキャップそのものを同じ形のまま縮小してください。

エンドキャップはカーテンレールの端部に正しく収まっている状態にしてください。レール端部から外側へ余分に突き出している部分があれば、そのはみ出した部分だけを削除してください。エンドキャップはレールの終端で止まり、外側へ延長しないでください。レール端の開口に正しく差し込まれた見え方にし、先端に貼り付いたような見え方ではなく、奥行きのある自然な嵌合にしてください。接合部はぴったり合い、隙間、浮き、段差、不自然な重なりが見えないようにしてください。

左右でサイズ感、角度、見え方の整合を取り、どちらか一方だけが不自然に大きい、または大きく張り出して見える状態をなくしてください。カーテンレール本体、カーテン、壁、窓、光、構図は変更せず、編集は左右エンドキャップ周辺の補正のみに限定してください。切り抜き感、浮き、輪郭ハロ、遠近感不一致のない、自然な実写の商品写真として仕上げてください。
```

## 補強用の一文
```text
エンドキャップは形を変えずに、現在より一段はっきり小さくし、レール端部からはみ出した部分だけを自然に消して、終端にきれいに収まる状態へ補正してください。
```

## ネガティブプロンプト
```text
changed end cap shape, redesigned end cap, replaced end cap design, altered hook shape,
still too large, protruding part outside rail end, detached cap, floating cap, visible gap,
pasted object, cutout look, halo edge, wrong fit, shallow insertion, distorted plastic part,
stretched part, flattened part, mismatch lighting, mismatch shadow, mismatch sharpness,
changed rail shape, changed curtain, changed room background, extra accessories,
cartoon, illustration, blur, low detail
```
