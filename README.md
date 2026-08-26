# Awesome Nano Banana API 🍌 — Prompts, Variants & One-Call Image Generation

> The most complete open guide to **Google Nano Banana — the viral AI image model (Nano Banana 2 & Pro, text-to-image + edit)** — a community prompt library and a single API to run every variant.

<p align="center">
  <a href="https://wavespeed.ai/nano-banana-2-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-nano-banana-api"><img src="https://img.shields.io/badge/▶_Run_Nano_Banana_2-Get_API_Key-00E5FF?style=for-the-badge&labelColor=0B0B0F" alt="Run Nano Banana 2"></a>
  <a href="https://wavespeed.ai/nano-banana-pro-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-nano-banana-api"><img src="https://img.shields.io/badge/Nano_Banana_Pro-Try_Now-7C3AED?style=for-the-badge&labelColor=0B0B0F" alt="Nano Banana Pro"></a>
</p>

<p align="center">
  <b>🌊 Powered by <a href="https://wavespeed.ai?utm_source=github&utm_medium=readme&utm_campaign=awesome-nano-banana-api">WaveSpeed AI</a> — serverless Nano Banana API, pay-as-you-go, zero cold starts.</b><br>
  <a href="https://wavespeed.ai/nano-banana-2-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-nano-banana-api"><b>→ Get a Nano Banana 2 API key</b></a> &nbsp;·&nbsp; <a href="https://wavespeed.ai/nano-banana-pro-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-nano-banana-api"><b>→ Try Nano Banana Pro</b></a>
</p>

---

> **Generate right now**
> ```bash
> npm i -g @wavespeed/cli && wavespeed login
> wavespeed run google/nano-banana-2/text-to-image -p "your prompt"
> ```
> No GPU, no cold start — the same endpoint powers every prompt below.

---

## 📖 Contents
1. [What is Nano Banana?](#what-is-nano-banana)
2. [Run it via API](#run-it-via-api)
3. [Model Variants](#model-variants)
4. [Prompt Library](#prompt-library) — 12 community prompts
5. [Related Model Guides](#related-model-guides)
6. [Contributing](#contributing)

---

## What is Nano Banana?

**Nano Banana** (Google) is the viral AI image model behind the internet's favorite character-consistent edits and figurine renders. WaveSpeed serves **Nano Banana 2** (+ lite / fast) and **Nano Banana Pro** (+ ultra / multi) — text-to-image and edit.

---

## Run it via API

One endpoint, submit + poll. Swap the model path for any variant below.

```bash
curl -s -X POST "https://api.wavespeed.ai/api/v3/google/nano-banana-2/text-to-image" \
  -H "Authorization: Bearer $WAVESPEED_API_KEY" -H "Content-Type: application/json" \
  -d '{"prompt": "A collectible figurine of a corgi astronaut on a clear acrylic base, studio light"}'
# → {"data": {"id": "<prediction_id>"}}

curl -s "https://api.wavespeed.ai/api/v3/predictions/<prediction_id>/result" \
  -H "Authorization: Bearer $WAVESPEED_API_KEY"
# → status: completed → outputs: ["<url>"]
```

**[→ Get your Nano Banana 2 API key](https://wavespeed.ai/nano-banana-2-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-nano-banana-api)** · pay-as-you-go, live pricing on each model page.

---

## Model Variants

All variants open in-browser with a copy-paste API snippet.

### Nano Banana 2 &nbsp;[▶ API](https://wavespeed.ai/nano-banana-2-api)
[text-to-image](https://wavespeed.ai/models/google/nano-banana-2/text-to-image) · [edit](https://wavespeed.ai/models/google/nano-banana-2/edit) · [fast](https://wavespeed.ai/models/google/nano-banana-2/text-to-image-fast) · [lite](https://wavespeed.ai/models/google/nano-banana-2-lite/text-to-image)

### Nano Banana Pro &nbsp;[▶ API](https://wavespeed.ai/nano-banana-pro-api)
[text-to-image](https://wavespeed.ai/models/google/nano-banana-pro/text-to-image) · [edit](https://wavespeed.ai/models/google/nano-banana-pro/edit) · [ultra](https://wavespeed.ai/models/google/nano-banana-pro/text-to-image-ultra) · [edit-multi](https://wavespeed.ai/models/google/nano-banana-pro/edit-multi)

> Full catalog: **[wavespeed.ai/nano-banana-2-api](https://wavespeed.ai/nano-banana-2-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-nano-banana-api)**

---

## Prompt Library

12 prompts curated from the Nano Banana creator community. Credit stays with the original author. Fill in `{...}` placeholders.

### 1. 浮世绘闪卡）
*by [@MANISH1027512](https://x.com/MANISH1027512)*

```
核心指令： 一张日式浮世绘风格的收藏级集换式卡牌设计，竖构图。插画风格需要紧密模仿《鬼灭之刃》的视觉美学，特征包括：粗细变化的墨笔轮廓线、传统木版画的配色方案，以及戏剧性的动态构图。

主体描述： 卡牌主角是 {角色名字}（称号：{柱名/称号}），处于动态战斗姿势，手持 {武器描述}。 角色正在施展 {呼吸法招式名称}，周围环绕着 {视觉特效描述}（例如：巨大的火焰 / 水龙 / 旋风），这些特效需要以 传统日式水墨画（Sumi-e）风格 呈现。

背景与材质： 背景需融合 纹理化的镭射闪卡（Holographic Foil）效果，在传统水墨元素下方闪烁。

边框： 图片周围要有 日本传统纹样（如青海波或麻叶纹）组成的装饰性边框。底部有一个风格化的横幅，上面用古朴的日式书法写着 “{日文汉字名字}”。
```

### 2. 人物分身术）
*by [@tapehead_Lab](https://x.com/tapehead_Lab)*

```
根据上传的参考角色，在一间宽敞的东京女孩公寓内拍摄一个真人场景——一间明亮、充满生活气息的单间，空间比例接近1LDK。房间应包含白色墙壁、温暖的木地板、米色窗帘、一张铺着柔软床品的矮床、一张摆放着化妆品的书桌、书架、绿植、一面立镜、一块地毯、散落的个人物品，以及位于房间后方的紧凑型厨房区域。房间必须具有强烈的景深，前景、中景和深邃的背景层次分明。

在房间内放置大约三十个与参考角色相同的角色（面部、发型、服装均与参考角色相同），每个角色都处于不同的动作或互动状态。调整角色之间的距离、比例、高度和可见度，使房间的密度看起来自然。

前景（非常靠近镜头/部分遮挡）：

- 人物走过镜头，略微失焦

- 一只手或肩膀进入画面

- 一人靠近镜头

- 一人半个身子在一株大植物后面

- 一人坐在正前方，正在扎头发

- 一人跪在桌旁整理物品

中景（主要房间区域）：

- 一人在床边伸展

- 一人坐在床上查看手机

- 一人趴在床上

- 一人伸手到床底下

- 一人在桌子上整理化妆品

- 一人在书架上翻书

- 一人站在镜子前

- 一人蹲在地毯上

- 一人靠墙

- 一人望向窗外

- 一人在调整窗帘

- 一人提着衣物

- 一人用杯子喝水

- 一人在整理枕头

- 一人坐在地板上吃零食

- 一人做小跳跃或动态模糊动作

- 一人移动小椅子

背景（深景/靠近厨房和……）走廊）：

- 一人站在炉灶旁喝水

- 一人打开橱柜

- 一人坐在凳子上

- 一人倚靠在门口

- 一人走向走廊

- 一人轮廓部分被冰箱遮挡

- 一人伸手够高处的架子

- 一人站在入口区域远处

- 一人透过走廊的框架隐约可见

- 一人坐在厨房地毯附近的地板上

确保强烈的层次感遮挡：前景人物部分遮挡中景人物，背景人物则显得更小，并呈现自然的透视衰减。将三十个人物自然地分散放置，避免对称或网格对齐。所有人物均采用柔和的自然日光照明，以确保画面与环境完美融合。

将人物置于与插画姿势和构图相匹配的实景背景中，同时忠实地保留插画的纹理和风格。运用逼真的光照、景深和微妙的拍摄效果，使插画与真实环境无缝衔接。
```

### 3. 根据文档生成流程图）
*by [@anderssandberg](https://x.com/anderssandberg)*

```
图示为根据论文 Armstrong, S., & Sandberg, A. (2013). Eternity in six hours: Intergalactic spreading of intelligent life and sharpening the Fermi paradox. Acta Astronautica, 89, 1-13 构建戴森群的过程。
```

### 4. 根据文章制作PPT）
*by [@op7418](https://x.com/op7418)*

```
帮我根据下面这个文章做一套中学生都能理解的中文PPT。

先写1个PPT大纲，规划出每一页的PPT的内容。

然后将每一页的PPT内容分别扔给Nana Banana pro生成对应页面的PPT，需要确保风格一致。

PPT的具体风格应该为请“Anthropic/Claude 风格”的“温暖学术人文主义”设计。

背景：使用暖米色/奶油色 (# F3F0E9) 作为底色，模仿高级纸张质感。

字体：标题使用优雅的衬线体（Serif），正文使用现代无衬线体（Sans-serif）。

配色：主色调为赤陶红 (# D67052) 和芥末黄 (# F0B857)，搭配深海军蓝作为点缀。避免使用霓虹色或纯黑色。

视觉元素：使用注重排版的网格布局，插图风格应为抽象的、有机的黑色手绘线条画，置于赤陶红纯色色块之上，部分关键信息使用卡片布局。

图表：扁平化、极简的柱状图，强调数据对比，去除多余边框。

文字和图像都由 Nano Banana Pro 生成，另外不要将PPT 变成一整张图，一页一张图。

文章内容为：[]
```

### 5. 人物拆解）
*by [@cheerselflin](https://x.com/cheerselflin)*

```
手绘风格的时尚概念分解图。

中心：一位时尚自信、略带性感（但并不露骨）的女性角色的全身像，姿态自然而充满活力。

周围：她的关键元素结构化布局：

• 服装层次——展示外套、内衣、紧身裤（蕾丝、薄纱材质）、塑身衣，并放大细节图案。

• 表情图——3-4种面部表情（中性、害羞、惊讶、专注）。

• 特写镜头——面料褶皱纹理、肌肤细节、手势。

• 生活方式及配饰——打开的手提包，内含日常用品：口红、香水、粉饼盒、护手霜、日记本、保健品。

• 材质标注——每件物品旁的手写风格注释（例如，“柔软蕾丝”、“哑光皮革”、“色号#520”）。

背景：柔和的米色或羊皮纸纹理，营造设计草图的氛围。

光线：干净柔和的阴影，使画面浑然一体。

输出：4K 高清 2D 插画，兼具性感与时尚感。

语言：中英文标签。
```

### 6. 儿童识字小报）
*by [@lxfater](https://x.com/lxfater)*

```
请生成一张儿童识字小报《游乐园》，竖版 A4，学习小报版式，适合 5–9 岁孩子 认字与看图识物。 一、小报标题区（顶部） 顶部居中大标题：《游乐园识字小报》 风格：十字小报 / 儿童学习报感 文本要求：大字、醒目、卡通手写体、彩色描边 装饰：周围添加与 游乐园 相关的贴纸风装饰，颜色鲜艳 二、小报主体（中间主画面） 画面中心是一幅 卡通插画风的「游乐园」场景： 整体气氛：明亮、温暖、积极 构图：物体边界清晰，方便对应文字，不要过于拥挤。 场景分区与核心内容 核心区域 A（主要对象）：表现 游乐园 的核心活动（孩子们在玩游乐设施）。 核心区域 B（配套设施）：展示相关的工具或物品（售票、零食、指示设施）。 核心区域 C（环境背景）：体现环境特征（入口、路牌、彩旗、绿地等）。 主题人物 角色：1 位可爱卡通人物（身份：游乐园工作人员/游客小朋友皆可）。 动作：正在进行与场景相关的自然互动（如微笑指路、挥手欢迎、陪孩子玩）。 三、必画物体与识字清单（Generated Content） 请务必在画面中清晰绘制以下物体，并为其预留贴标签的位置： 1. 核心角色与设施： gōng zuò rén yuán 工作人员 shòu piào chù 售票处 guò shān chē 过山车 mó tiān lún 摩天轮 xuán zhuǎn mǎ 旋转木马 2. 常见物品/工具： piào 票 qì qiú 气球 bīng jī líng 冰淇淋 bào mǐ huā 爆米花 táng hú lu 糖葫芦 miàn jù 面具 wán jù 玩具 xiǎo qí zi 小旗子 3. 环境与装饰： rù kǒu 入口 chū kǒu 出口 zhǐ shì pái 指示牌 cǎi qí 彩旗 guǎng chǎng 广场 (注意：画面中的物体数量不限于此，但以上列表必须作为重点描绘对象；总计 18 个典型名词，适合 5–9 岁儿童识字。) 四、识字标注规则 对上述清单中的物体，贴上中文识字标签： 格式：两行制（第一行拼音带声调，第二行简体汉字）。 样式：彩色小贴纸风格，白底黑字或深色字，清晰可读。 排版：标签靠近对应的物体，不遮挡主体。 五、画风参数 风格：儿童绘本风 + 识字小报风 色彩：高饱和、明快、温暖 (High Saturation, Warm Tone) 质量：8k resolution, high detail, vector illustration style, clean lines.
```

### 7. 为城市图片添加巨大生物）
*by [@AI_GIRL_DESIGN](https://x.com/AI_GIRL_DESIGN)*

```
使用上传的城市照片作为底图。请勿更改照片中的真实建筑、街道、车辆或人物。保持照片的真实性。在建筑物上方和后方的天空中添加一个非常巨大、风格化的插画生物，仿佛它俯瞰着整座城市。该生物应采用扁平化的图形风格绘制，轮廓清晰，并使用有限的霓虹色（例如柔和的霓虹绿、霓虹黄和柠檬绿），类似于壁画或海报插图。生物设计： - 奇幻的异想世界，而非恐怖或暴力 - 由层叠的形状、鳞片、毛发或花卉图案构成 - 长长的手臂或头发垂挂在建筑物旁 - 巨大的角或其他奇特的特征在天空的映衬下清晰可见 与照片的融合： - 将生物放置在建筑物边缘后方，使其部分身体出现在建筑物边缘之后，注意透视关系 - 使用正确的重叠方式：建筑物边缘在前，生物在后，使其融入场景之中 - 如有需要，可在附近的建筑物表面添加非常柔和的阴影或色彩反射，但要保持微妙 - 保持天空的原始亮度，使插图清晰突出 可选： - 在街道上添加一些小型、简单的插图人物（扁平、极简风格），例如遛狗或过马路，但不要遮挡真人。 整体氛围：梦幻般的超现实城市景象，一只巨大的、友好的插图生物出现在逼真的建筑物上方，将真实照片与简洁现代的插图相结合。
```

### 8. 玩具分解展示）
*by [@ZeroZ_JQ](https://x.com/ZeroZ_JQ)*

```
桌子上只有一个[阿童木]的玩具，玩具被对半分为左右两部分展示，玩具左半边是正常的玩具形象，右半边是透明的外壳，可以清晰的看到里面的内部构造，并有白色的线指出每一个部分是做什么的，在桌面上，明亮的背景，虚化的桌子。左边展示这个一半透明一半实体的玩具，画面的右边展示各类线条指出的参数指
```

### 9. 蓬松毛绒玩具）
*by [@toolfolio](https://x.com/toolfolio)*

```
将一个简单的扁平矢量标志转换成一个柔软蓬松的3D立体物体。使用原有颜色。该物体完全被毛发覆盖，拥有超逼真的毛发纹理和柔和的阴影。它位于干净的浅灰色背景中央，轻柔地漂浮在空中。风格超现实、触感丰富且现代，营造出舒适和趣味盎然的感觉。采用摄影棚灯光和高分辨率渲染。
```

### 10. 水晶质感emoji）
*by [@ZHO_ZHO_ZHO](https://x.com/ZHO_ZHO_ZHO)*

```
一幅照片级真实、细节高度丰富的图像，主体是 [一台 3D 拍立得相机]，以清澈、抛光度极高的透明玻璃或水晶材质渲染而成。[机身具有明显的厚度与立体深度，经典拍立得相机的标志性造型——方正机身、前置镜头、顶部取景器、正面拍照按钮以及底部吐片槽——全部以简化却极为精确的几何结构呈现，使其无需任何图案就能一眼辨认]。所有边缘采用圆润倒角与光滑曲面处理，在光线下产生优雅的折射效果。相机略微倾斜摆放，仿佛漂浮在洁净无暇、无缝衔接的淡米白或极浅灰色棚拍背景上方。

照明为明亮、干净的专业棚拍光，重点突出玻璃材质的透明性、镜面反射与折射特性。机身倒角、吐片槽边缘与镜头圆环处呈现锐利而细腻的高光，凸显晶莹质感与奢华视觉。光线穿透玻璃机身内部时产生微妙的折射、光线弯曲与局部失真效果，在镜头厚度变化区、吐片槽内部与顶部取景器附近尤为明显，极大增强了逼真感与视觉冲击力。相机下方与稍偏后方落下一片柔和、漫散的阴影，使画面具有落地感却不破坏极简气质。

整体美学风格极简、现代、干净，呈现高端产品摄影与概念艺术渲染的视觉效果。画面焦点完全聚焦于玻璃拍立得相机晶莹剔透的材质表现与经典几何造型。影像整体为高调光感与浅景深处理，使拍立得相机保持绝对清晰的焦点，而背景柔和虚化，从而最大程度突出主体。
```

### 11. 蓬松充气玩具）
*by [@gizakdag](https://x.com/gizakdag)*

```
将附件中的标志制作成一个高分辨率的3D渲染图，形状应为充气蓬松的物体。形状应呈现柔软饱满的效果，如同毛绒气球或充气玩具。使用光滑的哑光纹理，并添加细微的织物褶皱和缝线，以突出充气效果。物体应略带弹性，并辅以柔和的阴影和光线，以增强体积感和真实感。将其放置在简洁的背景（浅灰色）上。
```

### 12. 根据面部估算年龄）
*by [@Samann_ai](https://x.com/Samann_ai)*

```
根据（您的照片）制作一张超逼真、高分辨率的肖像信息图。保持（您的照片）中人物的身份、发型、服装和自然肤色不变，并使用中性摄影棚背景。在整张脸上叠加一个微妙的半透明面部分析网格，类似于3D面部扫描网格：纤细柔和的白色线条沿着面部轮廓延伸，略带光泽但不遮盖皮肤细节。在脸部一侧添加一条清晰的垂直红色激光线，如同未来主义的扫描效果。所有分析线都必须柔和、简洁、优雅，如同美容科技广告一般。制作一张简洁的医学美容信息图，使用全局数据百分比评估5个衰老因素：1. 细纹和皱纹；2. 皮肤纹理和弹性；3. 面部容量和下垂；4. 眼周衰老迹象；5.肤色和色素沉着：针对每个因素，放置一个带有细线指向相应面部区域的小标签，并在旁边写上简短的标题和一个0-100%的实际百分比分数（基于全球数据），例如：“细纹和皱纹 - 18%”“皮肤纹理和弹性 - 72%”“面部容量和下垂 - 35%”“眼周衰老迹象 - 41%”“肤色和色素沉着 - 63%”。使用简洁、现代的无衬线字体和小号技术风格文本，类似于科学的面部分析用户界面。在图像底部中央，用粗体大字显示基于分析的最终估计真实年龄，例如：“估计年龄：（基于面部分析的随机数字）”。整体风格：未来主义的AI引导护肤分析，极简主义，高级编辑灯光，不提及性别，适用于任何面部。
```

*Add yours via a PR — keep the original author's credit. See [Contributing](#contributing).*

---

## Related Model Guides
Part of the WaveSpeed **Awesome Model** series — one guide per frontier model, all runnable through one API:

- 🎬 [awesome-seedance-api](https://github.com/WaveSpeedAI/awesome-seedance-api) — ByteDance Seedance video
- 🌊 [awesome-wan-api](https://github.com/WaveSpeedAI/awesome-wan-api) — Alibaba Wan video
- ⚡ [awesome-minimax-h3-api](https://github.com/WaveSpeedAI/awesome-minimax-h3-api) — MiniMax Hailuo H3 video
- 🎞️ [awesome-kling-api](https://github.com/WaveSpeedAI/awesome-kling-api) — Kling video
- 🖼️ [awesome-seedream-api](https://github.com/WaveSpeedAI/awesome-seedream-api) — ByteDance Seedream image
- 🎨 [awesome-gpt-image-api](https://github.com/WaveSpeedAI/awesome-gpt-image-api) — OpenAI GPT Image
- 🍌 [awesome-nano-banana-api](https://github.com/WaveSpeedAI/awesome-nano-banana-api) — Google Nano Banana image *(this repo)*

---

## Contributing
PRs welcome:
1. Reusable prompts (`{placeholders}` for swappable parts).
2. **Credit the original author** with a link.
3. No output images unless you own and can license them.

## License
[CC0-1.0](LICENSE) — text & prompts are free to use. Model outputs follow the model provider's and [WaveSpeed](https://wavespeed.ai)'s terms.

---
<p align="center"><sub>Maintained by <a href="https://wavespeed.ai?utm_source=github&utm_medium=readme&utm_campaign=awesome-nano-banana-api">WaveSpeed AI</a> — the fastest way to run frontier image & video models via one API. <a href="https://wavespeed.ai/nano-banana-2-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-nano-banana-api"><b>Run Nano Banana →</b></a></sub></p>
