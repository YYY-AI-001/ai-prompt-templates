# FLUX 自然语言提示词构建器

## 资产信息

| 字段 | 内容 |
|------|------|
| 类型 | AI 生图 |
| 适用场景 | 将关键词式描述改写成适合 FLUX 的自然语言 prompt |
| 适用模型/平台 | FLUX / FLUX.2 / 其他自然语言友好模型 |
| 输入变量 | `{主体}`、`{场景}`、`{光线}`、`{镜头}`、`{风格}`、`{用途}` |
| 输出结果 | 英文自然语言 prompt、中文说明、负面约束 |
| 标签 | FLUX, 生图, 自然语言, 提示词 |
| 版本 | v1.0 |

## 标准版提示词

```text
请把下面的关键词描述，改写成适合 FLUX 的自然语言生图提示词。

主体：{主体}
场景：{场景}
光线：{光线}
镜头：{镜头}
风格：{风格}
用途：{用途}

要求：
- 不要使用 SD 时代的关键词堆砌
- 使用完整英文句子
- 主体、场景、光线、镜头、风格要自然连接
- 如果需要文字，请建议后期排版，不强迫模型生成中文文字

请输出：
1. English Prompt
2. 中文解释
3. 可选负面提示
4. 适合的画幅比例
```

## 增强版提示词

```text
You are a prompt editor for FLUX-style image models. Convert the user's rough keywords into a precise natural-language prompt.

Input:
Subject: {主体}
Environment: {场景}
Lighting: {光线}
Camera and lens: {镜头}
Style: {风格}
Use case: {用途}

Rules:
- Use coherent sentences, not keyword stacking.
- Describe visible details only.
- Keep one clear subject and one visual focus.
- Include camera, lighting, composition, and material details when useful.
- Avoid fake quality tags such as "masterpiece" unless they describe a real visual property.
- Do not ask the model to render important Chinese text; suggest post-editing instead.

Output:
## Prompt
## Why it works
## Optional negative prompt
## Parameter notes
```

## 使用建议

适合把旧 SD 风格关键词升级成 FLUX 风格。它不是单独的出图 prompt，而是 prompt 改写器。

## 版本记录

- v1.0：初版
