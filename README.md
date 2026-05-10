# 源力魔方提示词资产库

这里不是“提示词收藏夹”，而是一个面向 **AI 工作流创作** 的提示词资产库。

目标是把一次性 prompt 整理成可以复制、修改、分类、复用和持续迭代的资产。

## 这个库解决什么问题

很多提示词的问题不是“不够高级”，而是：

- 只能用一次，下次找不到
- 变量没有抽出来，不能复用
- 不知道适合哪个模型或平台
- 没有使用说明，别人复制后不会改
- 没有版本和标签，积累不起来

所以这个库的基本单位不是“一个 prompt”，而是：

> **一张提示词资产卡片。**

## 适合谁用

| 用户 | 可以怎么用 |
|------|------|
| AI 生图新手 | 直接复制示例，理解提示词结构 |
| ComfyUI 初学者 | 学习工作流相关提示词怎么组织 |
| AI 视频创作者 | 参考分镜、首尾帧和角色一致性 prompt |
| 内容创作者 | 快速生成 B站封面、公众号图文和知识卡片 |
| 想做 AI 副业的人 | 把提示词、教程和资料包沉淀成公开资产 |

## 仓库结构

```text
.
├── README.md
├── LICENSE
├── docs/
│   ├── asset-standard.md
│   ├── research-notes.md
│   └── usage-guide.md
├── templates/
│   └── prompt-asset-card.md
└── prompts/
    ├── content-creator/
    │   ├── bilibili-cover.md
    │   ├── bilibili-script-3min.md
    │   ├── knowledge-star-post.md
    │   ├── title-pack-generator.md
    │   └── wechat-article-outline.md
    ├── image-generation/
    │   ├── chinese-model-scan-cover.md
    │   ├── flux-natural-language-builder.md
    │   ├── knowledge-card-visual.md
    │   ├── model-comparison-infographic.md
    │   └── workflow-diagram-style.md
    ├── ai-video/
    │   ├── character-consistency.md
    │   ├── keyframe-pair.md
    │   ├── seedance-reference-pack.md
    │   ├── seedance-shot-prompt.md
    │   └── storyboard-shot-list.md
    └── comfyui/
        ├── model-path-checklist.md
        ├── runninghub-to-local.md
        ├── workflow-debug-checklist.md
        └── workflow-explainer.md
```

## 当前资产

| 分类 | 资产 | 用途 |
|------|------|------|
| 内容创作 | [B站 AI 教程封面](./prompts/content-creator/bilibili-cover.md) | 为 AI 工作流教程生成高点击率封面方向 |
| 内容创作 | [3 分钟 B站脚本](./prompts/content-creator/bilibili-script-3min.md) | 生成 AI 工作流扫盲短视频脚本 |
| 内容创作 | [标题包生成器](./prompts/content-creator/title-pack-generator.md) | 为视频和公众号生成系列化标题 |
| 内容创作 | [公众号文章大纲](./prompts/content-creator/wechat-article-outline.md) | 将视频选题扩展为公众号图文 |
| 内容创作 | [知识星球延伸帖](./prompts/content-creator/knowledge-star-post.md) | 把公开内容延伸成星球资料和答疑 |
| AI 生图 | [国产/开源模型扫盲封面](./prompts/image-generation/chinese-model-scan-cover.md) | 为模型扫盲文章生成封面图 |
| AI 生图 | [FLUX 自然语言构建器](./prompts/image-generation/flux-natural-language-builder.md) | 把关键词改成自然语言生图 prompt |
| AI 生图 | [知识卡片视觉](./prompts/image-generation/knowledge-card-visual.md) | 生成教程卡片和资料包视觉 |
| AI 生图 | [模型对比信息图](./prompts/image-generation/model-comparison-infographic.md) | 生成模型分类和能力对比图 |
| AI 生图 | [工作流示意图风格](./prompts/image-generation/workflow-diagram-style.md) | 生成节点、流程、生产线概念图 |
| AI 视频 | [分镜表生成器](./prompts/ai-video/storyboard-shot-list.md) | 把短片想法拆成可执行镜头 |
| AI 视频 | [角色一致性锚点](./prompts/ai-video/character-consistency.md) | 生成跨镜头角色设定和锚点 |
| AI 视频 | [首尾帧提示词](./prompts/ai-video/keyframe-pair.md) | 为图生视频准备首帧和尾帧 |
| AI 视频 | [Seedance 参考素材包](./prompts/ai-video/seedance-reference-pack.md) | 整理文本、图像、视频、音频参考 |
| AI 视频 | [Seedance 单镜头提示词](./prompts/ai-video/seedance-shot-prompt.md) | 将分镜转成视频生成 prompt |
| ComfyUI | [工作流解释器](./prompts/comfyui/workflow-explainer.md) | 把复杂工作流解释给新手 |
| ComfyUI | [模型路径检查清单](./prompts/comfyui/model-path-checklist.md) | 检查模型、LoRA、VAE、ControlNet 放置位置 |
| ComfyUI | [工作流报错排查清单](./prompts/comfyui/workflow-debug-checklist.md) | 辅助整理 ComfyUI 排错内容 |
| ComfyUI | [RunningHub 转本地检查](./prompts/comfyui/runninghub-to-local.md) | 将云端工作流迁移到本地前做差异检查 |

## 资产卡片格式

每个提示词文件都尽量包含：

- 标题
- 类型
- 适用场景
- 适用模型/平台
- 输入变量
- 标准版提示词
- 增强版提示词
- 输出格式
- 使用建议
- 标签
- 版本记录

模板见：[prompt-asset-card.md](./templates/prompt-asset-card.md)

## 研究来源

本库的资产结构参考了公开 prompt engineering 指南、提示词库和 AI 视频/图像工作流资料，但所有资产均按「源力魔方」内容体系重新组织，不直接搬运第三方提示词。

整理记录见：[research-notes.md](./docs/research-notes.md)

## 和源力魔方内容体系的关系

这个库承接这些内容：

- B站：AI 工作流扫盲、ComfyUI 实操、AI 视频分镜
- 公众号：图文教程、模型观察、工具资讯
- GitHub：提示词资产和公开模板
- RunningHub：云端工作流学习和案例演示
- 知识星球：系统教程、资料库和答疑

## 配合 Codex Skill 使用

可以配合 `prompt-asset-director` 使用：

```text
用 $prompt-asset-director 把这个提示词整理成提示词资产卡片。
```

也可以配合 `seedance-storyboard-director` 使用：

```text
用 $seedance-storyboard-director 把这个短片想法拆成分镜，再生成 Seedance prompt。
```

## 维护原则

- 少而精，优先沉淀真实会用的资产
- 不堆玄学词，尽量写清楚变量和使用场景
- 每个 prompt 都要能被修改，而不是只能复制
- 优先服务 AI 工作流、ComfyUI、AI 视频和内容副业主线
