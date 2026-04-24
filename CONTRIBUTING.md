# Contributing to AI Prompt Templates

Thank you for your interest in contributing! This guide covers everything you need to know about submitting high-quality prompts to this repository.

---

## Table of Contents

- [Submission Standards](#submission-standards)
- [File Format Specification](#file-format-specification)
- [File Naming Conventions](#file-naming-conventions)
- [Submission Process](#submission-process)
- [Review Criteria](#review-criteria)

---

## Submission Standards

### Required Fields

All submitted prompts must include:

| Field | Description | Example |
|:------|:------------|:--------|
| Positive Prompt | English, complete natural sentences | `A young woman with...` |
| Negative Prompt | Keywords to exclude unwanted elements | `cartoon, anime, deformed...` |
| Parameter Recommendations | Steps / CFG / Sampler / Resolution | `Steps: 25-30, CFG: 3.5` |
| Effect Description | Chinese, describes the generated result | 生成细节丰富的人像照片... |
| Use Cases | Chinese, lists applicable scenarios | 商业写真、简历照片... |

### Quality Checklist

Before submitting, verify:

- [ ] English prompt is grammatically correct and free of garbled text
- [ ] Prompt works out-of-the-box without debugging
- [ ] Parameter recommendations have been tested
- [ ] File naming follows conventions (lowercase + hyphens)
- [ ] No copyrighted artist names (except generic style descriptors)
- [ ] Frontmatter is complete and valid YAML

---

## File Format Specification

Every prompt file must use this Frontmatter structure:

```yaml
---
name: prompt-name              # Unique identifier (lowercase + hyphens)
description: 中文描述          # Brief description in Chinese
type: FLUX | MJ | ComfyUI | Natural-Language   # Platform type
subtype: photorealistic | cinematic | ...     # Sub-category
tags: [tag1, tag2, tag3]      # Searchable tags
created: YYYY-MM-DD           # Creation date
tested: true | false           # Whether tested
difficulty: 1-5               # Difficulty level (optional)
---
```

### Complete Example

```yaml
---
name: portrait-master
description: 生成高度逼真的商业级人像照片，适合写真、产品展示等场景
type: FLUX
subtype: photorealistic
tags: [人像, 商业, 写实]
created: 2026-04-24
tested: true
difficulty: 3
---
```

### Body Structure

After the Frontmatter, each file should contain:

```markdown
# [Title]

## 效果描述

[Chinese description of the generated result]

## 适用场景

- [Use case 1]
- [Use case 2]
- [Use case 3]

## 正向提示词

```
[English prompt text]
```

## 负面提示词

```
[Negative prompt keywords]
```

## 参数建议

| 参数 | 值 |
|:-----|:---|
| Steps | 25-35 |
| CFG | 3.5-5 |
| Sampler | euler_ancestral |
| 分辨率 | 1024×1024 |
```

---

## File Naming Conventions

```
# Format: platform-type-name.md (lowercase + hyphens only)

# FLUX prompts
flux-portrait-master.md
flux-cinematic-landscape.md
flux-illustration-chinese.md

# Midjourney prompts
mj-portrait-emotional.md
mj-fantasy-dragon.md

# ComfyUI workflows
comfyui-portrait-workflow.md
comfyui-cinematic-workflow.md

# Natural Language prompts
nl-brand-story.md
nl-product-showcase.md
```

---

## Submission Process

### Via GitHub Pull Request

```bash
# 1. Fork this repository
# Click the "Fork" button on GitHub

# 2. Clone your fork
git clone https://github.com/YOUR-USERNAME/ai-prompt-templates.git
cd ai-prompt-templates

# 3. Create a new branch
git checkout -b feature/add-flux-portrait

# 4. Add your prompt file
# Place in the appropriate prompts/{TYPE}/ subdirectory

# 5. Commit with clear message
git add prompts/FLUX/photorealistic/your-new-prompt.md
git commit -m 'Add: FLUX 新提示词名称'

# 6. Push to your fork
git push origin feature/add-flux-portrait

# 7. Open a Pull Request on GitHub
# Fill in the PR template with:
#   - What the prompt does
#   - What parameters were tested
#   - Any relevant generated examples
```

### Commit Message Format

```
Add: [TYPE] Prompt name (Chinese)
Fix: [TYPE] Fix description
Update: [TYPE] Updated prompt name
Docs: Documentation updates
```

Examples:
- `Add: FLUX 电影感人像提示词`
- `Add: MJ 奇幻龙题材`
- `Fix: ComfyUI 人像工作流参数`
- `Update: FLUX-GUIDE 参数参考`

---

## Review Criteria

PRs are reviewed for:

| Criterion | Description |
|:----------|:------------|
| **Usability** | Prompt works without debugging |
| **Parameters** | Settings are reasonable and tested |
| **Format** | Follows file format specification |
| **Copyright** | No unauthorized artist names or copyrighted content |
| **Grammar** | English content is error-free |
| **Completeness** | All required fields present |

### Response Time

- PRs are typically reviewed within **3-5 business days**
- Feedback will be provided via GitHub PR comments
- Once approved, your contribution will be merged

---

## Questions?

- 🐛 Found a bug? [Open an Issue](https://github.com/sourcecube/ai-prompt-templates/issues)
- 💡 Have a feature request? [Open an Issue](https://github.com/sourcecube/ai-prompt-templates/issues)
- 💬 Need help? [Discussions](https://github.com/sourcecube/ai-prompt-templates/discussions)

---

<div align="center">

**Thank you for contributing to AI Prompt Templates!**

</div>