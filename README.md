# 源力魔方开源模型提示词库

一个只收纳 **AI 生图 / AI 生视频提示词** 的纯提示词库。

这里只保留可直接用于图像和视频生成的 prompt 示例，围绕主流开源模型的提示词习惯来组织。

## 可视化入口

现在仓库增加了一个轻量静态浏览器：[index.html](./index.html)

它可以用来：

- 按生图 / 生视频筛选提示词
- 按模型方向筛选提示词
- 搜索场景、模型和文件名
- 查看模型写法矩阵
- 快速打开或复制提示词文件路径

如果开启 GitHub Pages，可以把 `index.html` 作为提示词库的可视化首页。

## 模型写法指南

新增：[各模型高质量提示词写法](./guides/model-prompt-writing.md)

这份指南总结了不同模型更适合的 prompt 结构：

- FLUX / SD3.5 / HiDream：自然语言完整描述
- Qwen-Image / 中文图像模型：短文本、清晰版式、明确文字位置
- SDXL / Stable Diffusion：关键词分组、负面提示词、LoRA 触发词
- Wan / HunyuanVideo / CogVideoX：一个 prompt 对应一个镜头
- LTX / SkyReels / FramePack：连续镜头、自然段描述、稳定主体

## 覆盖方向

| 类型 | 模型 / 方向 | 说明 |
|------|------|------|
| 生图 | Universal | 适合大多数文生图模型的通用提示词结构 |
| 生图 | FLUX / FLUX.2 | 自然语言、摄影、电影感、产品图、概念图 |
| 生图 | Qwen-Image | 中文文字、海报、知识卡片、人像材质 |
| 生图 | SDXL / Stable Diffusion | 关键词结构、负面提示词、LoRA 友好 |
| 生图 | SD3.5 / HiDream / Chroma | 新一代 DiT 图像模型、摄影、广告、风格化 |
| 生图 | Hunyuan / GLM / ERNIE / LongCat / Z-Image | 国产开源图像模型常用场景 |
| 生视频 | Universal Video | 通用短镜头、图生视频、首尾帧 |
| 生视频 | Wan | T2V / I2V / First-Last-Frame 风格 |
| 生视频 | HunyuanVideo | 电影感运动、人物与场景镜头 |
| 生视频 | CogVideoX | 简短动作、产品展示、镜头运动 |
| 生视频 | LTX / Mochi | 快速短镜头、运动和风格测试 |
| 生视频 | SkyReels / Open-Sora / FramePack | 长镜头、开源视频模型、低门槛测试 |

## 仓库结构

```text
.
├── README.md
├── LICENSE
├── index.html
├── guides/
│   └── model-prompt-writing.md
└── prompts/
    ├── image/
    │   ├── universal/
    │   ├── flux/
    │   ├── qwen-image/
    │   ├── sdxl/
    │   ├── sd3-hidream/
    │   └── chinese-open-models/
    └── video/
        ├── universal/
        ├── wan/
        ├── hunyuan-video/
        ├── cogvideox/
        ├── ltx-mochi/
        ├── skyreels/
        ├── open-sora/
        └── framepack/
```

## 快速选择

| 你想做什么 | 先看 |
|------|------|
| 通用高质量生图 | [Universal Image](./prompts/image/universal/) |
| FLUX 风格自然语言提示词 | [FLUX](./prompts/image/flux/) |
| 中文海报 / 中文文字图 | [Qwen-Image](./prompts/image/qwen-image/) |
| SDXL / LoRA / 关键词风格 | [SDXL](./prompts/image/sdxl/) |
| SD3.5 / HiDream / Chroma | [SD3 + HiDream](./prompts/image/sd3-hidream/) |
| 国产开源模型测试 | [Chinese Open Models](./prompts/image/chinese-open-models/) |
| 通用 AI 视频短镜头 | [Universal Video](./prompts/video/universal/) |
| Wan 图生视频 / 首尾帧 | [Wan](./prompts/video/wan/) |
| HunyuanVideo 电影镜头 | [HunyuanVideo](./prompts/video/hunyuan-video/) |
| CogVideoX 简洁动作镜头 | [CogVideoX](./prompts/video/cogvideox/) |
| LTX / Mochi 快速视频测试 | [LTX / Mochi](./prompts/video/ltx-mochi/) |
| 长视频 / 开源视频模型测试 | [SkyReels](./prompts/video/skyreels/) / [Open-Sora](./prompts/video/open-sora/) / [FramePack](./prompts/video/framepack/) |

## 使用原则

### 生图

- FLUX / Qwen / 新一代图像模型：优先使用自然语言完整句子。
- SDXL / 传统 SD：关键词结构仍然有效，负面提示词更重要。
- 中文文字图：优先用 Qwen-Image、GLM-Image、ERNIE-Image 等更擅长文字的模型；重要文字建议后期排版复核。
- 产品图、封面图、信息图：提示词里要明确主体、构图、光线、材质、背景和用途。

### 生视频

- 一个 prompt 只描述一个镜头。
- 一个镜头只做一个主要动作。
- 明确主体、动作、镜头运动、光线、场景、时长。
- 图生视频优先使用参考图。
- 首尾帧模式适合控制姿势、转场和镜头起止状态。
- 避免长动作链，例如“走进房间、拿书、翻开、微笑、转身离开”。

## 参考来源

本库参考了公开模型文档和提示词社区的通用经验，包括 FLUX 自然语言提示词写法、Qwen-Image 文字渲染经验、Stable Diffusion 3.5 提示词结构、Wan / SkyReels / LTX 等视频模型的镜头描述方式，以及多个开源提示词库的分类方式。

所有提示词均重新整理为源力魔方自己的示例，不直接搬运第三方 prompt。
