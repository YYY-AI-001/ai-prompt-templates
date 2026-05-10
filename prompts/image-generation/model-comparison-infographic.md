# 模型对比信息图提示词

## 资产信息

| 字段 | 内容 |
|------|------|
| 类型 | AI 生图 / 信息图 |
| 适用场景 | 生成模型分类、能力地图、学习路线的信息图视觉 |
| 适用模型/平台 | FLUX / ERNIE-Image / GLM-Image / 其他信息图模型 |
| 输入变量 | `{模型分类}`、`{对比维度}`、`{目标读者}` |
| 输出结果 | 信息图视觉 prompt 和后期排版建议 |
| 标签 | 模型对比, 信息图, AI生图, 教程 |
| 版本 | v1.0 |

## 标准版提示词

```text
请为 `{目标读者}` 设计一张 AI 模型对比信息图的视觉提示词。

模型分类：{模型分类}
对比维度：{对比维度}

要求：
- 信息层级清楚
- 适合后期加入中文文字
- 不要让模型直接生成大量中文
- 画面像教程资料页，而不是广告海报

请输出：
1. 生图英文 prompt
2. 中文版画面说明
3. 后期排版建议
4. 不建议出现的元素
```

## 增强版提示词

```text
Create a clean infographic-style background for comparing AI image generation models.
The design should show several grouped model cards, connected by subtle lines and arranged by capability categories: fast generation, Chinese text rendering, image editing, video generation, multimodal understanding.
Use a modern editorial data-visualization style, light background, blue and neutral accents, clear spacing, no fake readable text.
Leave space for manually added Chinese labels and comparison notes.
```

## 使用建议

适合模型扫盲文章。若模型支持文字生成，可以尝试让它生成英文短标签，但正式中文信息建议后期排版。

## 版本记录

- v1.0：初版
