# Character Design Sheet

适用模型：FLUX、Qwen-Image、SDXL、HunyuanImage、GLM-Image

## Prompt

```text
A clean character design sheet for an original sci-fi courier. The character is a young woman in her late twenties with short black hair, sharp eyes, and a compact athletic build. She wears a weathered gray utility jacket, lightweight tactical pants, fingerless gloves, and a small cross-body delivery pack with glowing blue indicators. Show front view, side view, and three-quarter view on the same sheet. Neutral light background, consistent outfit across all views, realistic concept art style, clear silhouette, detailed fabric folds, functional design, no text.
```

## Negative Prompt

```text
different outfits, multiple unrelated characters, inconsistent face, extra limbs, exaggerated armor, fantasy costume, text labels, watermark, messy layout, low detail
```

## Notes

- 多视图角色图容易不一致，最好加“consistent outfit across all views”。
- 如果模型支持参考图，先生成单张角色定稿，再扩展三视图。
