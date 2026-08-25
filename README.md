# Impasto Frame Skill

`Impasto Frame Skill` 将照片或文字场景转译成具有作者性构图、场景化色彩、主体照度和轻度油画立体质感的原创绘画动画画面。

它的重点不是给原图套一层纹理，而是先重建大形、前后关系、光色层次和主体美感，再把有限的厚薄笔触放在雪、草、布料、伞面、岩石、屋顶等能够说明空间关系的位置。天空、水面、皮肤和雾气等连续区域保持统一，不做全画面马赛克、拼贴或浮雕化处理。

## 适合用来做什么

- 将人物、风景、建筑、雪景和海景转成原创绘画动画关键帧。
- 在保留身份、动作、主体关系和关键色彩的前提下，重新组织构图、光形和色域。
- 为显著道具重新设计轮廓、折面、材质和图案节奏，避免逐像素复刻。
- 用轻度关系导向的油画笔触增强前景、接触、遮挡、折痕和材质转折。

## 使用方法

把图片上传后直接描述：

```text
使用 $impasto-frame-skill。
保留：{人物/动作/地标/关键关系}
希望强化：{主体、光形、前后关系或色彩层次}
允许的构图变化：{主体尺度/裁切/负空间/前景遮挡/透视压缩}
色彩：{保留原色 / 重新平衡 / 重新脚本}
避免：全局滤镜、马赛克笔触、拼贴色块、厚重浮雕、复制原图道具
```

显式调用：`$impasto-frame-skill`

## English

`Impasto Frame Skill` turns a photo or text scene into an original painterly animation frame with authored composition, scene-owned colour, motivated subject light and restrained tactile oil-paint depth.

It rebuilds large shapes, spatial relationships, colour hierarchy and focal beauty first. Local paint thickness is reserved for overlaps, contacts, folds, crests, edges and material changes; continuous sky, water, skin and haze stay coherent rather than becoming a tiled relief surface.

Use it when you want a strongly stylized painterly frame with controlled composition and material depth—not a global texture filter, literal prop tracing or all-over heavy impasto.

## 安装

```bash
git clone https://github.com/zcjunn/impasto-frame-skill.git ~/.codex/skills/impasto-frame-skill
```

## 许可证

本项目采用 [个人非商业许可证](LICENSE)。仅限个人、非商业使用；商业使用须事先获得 zcjun 的明确书面许可。
