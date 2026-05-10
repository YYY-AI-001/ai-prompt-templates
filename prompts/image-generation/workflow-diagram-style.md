# AI 工作流示意图风格提示词

## 资产信息

| 字段 | 内容 |
|------|------|
| 类型 | AI 生图 / 教程配图 |
| 适用场景 | 生成 AI 工作流、节点、生产线概念图 |
| 适用模型/平台 | FLUX / Midjourney / 即梦 / 其他生图工具 |
| 输入变量 | `{工作流主题}`、`{核心节点}`、`{视觉风格}` |
| 输出结果 | 教程用概念示意图 |
| 标签 | 工作流, ComfyUI, 节点, 教程配图 |
| 版本 | v1.0 |

## 标准版提示词

```text
A clean visual metaphor for an AI workflow system about {工作流主题}.
Show several modular nodes connected by smooth lines, like a transparent production pipeline.
The nodes represent {核心节点}.
Use a modern educational diagram style, dark neutral background, soft blue and white highlights, clear spacing, no clutter.
The image should feel like a professional tutorial cover, not a complex engineering blueprint.
No readable text, no logo, no watermark.
```

## 增强版提示词

```text
Create a high-quality educational concept image showing an AI workflow as a reusable production line.
There are input materials on the left, connected processing nodes in the middle, and polished output images on the right.
Each node is visually distinct but simple, with subtle glowing connection lines.
The composition should explain "workflow" visually for beginners.
Style: clean, modern, calm technology, tutorial-friendly, high contrast, 16:9.
Avoid messy dashboards, tiny text, brand logos, cyberpunk overload, and unreadable UI.
```

## 使用建议

适合给公众号和 B站视频做工作流概念配图。尽量不要让模型生成文字，把文字说明留给后期排版。
