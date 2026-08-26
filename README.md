# Impasto Frame

`Impasto Frame` 将照片或文字场景转译为具有作者性构图、自然人物表现、场景化色彩和轻度油画触感的原创绘画画面。

它先重新组织大形、前后关系、主体照明和色彩层级，再把有限的立体笔触放在真正能够说明空间的位置，例如遮挡、接触、折痕、形体转折和前景分离。天空、水面、皮肤、雾气等连续区域保持连贯，不会被全画面马赛克、拼贴色块或厚重浮雕破坏。

## 色彩特点

- 先分析原图的中性色、白平衡、主色面积、局部色和光源，再决定是否调色。
- 默认尊重原图的冷暖倾向，不自动套用暖色、青橙或互补色模板。
- 可选择保留并优化、重新平衡或重新设计色域，但每次变化都必须有明确的空间、材质、光源或叙事所有者。
- 将局部色、主体照明、环境反射和最终调色分开，避免肤色偏橙、绿植偏黄、雪景发暖或整张图被单一色罩污染。
- 背景使用带色灰和低色噪组织空间，不用灰雾、全局去饱和或抬黑来制造“电影感”。

## 适合用来做什么

- 将人物、风景、建筑、雪景、海景和城市照片转成原创绘画画面。
- 保留人物身份、动作和关键关系，同时主动调整裁切、主体尺度、负空间、光形与色域。
- 为伞、服装、建筑、机械等显著主体重新设计轮廓、折面、材质和图案节奏，避免逐像素复刻。
- 用轻度、关系导向的油画笔触增强前后层次，而不是把整张画面拼成厚颜料块。

## 使用方法

上传图片后可以直接说：

```text
使用 $impasto-frame。
保留：{人物身份、动作、关键地标或主体关系}
希望强化：{构图、主体照明、前后关系或绘画质感}
色彩：{参考原图 / 保留并优化 / 重新平衡 / 重新设计色域}
避免：自动暖色调、全局滤镜、马赛克笔触、拼贴色块、厚重浮雕、道具照抄
```

如果没有指定色彩方向，Skill 会优先参考原图的白平衡、冷暖倾向和受保护的局部色，再做必要的层级优化。

显式调用：`$impasto-frame`

## English

`Impasto Frame` transforms a photo or text scene into an original painterly frame with authored composition, natural focal treatment, source-led colour and restrained tactile oil-paint depth.

It analyses source neutrals, white balance, colour ownership and motivated light before grading. The source temperature remains the default; warm/cool opposition, complementary colour and stronger chroma are used only when a named light, material, spatial region or narrative function justifies them. Local colour, illumination, environment influence and final grade stay separate, preventing automatic amber skin, yellow-green vegetation, warmed snow or one global cast.

Use it for a strongly stylized painted result with visible shape and composition authorship—not a global texture filter, literal prop trace, dirty colour wash, mosaic surface or all-over heavy impasto.

## Install

```bash
git clone https://github.com/zcjunn/impasto-frame.git ~/.codex/skills/impasto-frame
```

## License

This project uses the [Personal Non-Commercial License](LICENSE). Personal, non-commercial use only. Commercial use requires prior explicit written permission from zcjun.
