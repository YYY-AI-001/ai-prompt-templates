# 知识卡片视觉提示词

## 资产信息

| 字段 | 内容 |
|------|------|
| 类型 | AI 生图 / 内容视觉 |
| 适用场景 | 为公众号、知识星球、资料包生成知识卡片背景和视觉方向 |
| 适用模型/平台 | FLUX / Midjourney / 即梦 / 其他生图工具 |
| 输入变量 | `{知识主题}`、`{核心概念}`、`{视觉隐喻}`、`{配色}` |
| 输出结果 | 知识卡片视觉 prompt |
| 标签 | 知识卡片, 公众号, 资料包, 教程 |
| 版本 | v1.0 |

## 标准版提示词

```text
Create a clean educational knowledge-card visual about {知识主题}.
Use {视觉隐喻} as the main visual metaphor.
The image should feel like a modern AI tutorial card: clear layout, generous spacing, subtle technology elements, calm {配色} palette, high readability.
No readable text, no logo, no watermark.
Leave enough blank space for Chinese title and notes to be added later.
```

## 增强版提示词

```text
Generate a polished background image for a Chinese educational knowledge card.

Topic: {知识主题}
Core concept: {核心概念}
Visual metaphor: {视觉隐喻}
Color palette: {配色}

Design requirements:
- 4:5 or 16:9 composition
- Clean editorial style
- One clear visual focus
- Subtle AI workflow elements such as nodes, lines, cards, or layers
- Leave safe space for manually added Chinese text
- Avoid dense UI, fake text, random symbols, and stock-photo feeling
```

## 使用建议

适合给公众号文章配图、知识星球资料封面、资料包说明页使用。中文标题建议用后期排版。

## 版本记录

- v1.0：初版
