# 各模型高质量提示词写法

这份指南只讨论 **生图 / 生视频 prompt 怎么写**，不展开其他类型内容。

## 一句话原则

不同模型不是“越长越好”或“词越高级越好”，而是要匹配模型的理解习惯：

| 模型方向 | 更适合的写法 |
|------|------|
| FLUX / SD3.5 / HiDream | 完整自然语言，先说主体和关系，再补风格、光线、构图 |
| Qwen-Image / 中文图像模型 | 先放主体和文字内容，文字要短、准确、放在引号里 |
| SDXL / 传统 Stable Diffusion | 关键词分组 + 负面提示词 + 参数配合 |
| Wan / HunyuanVideo / CogVideoX | 一个 prompt 写一个镜头，一个镜头只保留一个核心动作 |
| LTX / SkyReels / FramePack | 用连续镜头语言写成一段自然流动的场景描述 |

## 生图模型

### Universal Image

适合不确定模型时使用。

高质量结构：

```text
主体 + 动作/状态 + 场景 + 构图 + 光线 + 材质/细节 + 风格 + 限制
```

写法要点：

- 先写画面里最重要的主体，不要先写风格词。
- 场景、构图、光线要具体，例如 `large window`, `soft diffused daylight`, `low-angle composition`。
- 如果是封面、海报、产品图，要写清楚“用途”和“留白”。
- 不要把互相冲突的风格堆在一起，例如同时要求写实摄影、油画、像素风。

适合模板：

```text
A high-quality image of {subject}, {action or pose}, located in {scene}. The composition is {framing}, with {lighting} and {color palette}. Include {material details}. The style is {visual style}. No text, no watermark, no logo.
```

### FLUX / FLUX.2

适合自然语言、摄影感、产品图、海报、概念图。

高质量结构：

```text
主体 + 动作 + 风格 + 环境上下文 + 摄影/构图参数 + 画面限制
```

写法要点：

- FLUX 更吃自然语言完整句，不需要大量堆 `masterpiece, best quality`。
- 词序很重要，越靠前的信息越像主指令。
- 负面提示词不是主要控制方式，尽量用正向表达替代，例如写 `clean background`，而不是只写 `no clutter`。
- 文本生成可做，但复杂中文排版不建议完全交给模型。

推荐写法：

```text
A cinematic product photograph of {product} on {surface}, {main visual feature}. The scene is lit by {lighting}, with {background} and {composition}. Shot with {lens or camera style}, {texture details}, clean modern commercial style, no readable text, no logo.
```

### Qwen-Image

适合中文文字、知识卡片、海报、人像材质和带排版需求的图片。

高质量结构：

```text
画面类型 + 主体 + 需要生成的文字 + 版式位置 + 字体气质 + 背景 + 限制
```

写法要点：

- 把最重要的主体和文字放在前面。
- 需要出现的文字用中文引号或英文引号包住。
- 文字越短越稳，标题优先，正文尽量后期排版。
- 明确“不要生成小字正文”“不要出现错别字”“留出空白区域”。
- 海报类 prompt 要同时写清楚标题位置、主体位置、背景层级。

推荐写法：

```text
一张{比例}中文海报，主题是“{主题}”。画面上方清晰显示标题：“{标题}”。主体是{主体描述}，位于画面{位置}。背景为{背景}，字体简洁有力，字形端正，不能出现错别字。不要生成小字正文，保留{留白位置}。
```

### SDXL / Stable Diffusion

适合 LoRA、风格模型、传统关键词控制和本地部署。

高质量结构：

```text
主体关键词, 外观关键词, 场景关键词, 镜头关键词, 光线关键词, 风格关键词, 质量关键词
```

写法要点：

- SDXL 仍然适合关键词分组，不必写成很长的自然段。
- negative prompt 很重要，尤其是手、脸、文字、水印、低清晰度。
- LoRA 触发词放在主体附近，不要塞到最后。
- 参数会强烈影响结果，prompt、CFG、采样器、尺寸要一起看。

推荐写法：

```text
{subject}, {appearance}, {pose}, {scene}, {lighting}, {camera lens}, {style}, high detail, sharp focus, realistic texture

Negative prompt: bad anatomy, bad hands, extra fingers, missing fingers, blurry, low resolution, watermark, text, logo
```

### SD3.5 / HiDream / Chroma

适合新一代 DiT 图像模型、写实广告、风格化插画和更强语义跟随。

高质量结构：

```text
风格方向 + 主体动作 + 场景关系 + 构图/镜头 + 光线色彩 + 细节限制
```

写法要点：

- 比 SDXL 更适合自然语言，但仍要保持结构清楚。
- 对广告图、文字图、产品图，最好明确“物体位置、标题位置、背景关系”。
- HiDream 写实场景要补足环境道具，让主体融入真实空间。
- Chroma / 动漫方向要固定角色锚点：发型、服装、眼睛、配饰、姿态。

推荐写法：

```text
A {style} image of {subject} {action}, placed in {scene}. The composition is {shot type}, with {lighting} and {color palette}. Include {specific details}. Keep the subject consistent, clean background, no text, no watermark.
```

### 国产开源图像模型

适合 Hunyuan、GLM、ERNIE、LongCat、Z-Image 等中文语义或快速生图方向。

高质量结构：

```text
中文主题 + 主体 + 画面结构 + 风格 + 文字/无文字要求 + 用途
```

写法要点：

- 中文 prompt 可以直接写，尤其是信息图、海报、知识卡片。
- 文字类图片要控制字数，标题和短标签优先。
- Z-Image / Fast 类模型适合短、清楚、直接的 prompt。
- 如果要跨模型测试，保持主体不变，只改风格、光线和负面约束。

推荐写法：

```text
生成一张{比例}图片，主题是“{主题}”。画面主体是{主体}，背景是{背景}，整体风格为{风格}。如果需要文字，只显示“{短标题}”，不要生成其他小字。画面清晰、构图稳定、无水印、无Logo。
```

## 生视频模型

### Universal Video

适合所有视频模型的基础写法。

高质量结构：

```text
镜头类型 + 主体 + 一个主要动作 + 场景 + 镜头运动 + 光线 + 时间长度/节奏 + 限制
```

写法要点：

- 一个 prompt 只写一个镜头。
- 一个镜头只保留一个主要动作。
- 动作要能被拍出来，不要写抽象心理活动。
- 镜头运动要明确，例如 `slow dolly in`, `camera pans right`, `handheld tracking`。
- 复杂剧情要拆成多个镜头，不要塞进一个 prompt。

推荐写法：

```text
A {shot type} of {subject} {single action} in {scene}. The camera {camera movement}, keeping {subject} centered. {Lighting and atmosphere}. Smooth realistic motion, stable identity, no subtitles, no watermark.
```

### Wan

适合 T2V、I2V、首尾帧、短镜头和镜头控制。

高质量结构：

```text
风格 + 主体 + 动作起点到终点 + 镜头跟随方式 + 背景 + 稳定性限制
```

写法要点：

- Wan 的 I2V / FLF 任务更适合写清楚“从什么状态到什么状态”。
- 首尾帧任务建议中文 prompt 也测试一版。
- 可以使用负面提示词控制闪烁、变形、字幕、水印。
- 不要在一个镜头里写多个连续动作，容易导致动作断裂。

推荐写法：

```text
电影感镜头，{主体}从{起始状态}逐渐{主要动作}到{结束状态}。镜头以{镜头运动}跟随主体，背景是{场景}，光线为{光线}。保持主体外观一致，动作自然流畅，无字幕、无水印。
```

### HunyuanVideo

适合电影感人物、场景运动、写实镜头和中文语义描述。

高质量结构：

```text
人物/场景 + 明确动作 + 环境变化 + 镜头语言 + 光线氛围 + 一致性要求
```

写法要点：

- 要把“人物外观锚点”写清楚，例如服装、发型、年龄感、颜色。
- 把情绪改成可见动作，例如“低头整理袖口”比“焦虑”更稳定。
- 镜头语言要服务动作，不要同时写多个互相冲突的机位。
- 如果是图生视频，prompt 重点写“希望图片怎么动”。

推荐写法：

```text
一段写实电影镜头，{人物锚点}在{场景}中{可见动作}。镜头{镜头运动}，背景中{环境运动}，光线为{光线}。人物服装、发型和面部特征保持一致，动作平滑自然，无字幕、无水印。
```

### CogVideoX

适合简洁动作、产品展示、基础镜头运动测试。

高质量结构：

```text
主体 + 一个动作 + 简单场景 + 简单镜头运动 + 画面限制
```

写法要点：

- prompt 不宜太绕，简洁、明确比复杂叙事更有效。
- 主体动作要具体，例如“转身看向镜头”“杯中咖啡缓慢旋转”。
- 产品演示要写清楚“产品不变形、logo 不出现、背景简洁”。

推荐写法：

```text
A clear video shot of {subject} {single action} in {simple scene}. The camera {simple movement}. Clean background, stable subject shape, smooth motion, no text, no watermark.
```

### LTX / Mochi

适合快速迭代、镜头动作测试、LTX 的声音/对白/完整镜头描述。

高质量结构：

```text
一段自然流动的场景描述：镜头开场 + 主体动作 + 环境 + 镜头移动 + 声音/氛围 + 收束状态
```

写法要点：

- LTX 更适合单段自然段，不要写成列表。
- 用现在时描述动作，让镜头从开始自然流到结束。
- 如果模型支持声音，可以写环境声、音乐、对白；对白要短。
- Mochi 方向建议先用简单动作和清楚镜头，不要一开始写复杂多人场景。

推荐写法：

```text
The shot opens on {scene}. {Subject} {main action} while {environment detail}. The camera {camera movement}, ending on {final framing}. {Lighting and atmosphere}. {Optional audio cue}. Smooth motion, coherent subject, no subtitles, no watermark.
```

### SkyReels / Open-Sora / FramePack

适合长镜头、开源视频模型测试、低显存视频续写和持续小动作。

高质量结构：

```text
连续镜头 + 稳定主体 + 环境递进 + 小幅动作 + 镜头路径 + 避免切镜
```

写法要点：

- 长镜头最怕“内容漂移”，所以要给一个清楚的主线人物或主线运动。
- Open-Sora 类模型适合先测风景、运动稳定性、相机推进。
- FramePack / 续写类模型适合可持续小动作，例如写字、调色、整理物品。
- 明确 `continuous shot`、`no sudden cuts`、`stable identity`。

推荐写法：

```text
A continuous shot of {subject} {slow action} in {scene}. The camera {camera path} while {environment changes gradually}. Keep the same subject, same clothing, and same location. No sudden cuts, no subtitles, no watermark.
```

## 通用质量检查

写完 prompt 后，至少检查 6 件事：

- 主体是否放在最前面。
- 是否只要求一个核心动作。
- 场景、光线、构图是否具体。
- 是否有冲突风格。
- 是否明确“不需要文字 / 需要哪些文字”。
- 视频 prompt 是否像一个镜头，而不是一整段剧情。

## 参考资料

- [FLUX Prompting Guide](https://docs.bfl.ai/guides/prompting_summary)
- [Qwen Image Models](https://docs.qwencloud.com/developer-guides/getting-started/image-models)
- [Stable Diffusion 3.5 Prompt Guide](https://stability.ai/learning-hub/stable-diffusion-3-5-prompt-guide)
- [Wan2.1 GitHub](https://github.com/Wan-Video/Wan2.1)
- [HunyuanVideo GitHub](https://github.com/Tencent-Hunyuan/HunyuanVideo)
- [LTX Prompting Guide](https://docs.ltx.video/open-source-model/usage-guides/prompting-guide)
