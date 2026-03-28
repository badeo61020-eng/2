# 门锁图添加“正在拧钥匙的手”编辑提示词

## 用途

用于基于原图进行局部真实感编辑，在不改变门、门锁、安全链和整体构图的前提下，给钥匙位置自然添加一只正在拧钥匙的手。

## 主提示词

```text
请基于这张原图进行局部真实感编辑，保留门、门锁、安全链、钥匙和整体构图不变。

在右侧钥匙位置自然添加一只正在拧钥匙的成年人手部，手正握住钥匙头并做“正在旋转开锁”的动作，姿势自然，手指受力合理，解剖真实。
手从画面右侧自然伸入，只出现手和少量手腕，不要出现完整手臂，不要遮挡过多门锁结构。
保持钥匙仍然插在锁芯中，表现出“正在拧动钥匙”的瞬间，而不是已经拔出或已经开完。
光线方向、阴影、透视、清晰度、肤色反射要与原图一致，让手和门锁像原本就在同一张照片里一样自然。
门锁表面的反光、手指与钥匙接触处的遮挡关系、钥匙圈下垂状态都要合理真实。
整体风格保持为干净、写实、产品摄影级别的近景照片，不要改变门和锁的材质、颜色、比例。

避免贴图感、避免手部变形、避免多余手指、避免多余钥匙、避免钥匙位置错位、避免夸张动作、避免卡通感、避免模糊。
```

## 负面提示词

适用于支持 negative prompt 的模型。

```text
deformed hand, extra fingers, missing fingers, fused fingers, broken wrist, unnatural grip,
floating hand, pasted hand, mismatch lighting, mismatch perspective, wrong shadow,
key removed, extra key, duplicated keyring, distorted lock, changed door structure,
cartoon, illustration, blur, low detail, bad anatomy
```

## 短版约束

当模型容易乱改整体结构时，可额外补一句：

```text
只在钥匙区域新增一只真实手部，其他物体和构图保持不变，表现“手正握住插在锁里的钥匙并轻微旋转”的瞬间。
```

## 使用建议

- 优先使用“局部编辑 / inpaint / reference edit”模式，而不是纯文生图。
- 如果手容易挡住锁芯，可以补一句“手指不要完全遮住钥匙插入位置”。
- 如果动作不明显，可以补一句“钥匙有轻微旋转角度变化，但仍保持真实自然”。
- 如果出现贴上去的感觉，可以补一句“hand integrated naturally with matching light, shadow, perspective, and focus”。
