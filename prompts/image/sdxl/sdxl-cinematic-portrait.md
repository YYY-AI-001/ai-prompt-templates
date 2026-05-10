# SDXL Cinematic Portrait

适用模型：SDXL、JuggernautXL、RealVisXL、DreamShaperXL 等

## Positive Prompt

```text
cinematic portrait photo of a young Asian woman, natural skin texture, detailed eyes, subtle smile, black blazer, standing near a large window, soft diffused daylight, rim light, 85mm lens, shallow depth of field, realistic photography, film grain, muted teal and amber color grading, high detail, sharp focus
```

## Negative Prompt

```text
anime, cartoon, illustration, painting, doll-like skin, over-smoothed face, bad anatomy, bad hands, extra fingers, missing fingers, deformed eyes, crossed eyes, blurry, low resolution, jpeg artifacts, watermark, text, logo
```

## Suggested Settings

```text
Steps: 25-35
CFG: 5-7
Sampler: DPM++ 2M Karras / Euler a
Size: 1024x1024 or 832x1216
```

## Notes

- SDXL 更吃关键词结构和 negative prompt。
- 如果用 LoRA，把 LoRA 触发词放在主体后面，不要塞到最后。
