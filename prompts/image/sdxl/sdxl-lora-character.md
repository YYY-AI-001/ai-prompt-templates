# SDXL LoRA Character Prompt

适用模型：SDXL + 角色 LoRA / 风格 LoRA

## Positive Prompt

```text
<lora:character_lora_name:0.75>, full body character portrait, original female courier character, short black hair, gray utility jacket, cross-body delivery bag, fingerless gloves, standing pose, neutral studio background, detailed clothing folds, realistic concept art, clean silhouette, front view, high detail, sharp focus
```

## Negative Prompt

```text
wrong character, inconsistent face, different outfit, extra limbs, extra fingers, bad hands, bad anatomy, blurry, low quality, messy background, watermark, text, logo
```

## Suggested Settings

```text
Steps: 28-36
CFG: 5-7
Sampler: DPM++ 2M Karras
Size: 832x1216
LoRA strength: 0.6-0.85
```

## Notes

- 角色 LoRA 的权重不要一开始拉满。
- 想保持服装一致，把服装描述写在 LoRA 后面。
