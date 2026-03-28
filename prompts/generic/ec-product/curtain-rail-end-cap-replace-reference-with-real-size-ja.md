# 参照形状と実寸参照で図1の両端エンドキャップを自然に差し替えるプロンプト

## 用途
図1のカーテン両端エンドキャップを、図2のエンドキャップ形状へ差し替えたいときに使う Nano Banana Pro 用プロンプトです。図2を形状参照、図3を実寸参照として使い、図1のレールや空間に自然になじむように置換する用途を想定しています。

## メインプロンプト
```text
図1を編集対象画像として、図1のカーテン両端に付いているエンドキャップを、図2のエンドキャップ形状に差し替えてください。図2は差し替えるエンドキャップの形状参照、図3はそのエンドキャップの実物サイズ参照として使ってください。図1の左右端に、図2と同じデザインのエンドキャップを自然に取り付けてください。

図2のエンドキャップは、正面形状、側面形状、先端の造形、厚みの取り方、金具の構成を保ったまま、図1のカーテンレール端部に合うように自然に再構成してください。図3の実寸感を参考にして、図1のカーテンやレールの見え方に対して大きすぎたり小さすぎたりしない、実物らしいサイズへ調整してください。サイズは図1のカーテンとレールのバランスに合わせて微調整してよいですが、図2の形状自体は変えないでください。

エンドキャップはレール端の開口に正しく差し込まれているように見せ、先端に貼り付いたような見え方ではなく、奥行きのある自然な嵌合にしてください。左右でサイズ感、角度、見え方の整合を取り、図1の遠近や光に合った自然な立体としてなじませてください。単純に平面的に貼り付けたり、図2や図3をそのまま切り抜いて載せたりせず、図1の撮影条件に合う実写の一部として再構成してください。

図1のカーテンレール本体、カーテン、壁、窓、床、家具、光、構図は変更しないでください。編集は左右エンドキャップ周辺に限定し、切り抜き感、浮き、輪郭ハロ、サイズ不一致、遠近感不一致のない、自然な商品写真として仕上げてください。
```

## 補強用の一文
```text
図2は形状参照、図3は実寸参照として役割を分けて使い、図1の左右端に自然に装着された一体物として見えるように、サイズだけは図1のレールとカーテンに合わせて微調整してください。
```

## ネガティブプロンプト
```text
wrong end cap shape, mixed inconsistent shape, wrong back shape, wrong side profile,
wrong reference usage, copied flat part from reference, detached cap, floating cap,
shallow insertion, visible gap, pasted object, cutout look, halo edge,
wrong scale, oversized cap, undersized cap, distorted plastic part, stretched part,
flattened part, mismatch lighting, mismatch shadow, mismatch sharpness,
changed rail shape, changed rail opening, altered curtain design, changed room layout,
extra accessories, cartoon, illustration, blur, low detail
```
