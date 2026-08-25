# Impasto Frame Skill

`Impasto Frame Skill` 将照片或文字场景转译成具有作者性构图、场景化色彩、主体照度和轻度油画立体质感的原创绘画动画画面。

它的重点不是给原图套一层纹理，而是先提出一个缩略图可见的“主导演变化”，再用一个辅助变化强化：可以重排面积、裁切、负空间、前景遮挡、透视、光形或色域，也可以放大一个环境主体。随后重建大形、前后关系、光色层次和主体美感，最后只在说明空间关系的位置加入轻度厚薄笔触。天空、水面、皮肤和雾气等连续区域保持统一，不做全画面马赛克、拼贴或浮雕化处理。

人物照片采用“双重硬门槛”：五官、表情、视线、头颈、身材比例、姿态、肢体、手脚、服装轮廓以及人与道具/地面的接触关系都要保留；同时人物必须和新环境共享同一套光线、色彩、边缘、笔触与材质系统，不能成为贴在绘画背景上的照片剪影。

## 适合用来做什么

- 将人物、风景、建筑、雪景和海景转成原创绘画动画关键帧。
- 在保留身份、动作、主体关系和关键色彩的前提下，重新组织构图、光形和色域。
- 以主体、支撑层和背景三层预算控制局部对比、微对比、边缘密度、色度、色相噪声与纹理频率。
- 用带有场景色相的彩灰安静背景，同时保留空间、材质和照明，避免灰雾、全局去饱和或抬黑。
- 按“无 / 保留原有 / 主动建立”决定是否需要色彩对撞；主动建立时明确颜色所有者、交界位置、面积主次和视觉功能。
- 为显著道具重新设计轮廓、折面、材质和图案节奏，避免逐像素复刻。
- 用轻度关系导向的油画笔触增强前景、接触、遮挡、折痕和材质转折。

## 使用方法

把图片上传后直接描述：

```text
使用 $impasto-frame-skill。
保留：{人物/动作/地标/关键关系}
人物硬保真：五官、表情、视线、身材比例、姿态、肢体、手脚、服装轮廓与接触关系不变
主导演变化：{尺度接管/面积重排/裁切重构/前景遮挡/负空间扩张/透视压缩/光形重建/色域重排}
辅助变化：{强化主变化的第二个动作}
三层对比预算：{主体/支撑/背景的局部对比、微对比、边缘、色度、色相噪声、纹理频率}
色彩：{保留原色 / 重新平衡 / 重新脚本}
色彩对撞：{无 / 保留原有 / 主动建立：所有者、交界、面积主次、功能}
避免：人物几何变化、人物与环境风格分离、灰雾、全局滤镜、马赛克笔触、厚重浮雕、复制原图道具
```

显式调用：`$impasto-frame-skill`

## English

`Impasto Frame Skill` turns a photo or text scene into an original painterly animation frame with authored composition, scene-owned colour, motivated subject light and restrained tactile oil-paint depth.

It begins with one thumbnail-visible primary directorial change and one supporting move, then rebuilds large shapes, spatial relationships, a three-tier contrast budget, colour hierarchy and focal beauty. Local paint thickness is reserved for overlaps, contacts, folds, crests, edges and material changes; continuous sky, water, skin and haze stay coherent rather than becoming a tiled relief surface.

For human edit targets, facial and body geometry, expression, pose, limbs, hands, feet, clothing silhouette and contacts are hard-locked. The protected person must nevertheless share the environment's light, colour, edge, abstraction, material and grading system; neither geometry drift nor a pasted photographic person passes.

Use it when you want a strongly stylized painterly frame with controlled composition and material depth—not a global texture filter, literal prop tracing or all-over heavy impasto.

## 安装

```bash
git clone https://github.com/zcjunn/impasto-frame-skill.git ~/.codex/skills/impasto-frame-skill
```

## 许可证

本项目采用 [个人非商业许可证](LICENSE)。仅限个人、非商业使用；商业使用须事先获得 zcjun 的明确书面许可。
