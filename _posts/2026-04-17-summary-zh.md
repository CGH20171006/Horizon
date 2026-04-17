---
layout: default
title: "Horizon Summary: 2026-04-17 (ZH)"
date: 2026-04-17
lang: zh
---

> From 71 items, 29 important content pieces were selected

---

1. [Claude Opus 4.7 引入自适应思考](#item-1) ⭐️ 9.0/10
2. [OpenAI 将 Codex 扩展为电脑操作智能体](#item-2) ⭐️ 8.0/10
3. [Qwen 开源 Qwen3.6-35B-A3B 编程模型](#item-3) ⭐️ 8.0/10
4. [Cloudflare 推出面向智能体的 AI 推理层](#item-4) ⭐️ 8.0/10
5. [AI 战争中的人工控制正在失效](#item-5) ⭐️ 8.0/10
6. [微软暂停冲击碳移除市场](#item-6) ⭐️ 8.0/10
7. [Telegram 工具助骗子绕过银行核验](#item-7) ⭐️ 8.0/10
8. [镜像细菌引发生物安全担忧](#item-8) ⭐️ 8.0/10
9. [战争挤压海湾主权财富](#item-9) ⭐️ 8.0/10
10. [阿里腾讯发布 3D 世界模型](#item-10) ⭐️ 8.0/10
11. [DeepGEMM 新增 Mega MoE 与 FP4 支持](#item-11) ⭐️ 8.0/10
12. [Anthropic 发布 Claude Opus 4.6](#item-12) ⭐️ 8.0/10
13. [星链故障中断美海军无人艇测试](#item-13) ⭐️ 8.0/10
14. [猎鹰重型将于 2028 年发射 ESA 火星车](#item-14) ⭐️ 8.0/10
15. [Google 推出面向智能代理的 Android CLI](#item-15) ⭐️ 7.0/10
16. [Aphyr 警告 LLM 引发信任崩塌](#item-16) ⭐️ 7.0/10
17. [加州诉讼聚焦亚马逊价格施压](#item-17) ⭐️ 7.0/10
18. [Google 预览 Gemini 3.1 Flash TTS](#item-18) ⭐️ 7.0/10
19. [企业 AI 的护城河在操作层](#item-19) ⭐️ 7.0/10
20. [全球失衡卷土重来](#item-20) ⭐️ 7.0/10
21. [巴基斯坦外交缓压却拖延改革](#item-21) ⭐️ 7.0/10
22. [古老微生物防御塑造人类免疫](#item-22) ⭐️ 7.0/10
23. [宇宙尘埃或可解释金星下层霾](#item-23) ⭐️ 7.0/10
24. [衰老或按性别重塑疾病风险](#item-24) ⭐️ 7.0/10
25. [创纪录数量研究人员竞选美国公职](#item-25) ⭐️ 7.0/10
26. [脑细胞性别相关基因活性图谱揭示](#item-26) ⭐️ 7.0/10
27. [DeepL 推出实时语音翻译](#item-27) ⭐️ 7.0/10
28. [360 智能体发现两项高危漏洞](#item-28) ⭐️ 7.0/10
29. [科研削资与 AI 科学家零工化](#item-29) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [Claude Opus 4.7 引入自适应思考](https://www.anthropic.com/news/claude-opus-4-7) ⭐️ 9.0/10

Anthropic 发布了 Claude Opus 4.7，这一新版 Opus 引入了自适应思考机制，并调整了与推理输出相关的开发者默认行为。该版本也引发了开发者反馈，称其在一些场景下会消耗更多 token、生成更长的计划，并在部分网络安全相关工作流中出现更严格的拒答。 这很重要，因为 Opus 被用于生产环境应用，推理控制、输出格式和 token 消耗的变化会直接影响成本、延迟和集成稳定性。这也反映了前沿模型的更广泛趋势：更自动化地分配推理资源，并收紧安全护栏，这对某些用例可能提升可靠性，但也会让另一些用户感到受限。 根据 Claude API 文档，Opus 4.7 通过 thinking: { type: "adaptive" } 支持自适应思考，由模型自行决定何时需要额外推理，而不是像旧模型那样依赖固定的 budget_tokens 设置。文档还说明，从 Opus 4.7 开始，如果将 temperature、top_p 或 top_k 设为非默认值会返回 400 错误，因此推荐的迁移方式是直接省略这些参数。

hackernews · meetpateltech · Apr 16, 14:23

**背景**: 在 Claude 的 API 中，“thinking” 指的是模型在生成答案前分配内部推理资源的行为。较早的 Claude 模型需要开发者显式开启 thinking 并设置 token 预算，而自适应思考则允许模型根据请求自行决定是否使用以及使用多少额外推理。token 使用量之所以重要，是因为 LLM 以 token 为单位处理输入和输出，更高的 token 数通常意味着更高的成本，有时也会带来更长的响应或更高的延迟。Anthropic 一直强调 AI 安全，因此在敏感任务上更严格的拒答也符合其整体产品方向。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://platform.claude.com/docs/en/build-with-claude/adaptive-thinking">Adaptive thinking - Claude API Docs</a></li>
<li><a href="https://platform.claude.com/docs/en/about-claude/models/whats-new-claude-4-7">What's new in Claude Opus 4.7 - Claude API Docs</a></li>
<li><a href="https://www.ibm.com/think/topics/context-window">What is a context window? | IBM</a></li>

</ul>
</details>

**社区讨论**: 社区反应褒贬不一，而且非常偏重实际使用体验。一些开发者对从显式思考预算转向自适应思考感到困惑，也指出现在默认不会输出人类可读的推理摘要，除非显式请求 display: "summarized"；另一些人则认为它与之前版本差异不大，只是消耗了更多 token。另一类批评集中在更严格的网络安全拒答上，有评论者表示这些安全过滤已经影响到合法的防御性研究，同时也有人认为 Anthropic 没有把这些取舍解释得足够清楚。

**标签**: `#AI`, `#LLMs`, `#Anthropic`, `#API`, `#Model Release`

---

<a id="item-2"></a>
## [OpenAI 将 Codex 扩展为电脑操作智能体](https://openai.com/index/codex-for-almost-everything/) ⭐️ 8.0/10

OpenAI 宣布对 Codex 进行重大扩展，使其从以编程为主的工具转向更广泛的 AI 智能体工作流，可处理通用电脑操作和知识型工作任务。根据提供的摘要和讨论，这次更新的重点是更直接地操作软件，并支持持续时间更长、自治程度更高的任务执行。 这很重要，因为它把 Codex 从开发者辅助工具推进到更庞大的通用知识工作者市场，在那里 AI 智能体有望自动化大量重复性的桌面与流程任务。这也表明围绕电脑操作智能体的竞争正在加剧，OpenAI 正在让 Codex 对标类似产品，并顺应能够跨软件工具进行感知、推理和执行的 AI 系统这一更大趋势。 已提供的信息显示，新能力包括通过视觉与电脑交互、在应用中点击和输入、后台运行、在 Mac 上并行运行多个智能体、内置浏览器、图像生成、SSH 访问以及多终端标签页。不过，这里给出的官方技术细节仍然有限，因此此次公告更清楚地展示了产品方向和工作流目标，而不是底层架构、基准测试或可靠性边界。

hackernews · mikeevans · Apr 16, 17:12

**背景**: Codex 是 OpenAI 的一类 AI 编程工具与智能体，最初主要用于把自然语言转化为代码，并协助软件开发。OpenAI 近期围绕 Codex 的表述，越来越强调“AI 开发者队友”的模式，也就是让系统能在配置好的环境中执行多步骤任务。更大的行业背景是面向电脑操作和知识工作的 AI 智能体正在兴起，这类模型不再只是回答问题，而是被期待能够操作软件、调用工具，并在有限监督下完成完整工作流。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/introducing-codex/">Introducing Codex | OpenAI</a></li>
<li><a href="https://en.wikipedia.org/wiki/OpenAI_Codex">OpenAI Codex - Wikipedia</a></li>
<li><a href="https://www.v7labs.com/blog/rise-of-work-ai">The Rise of Work AI: Will Knowledge Work Be Fully Automated?</a></li>

</ul>
</details>

**社区讨论**: 社区讨论非常热烈，但观点不一：一些评论者认为，这可能会成为面向非技术知识工作者的最重要软件品类之一；另一些人则怀疑 OpenAI 并没有真正开创新东西。一个反复出现的话题是，提示词驱动界面在隐藏代码的同时，是否牺牲了技术用户需要的透明度；此外，也有不少人将其与 Claude Desktop 和 Cowork 等产品比较，认为类似能力其实已经存在。

**标签**: `#AI agents`, `#OpenAI`, `#developer tools`, `#knowledge work automation`, `#Hacker News`

---

<a id="item-3"></a>
## [Qwen 开源 Qwen3.6-35B-A3B 编程模型](https://qwen.ai/blog?id=qwen3.6-35b-a3b) ⭐️ 8.0/10

Qwen 发布了 Qwen3.6-35B-A3B，这是一款开放权重的代理式编程模型，采用稀疏 MoE 架构，总参数为 35B、激活参数约为 3B。根据发布摘要，它在 SWE-bench、Terminal-Bench 和 MCPMark 等编程与工具使用基准上优于前代，同时提供可自托管的权重，并兼容 OpenAI 与 Anthropic 风格的 API 工作流。 这很重要，因为它把较强的编码代理能力带到了可本地部署、可企业内网部署的开放权重模型上，对无法依赖公有云托管模型的受监管行业尤其有吸引力。这也进一步说明，较小激活参数的 MoE 系统可以在不承担超大稠密模型推理成本的情况下，提供有竞争力的实际表现。 “A3B” 这一命名表示模型总参数为 35B，但每个 token 仅激活约 3B 参数，这也解释了社区为何关注它在本地硬件上的运行可行性。Hugging Face 页面还给出了通过 vLLM 或 SGLang 提供 OpenAI 兼容服务的配置示例，并包含工具配置与 thinking 模式选项，便于接入现有的编码代理系统。

hackernews · cmitsakis · Apr 16, 13:36

**背景**: 代理式编程模型是一类不仅能生成代码片段，还能为多步骤任务做规划，并在处理软件问题时与终端、文件系统或 MCP 服务器等外部工具交互的 LLM。“开放权重”表示训练后的模型权重可以下载和运行，但这并不等同于完全开源的 AI；后者通常还应包含更多训练数据、训练代码以及可复现性细节。稀疏 MoE 模型会让每个 token 只经过网络中的一部分模块，因此能在保持较大总参数规模的同时，降低推理时使用的计算量。对于自托管的编码助手来说，这种权衡尤为重要，因为延迟、硬件限制和隐私要求都会直接影响部署选择。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/Qwen/Qwen3.6-35B-A3B">Qwen/Qwen3.6-35B-A3B · Hugging Face</a></li>
<li><a href="https://simonwillison.net/guides/agentic-engineering-patterns/how-coding-agents-work/">How coding agents work - Agentic Engineering Patterns - Simon Willison's Weblog</a></li>
<li><a href="https://opensource.org/ai/open-weights">Open Weights: not quite what you’ve been told - Open Source Initiative</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论整体非常积极，许多评论都聚焦于实际部署层面：用户很快分享了 GGUF 量化版本、本地笔记本运行体验，以及与 LM Studio 的兼容性。反复出现的观点是，开放权重的编程模型对银行、医疗等受限环境具有战略价值；也有人表示欣慰，认为 Qwen 仍在持续发布开放权重模型，并讨论它与领先闭源模型相比的表现。

**标签**: `#AI models`, `#open weights`, `#coding assistants`, `#LLMs`, `#Hacker News`

---

<a id="item-4"></a>
## [Cloudflare 推出面向智能体的 AI 推理层](https://blog.cloudflare.com/ai-platform/) ⭐️ 8.0/10

Cloudflare 推出了一个 AI 平台，将 AI Gateway 升级为其网络上面向智能体和 AI 应用的统一推理层。根据 Cloudflare 的公告，开发者可以通过一个接口访问来自 14 家以上提供商的模型，并结合 Workers AI 集成以及扩展后的多模态模型目录来使用。 这件事之所以重要，是因为它把模型访问、路由以及配套应用基础设施整合进了一个由大型互联网边缘平台提供的开发者平台。对于构建智能体的团队来说，这可能降低集成复杂度，同时提供更简单的故障切换、统一计费以及依托 Cloudflare 网络的更低延迟部署能力。 Cloudflare 将该产品描述为一个围绕 AI Gateway 构建的统一推理层，而相关资料强调可通过单一 API 和统一计费入口访问来自 12 家以上提供商的 70 多个模型。此次发布也把该平台与 Cloudflare 更广泛的技术栈连接起来，包括 Workers AI；后者可在 Cloudflare 网络上提供无服务器推理，而不需要用户直接管理 GPU 基础设施。

hackernews · nikitoci · Apr 16, 13:17

**背景**: 在 AI 应用开发中，推理层是负责向模型发送请求、处理不同提供商差异，并通常提供路由、可观测性和故障切换等能力的那一层。对于智能体来说，这一点尤为重要，因为它们往往会发起多次串联的模型调用，并需要对不同类型模型进行可靠且低延迟的访问。Cloudflare 此前已经提供了 Workers AI 这一在其网络上运行推理的服务，而这个新平台则表明 Cloudflare 正把自己定位为更广泛的模型访问协调层，而不只是单个模型的托管方。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.cloudflare.com/ai-platform/">Cloudflare’s AI Platform: an inference layer designed for agents</a></li>
<li><a href="https://www.cloudflare.com/developer-platform/products/workers-ai/">Cloudflare Workers AI | Open-source AI inference</a></li>
<li><a href="https://developers.cloudflare.com/workers-ai/">Overview · Cloudflare Workers AI docs</a></li>

</ul>
</details>

**社区讨论**: 社区讨论总体偏积极，但也相当务实：一些读者认为这更像是把 OpenRouter 与 Cloudflare 网络能力结合起来，另一些人则觉得这种集成式工具链确实很有价值。评论者也提出了一些尚未解决的问题，包括平台对自定义模型或 LoRA 的可扩展部署支持是否足够、Cloudflare 不同模型目录之间差异令人困惑，以及 Cloudflare 未来是否会进一步解决比推理更难的智能体治理层问题。

**标签**: `#AI infrastructure`, `#Cloudflare`, `#agents`, `#model inference`, `#developer platforms`

---

<a id="item-5"></a>
## [AI 战争中的人工控制正在失效](https://www.technologyreview.com/2026/04/16/1136029/humans-in-the-loop-ai-war-illusion/) ⭐️ 8.0/10

MIT Technology Review 认为，随着军事 AI 从情报辅助转向作战决策，所谓让人类在 AI 战争中“保持在回路中”的设想正变得越来越不现实。文章将这一变化与 Anthropic 和 Pentagon 之间正在进行的法律争议，以及 AI 在当前伊朗冲突中不断扩大的作用联系起来。 这很重要，因为许多 AI 治理和武器政策框架都把人工监督当作防止误用武力、违法攻击或冲突升级的核心安全机制。如果人类无法在机器速度的战场决策中真正完成审查或控制，那么当前关于问责、合法性和威慑的许多政策前提都可能比决策者宣称的更脆弱。 在武器讨论中，“human in the loop”传统上指的是由人类批准或发起致命行动，而“human on the loop”等相关模式则更接近监督而非直接控制。文章的核心观点是，一旦 AI 系统被嵌入作战层面的军事决策支持流程，决策速度、复杂性和数量就可能让名义上的人工批准沦为程序性步骤，而不再是真正有意义的审慎判断。

rss · MIT Technology Review · Apr 16, 12:00

**背景**: “Human in the loop” 是 AI 和武器政策中的一个长期术语，在军事语境下通常指必须由人类操作员授权使用武力的系统。分析人士和国防研究者近年来越来越多地讨论 AI 不只是情报分析工具，也可以用于支持作战层面的军事决策，而这一层级位于战术执行与高层战略之间。近期报道还提到 Anthropic 与美国国防部在 2026 年围绕 AI 军事用途发生法律冲突，这表明国防 AI 的治理已经从假设性讨论变成现实的制度与法律问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Human-in-the-loop">Human - in - the - loop - Wikipedia</a></li>
<li><a href="https://www.rand.org/pubs/research_reports/RRA815-1.html">Machine Learning for Operational Decisionmaking in... | RAND</a></li>
<li><a href="https://techxplore.com/news/2026-04-court-anthropic-legal-department-war.html">US court expedites Anthropic's legal battle with Department ...</a></li>

</ul>
</details>

**标签**: `#AI policy`, `#autonomous weapons`, `#military technology`, `#geopolitics`, `#AI ethics`

---

<a id="item-6"></a>
## [微软暂停冲击碳移除市场](https://www.technologyreview.com/2026/04/16/1135928/carbon-removal-microsoft/) ⭐️ 8.0/10

有报道称微软可能暂停购买碳移除额度，这引发了行业警报，因为据报道该公司约占所有已签约碳移除需求的 80%。《MIT Technology Review》认为，这可能会对一个高度依赖单一大买家来支持项目融资的早期市场造成冲击。 如果最大的购买方后撤，碳移除项目开发商可能会面临资金缺口、价格支撑减弱以及部署放缓的问题。这不仅关系到气候科技初创公司，也关系到更广泛的自愿碳市场，因为长期企业承购协议能够让昂贵的碳移除技术更容易获得融资。 这一担忧对工程化碳移除尤其严重，这类方法包括 direct air capture，通常比传统碳信用更昂贵。在这类市场中，多年期承购协议非常重要，因为它们能降低供应方和投资者的不确定性；因此，主导买家的暂停行为可能会传导到定价和项目开发层面。

rss · MIT Technology Review · Apr 16, 10:00

**背景**: 碳移除是指将二氧化碳从大气中移出，并进行具有实际意义时长的储存。它既包括基于自然的方法，也包括工程化方法；后者可包括 direct air capture，即利用工业系统直接从环境空气中提取 CO2。由于许多工程化碳移除方案仍然成本高且处于早期阶段，买方通常会通过长期采购协议帮助项目获得融资并扩大产能。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cleanenergywire.org/factsheets/qa-dac">Q&A: Direct air capture - Hype or hope for... | Clean Energy Wire</a></li>
<li><a href="https://www.sentinelearth.com/post/nature-based-vs-engineered-carbon-removals">Nature-Based vs Engineered Carbon Removals: What Is The ...</a></li>
<li><a href="https://www.msci.com/research-and-insights/blog-post/nature-based-offtake-deals-something-is-stirring-in-voluntary-carbon-markets">Nature-Based Offtake Deals: Something Is Stirring in ... - MSCI</a></li>

</ul>
</details>

**标签**: `#carbon removal`, `#climate tech`, `#Microsoft`, `#carbon markets`, `#industry trends`

---

<a id="item-7"></a>
## [Telegram 工具助骗子绕过银行核验](https://www.technologyreview.com/2026/04/15/1135898/cyberscammers-bypassing-bank-telegram/) ⭐️ 8.0/10

一篇调查报道披露，柬埔寨的诈骗园区正在使用通过 Telegram 出售的非法工具，绕过手机银行应用中的照片比对和视频活体检测。报道称，这些工具让有组织的诈骗网络能够大规模突破生物识别和身份核验环节，从而实施账户接管和欺诈转账。 这很重要，因为银行越来越依赖远程 KYC、自拍核验和活体检测作为数字金融的一线防线，而一旦出现可重复使用的绕过方法，就会削弱这层核心安全保障。该威胁同时影响消费者和金融机构，会增加欺诈损失、削弱用户对应用开户和账户恢复流程的信任，并显示 Telegram 如何充当网络犯罪基础设施。 活体检测的目标是确认现场存在的是真人，而不是照片、回放视频或合成媒体，但行业指南和安全研究都指出，如果缺少更强的反欺骗机制，基础活体检查可能被绕过。更广泛地说，KYC 合规与身份核验彼此相关但并不相同：通过类似开户的证件检查，并不一定能证明当前会话的操作者是合法、在场且已获授权的用户。

rss · MIT Technology Review · Apr 15, 11:26

**背景**: KYC，即“了解你的客户”，是金融机构在开户或维持账户关系时，为满足监管要求而进行的身份与风险审查。在手机银行和金融科技应用中，这通常包括远程身份核验步骤，例如证件拍摄、自拍比对和活体检测，用来区分真人与伪造输入。厂商通常将被动活体描述为分析深度、动作或其他细微生物特征信号，但安全研究人员和反欺诈公司已警告，犯罪分子正越来越多地把社会工程、合成媒体和自动化工具结合起来攻击这些流程。Telegram 也在其他欺诈和钓鱼生态中出现，常被用作工具包分发、团伙协同和数据回传的渠道。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Know_your_customer">Know your customer - Wikipedia</a></li>
<li><a href="https://www.jumio.com/deepfake-detection-guide/">Advanced Deepfake Detection : Essential Guide from Jumio</a></li>
<li><a href="https://blog.knowbe4.com/telekopye-phishing-toolkit-telegram-bots-scammers">New Telekopye Phishing Toolkit Uses Telegram-Based Bots To ...</a></li>

</ul>
</details>

**标签**: `#cybersecurity`, `#financial-fraud`, `#banking`, `#telegram`, `#digital-identity`

---

<a id="item-8"></a>
## [镜像细菌引发生物安全担忧](https://www.technologyreview.com/2026/04/15/1135197/synthetic-mirror-life-microbes-kill-us-all/) ⭐️ 8.0/10

MIT Technology Review 报道了围绕合成“镜像”细菌这一设想不断升温的科学与政策审视，这一概念曾在 2019 年一次由 NSF 相关头脑风暴会议上被合成生物学家和伦理学家讨论。文章关注的不是新的实验突破，而是在潜在风险极端巨大的情况下，这类反手性微生物是否根本就不应被研发。 这之所以重要，是因为镜像生命可能构成一种性质全新的生物安全威胁：由相反手性生物分子构成的自我复制生物体，可能逃避免疫防御和生态捕食。这个争论也在检验合成生物学界应如何在技术能力真正成熟之前，先行治理高风险研究。 镜像细菌是假想中的细胞，其组成材料是现有生命常用构件的对映异构版本，例如采用相反方向的生物分子手性。检索结果显示，这类生物目前并不存在，但专家警告说，它们未来若被制造出来，可能在生态系统中扩散、利用非手性营养物，并且让现有免疫系统或微生物捕食者难以识别。

rss · MIT Technology Review · Apr 15, 09:00

**背景**: 生物手性指的是许多分子存在两种互为镜像且无法重合的形式，就像左手和右手。已知生命在核心化学组成上几乎都只使用其中一种“手性”，例如蛋白质和核酸，因此一个完整的“镜像”生物将与天然生物有根本差异。根据 ASM 等资料，镜像细菌目前仍停留在假想阶段，但人们的担忧正在增加，因为能够复制的镜像微生物可能不受限制普通微生物的那些生物相互作用所约束。因此，这一议题同时关联生命起源研究与现代生物安全政策。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://asm.org/articles/2025/may/mirror-bacteria-reflecting-alternate-chirality">Mirror Bacteria: Reflecting on Alternate Chirality - asm.org</a></li>
<li><a href="https://en.wikipedia.org/wiki/Mirror-image_life">Mirror-image life - Wikipedia</a></li>
<li><a href="https://medicine.yale.edu/news-article/qanda-how-mirror-bacteria-could-take-a-devastating-toll-on-humanity/">Q&A: How ‘Mirror Bacteria’ Could Take a Devastating Toll on ... Mirror life | Definition, Dangers, & Facts | Britannica Life’s evil twins—mirror cells—could doom Earth if scientists ... Scientists Weigh the Risks of ‘Mirror Life,’ Synthetic ... Mirror Microbes: Understanding the How and Why of ...</a></li>

</ul>
</details>

**标签**: `#synthetic biology`, `#biosecurity`, `#ethics`, `#science policy`, `#emerging technology`

---

<a id="item-9"></a>
## [战争挤压海湾主权财富](https://www.economist.com/finance-and-economics/2026/04/15/war-will-drain-the-gulfs-6trn-treasure-chest) ⭐️ 8.0/10

《经济学人》指出，中东战争正使海湾国家更难管理和动用大约 6 万亿美元的石油衍生金融储备。冲突让这些资产的管理者在国内支出、保持流动性以及对外投资之间的取舍变得更加复杂。 这些基金是全球金融中的重要参与者，因此它们行为的变化会影响中东以外的资本流动、资产价格和投资活动。对海湾国家自身而言，这同样重要，因为战争会推高财政支出需求、扰乱能源市场，并考验依赖石油收入的发展模式是否可持续。 问题的核心是由石油收入积累而成的主权财富基金及其他国家资本池，它们必须在长期投资目标与短期地缘政治、财政压力之间取得平衡。需要注意的是，这更像是一篇分析性判断，而不是一次单独的政策发布，因此其意义主要在于海湾资本配置所处风险环境正在变化。

rss · The Economist Finance · Apr 15, 13:37

**背景**: 主权财富基金是由国家拥有的投资工具，用于管理国家财富，资金通常来自石油等自然资源收入。在海湾地区，这类基金已经成为把多余能源收入投向全球股票、债券、基础设施和私募市场的重要机制。这与“石油美元回流”密切相关，也就是把石油出口收入重新投入国际金融资产，而不是立即在国内花掉。当地缘冲突加剧不确定性时，政府往往更倾向于保留更多现金、支持国内财政，或调整投资组合风险，而这会向全球市场传导影响。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://101blockchains.com/sovereign-wealth-fund-explained/">Know everything about Sovereign Wealth Fund - 101 Blockchains</a></li>
<li><a href="https://en.wikipedia.org/wiki/Petrodollar_recycling">Petrodollar recycling - Wikipedia</a></li>
<li><a href="https://www.investopedia.com/terms/p/petrodollars.asp">Understanding Petrodollars: Definition, History, and Global Impact - Investopedia</a></li>

</ul>
</details>

**标签**: `#geopolitics`, `#sovereign-wealth-funds`, `#middle-east`, `#energy-markets`, `#global-finance`

---

<a id="item-10"></a>
## [阿里腾讯发布 3D 世界模型](https://www.bloomberg.com/news/articles/2026-04-16/alibaba-releases-new-ai-model-for-gaming-development) ⭐️ 8.0/10

阿里巴巴发布了 Happy Oyster，这是一款面向游戏开发以及影视制作的可交互 3D 视频生成模型。腾讯则在同日发布并开源混元 3D 世界模型 2.0，支持基于文本、图片和视频生成、重建与模拟 3D 世界。 两家公司在同一天发布相关产品，说明中国大型互联网公司正从图像和视频生成进一步推进到完整的 3D 世界生成，这对游戏、数字孪生和内容制作流程都有直接价值。腾讯支持将资产导入 Unity 和 UE，也让这次发布对现有开发工作流具有更强的落地意义。 腾讯表示，该模型可导出 Mesh、点云和 3DGS 等资产格式，为后续编辑与渲染提供多种 3D 表达方式。3DGS 即 3D Gaussian Splatting，是一种面向实时辐射场渲染的技术，擅长基于照片或视频生成高质量的新视角画面，但这则消息并未披露基准测试、成本或画质对比数据。

telegram · zaihuapd · Apr 16, 07:58

**背景**: 这里所说的“世界模型”，指的不只是生成静态图像的 AI 系统，而是能够在结构化的 3D 环境中表示场景、物体和交互，并进一步进行模拟或编辑的能力。这对游戏开发很重要，因为开发者通常需要可复用的资产和场景表示，而不只是平面的媒体输出。数字孪生是对真实空间或系统的虚拟映射，因此从真实视频或多视角图片重建 3D 场景，可用于仿真、可视化和业务流程。支持 Mesh、点云和 3DGS 等格式也很关键，因为不同引擎和制作流程依赖的 3D 表达方式并不相同。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Gaussian_splatting">Gaussian splatting - Wikipedia</a></li>
<li><a href="https://cloud.tencent.com/developer/article/2655496">“世界模型”到底是个啥？OpenWorldLib一锤定音：感知+交互+记忆，这才...</a></li>
<li><a href="https://pdf.dfcfw.com/pdf/H3_AP202011231431940763_1.pdf?1606214310000.pdf">中国电子技术标准化研究院-2020版 数 字 孪 生 应用白皮书-201120.pdf</a></li>

</ul>
</details>

**标签**: `#AI`, `#3D Generation`, `#Game Development`, `#Multimodal Models`, `#China Tech`

---

<a id="item-11"></a>
## [DeepGEMM 新增 Mega MoE 与 FP4 支持](https://github.com/deepseek-ai/DeepGEMM/tree/public-release-260416) ⭐️ 8.0/10

2026 年 4 月 16 日，DeepSeek 发布了 DeepGEMM 的重大更新，新增了 Mega MoE 融合算子、FP8xFP4 GEMM 内核、FP4 Indexer、PDL 支持，以及更快的 JIT 编译。新的 Mega MoE 路径旨在让 dispatch、SwiGLU 和 NVLink 通信重叠执行，从而提升 NVIDIA SM90 和 SM100 GPU 上大模型训练与推理的效率。 这很重要，因为 MoE 系统和低精度内核是现代大模型高效扩展的关键，而更好的计算与通信重叠可以直接提升吞吐量和硬件利用率。对 FP4 相关内核的支持也表明，业界正在继续推动在新一代 NVIDIA 架构上使用更激进的低精度方案来提升训练和推理效率。 DeepGEMM 是一个运行时 JIT 的 CUDA 内核库，而不是依赖复杂预编译流程的重量级构建系统，并且面向包括 SM90 和 SM100 在内的现代 NVIDIA 架构。网页资料还表明，基于 DeepGEMM 的融合 MoE 路径已经集成到 vLLM 等项目中，而 NVIDIA 的 PDL 特性正是为了让同一 stream 中存在依赖关系的内核实现重叠执行。

telegram · zaihuapd · Apr 16, 09:57

**背景**: DeepGEMM 是一个面向大模型核心计算原语的 CUDA 内核库，重点覆盖 GEMM 和融合 MoE 执行等能力。在 mixture-of-experts 模型中，token 会被路由到不同专家，因此性能不仅取决于矩阵乘法本身，还高度依赖 dispatch、同步以及多 GPU 通信效率。PDL 也就是 Programmatic Dependent Launch，是较新 NVIDIA GPU 上的 CUDA 特性，允许同一 stream 中存在依赖关系的内核在前序内核完全结束前开始重叠执行。vLLM 文档也展示了基于 DeepGEMM 的融合 MoE 实现，这说明这些内核的价值并不局限于 DeepSeek 自身技术栈。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.vllm.ai/en/latest/api/vllm/model_executor/layers/fused_moe/experts/deep_gemm_moe/">deep _ gemm _ moe - vLLM</a></li>
<li><a href="https://docs.nvidia.com/cuda/cuda-programming-guide/04-special-topics/programmatic-dependent-launch.html">4.5. Programmatic Dependent Launch and Synchronization — CUDA ...</a></li>
<li><a href="https://deepwiki.com/deepseek-ai/DeepGEMM">deepseek-ai/DeepGEMM | DeepWiki</a></li>

</ul>
</details>

**标签**: `#AI infrastructure`, `#MoE`, `#GPU kernels`, `#Low-precision inference`, `#DeepSeek`

---

<a id="item-12"></a>
## [Anthropic 发布 Claude Opus 4.6](https://t.me/zaihuapd/40903) ⭐️ 8.0/10

Anthropic 发布了 Claude Opus 4.6，提供 200K token 上下文窗口、测试版最高 100 万 token 支持，并将最大输出长度从上一代的 64K token 提升到 128K token。新版本还加入了可按任务复杂度动态调整推理深度的自适应思考模式，以及在对话接近窗口上限时自动总结早期内容的上下文压缩功能。 这很重要，因为上下文窗口大小和输出上限会直接影响开发者能在单次会话中保留多少信息，以及模型一次能返回多长的结果。如果此次宣布的自适应推理和上下文压缩在实际使用中效果稳定，它们就有望降低长时对话助手、编程工具和企业工作流中的提示词管理成本，并增强 Anthropic 在前沿模型市场中的竞争力。 上下文窗口指模型一次能够处理的 token 总量，而最大输出上限限制的是单次回复可生成的文本长度，因此此次提升到 128K 输出是区别于 200K 上下文窗口的另一项重要变化。上下文压缩可以延长可用对话长度，但由于它依赖对早期内容进行总结，通常会在细节保真度与 token 限额之间进行权衡。

telegram · zaihuapd · Apr 16, 14:28

**背景**: 在大语言模型中，token 是文本处理的基本单位，而上下文窗口决定了模型在生成答案时能够同时考虑多少 token。更大的上下文窗口对于长文档处理、多步骤编程任务和长时间聊天尤其有用，但也会提高计算和内存开销。上下文压缩是指在减少 token 使用量的同时尽量保留早期内容中关键信息的技术，从而帮助模型在不超出限制的情况下继续更长的对话。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.geeksforgeeks.org/artificial-intelligence/tokens-and-context-windows-in-llms/">Tokens and Context Windows in LLMs - GeeksforGeeks</a></li>
<li><a href="https://www.morphllm.com/context-compression">Context Compression for LLMs: 7 Methods Compared with ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Large_language_model">Large language model - Wikipedia</a></li>

</ul>
</details>

**标签**: `#AI`, `#LLM`, `#Anthropic`, `#Model Release`, `#Context Window`

---

<a id="item-13"></a>
## [星链故障中断美海军无人艇测试](https://www.reuters.com/business/media-telecom/starlink-outage-hit-drone-tests-exposing-pentagons-growing-reliance-spacex-2026-04-16/) ⭐️ 8.0/10

Reuters 报道称，内部文件显示，Starlink 在 2025 年的多次故障曾中断美国海军无人水面艇测试。2025 年 8 月一次全球性断网期间，加州海岸外的 24 艘无人艇失去通信并滞留近一小时，而同年 4 月的测试还暴露出其在多设备高负载场景下的连接瓶颈。 这一事件凸显出五角大楼在无人系统和导弹追踪等任务的作战通信上，已对 SpaceX 形成较深依赖。如果商业网络故障能够直接打断军事行动，那么它就可能成为国家安全基础设施中的单点故障。 Starlink 依靠低地球轨道卫星的大规模部署获得了成本和覆盖优势，但 LEO 卫星互联网系统仍要依赖星座切换和地面网络链路，这些环节都可能形成瓶颈。对于在超视距条件下运行的无人水面艇而言，稳定的指挥控制通信是任务关键，因此即使是短时间中断也会导致测试停止并带来作战风险。

telegram · zaihuapd · Apr 17, 04:19

**背景**: 卫星互联网星座是由大量卫星组成的网络，通常部署在低地球轨道，以提供比传统高轨系统更低时延、更高带宽的连接能力。这类系统依赖卫星、地面网关和网络切换之间的协同，因此在高负载下保持可靠性是重要的工程挑战。执行超视距任务的无人水面艇需要持续的指挥控制链路，才能接收指令并回传遥测或视频等数据。这也是为什么在军事自主系统中，通信韧性与带宽本身同样重要。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Satellite_internet_constellation">Satellite internet constellation - Wikipedia</a></li>
<li><a href="https://comtech.com/blog-post/2025/05/07/pushing-distributed-maritime-operations-beyond-the-current-scope/">Pushing Distributed Maritime Operations Beyond the Current ...</a></li>
<li><a href="https://report.az/en/other-countries/reuters-pentagon-finds-critical-dependency-on-spacex-satellite-network">Reuters: Pentagon finds critical dependency on SpaceX ...</a></li>

</ul>
</details>

**标签**: `#Starlink`, `#Defense Technology`, `#Space Infrastructure`, `#National Security`, `#Pentagon`

---

<a id="item-14"></a>
## [猎鹰重型将于 2028 年发射 ESA 火星车](https://arstechnica.com/space/2026/04/after-a-saga-of-broken-promises-a-european-rover-finally-has-a-ride-to-mars/) ⭐️ 8.0/10

NASA 已选定 SpaceX 的 Falcon Heavy，于 2028 年底从肯尼迪航天中心发射 ESA 的 Rosalind Franklin 火星车。NASA 还将提供该任务所需的关键硬件，包括着陆平台减速发动机、放射性同位素加热装置，以及火星有机分子分析仪相关组件。 这为这辆经历多年延期和任务重构的欧洲火星车提供了明确的发射路径，使原本脆弱的计划变成了可执行的国际任务。它也强化了 NASA 与 ESA 在行星探测上的合作，并让一项重要的生命探测火星车任务得以在本十年继续推进。 该火星车计划前往 Oxia Planum，并使用可钻探至火星表面下约 2 米的钻头，这比此前火星有机物搜索任务更深。ESA 仍负责火星车本体、着陆系统和地表运行，而 NASA 的支持重点则是发射、着陆辅助硬件、加热装置以及科学仪器部件。

telegram · zaihuapd · Apr 17, 06:36

**背景**: Rosalind Franklin 是 ESA 的天体生物学火星车，最初作为 ExoMars 计划的一部分开发，目标是在火星上寻找过去或现在生命存在的迹象。该任务的一项关键能力是可向地下钻探最深 2 米，因为有机分子在地下环境中更有可能避开表面辐射和强氧化剂而保存下来。其核心科学设备之一是 Mars Organic Molecule Analyzer，用于分析钻取样本中的有机化合物。该任务多年来反复延期，而如今其发射与部分关键硬件方案依赖 NASA 的新支持才得以明确。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://science.nasa.gov/blogs/mars-rosa/2026/04/16/nasa-begins-implementation-for-esas-rosalind-franklin-mission-to-mars/">NASA Begins Implementation for ESA’s Rosalind Franklin ...</a></li>
<li><a href="https://explorationscience.esa.int/project/exomars-rosalind-franklin-rfm/">ExoMars Rosalind Franklin (RFM) - Exploration Science</a></li>
<li><a href="https://spacenews.com/nasa-and-esa-complete-agreement-for-cooperation-on-mars-rover-mission/">NASA and ESA complete agreement for cooperation on Mars rover ... NASA has given approval to begin implementing its project to ... Falcon Heavy Rosalind Franklin Mission Set for Mars Launch in ... Europe’s Mars Rover Will Use New Nuclear Power Source</a></li>

</ul>
</details>

**标签**: `#SpaceX`, `#NASA`, `#ESA`, `#Mars Exploration`, `#Space Industry`

---

<a id="item-15"></a>
## [Google 推出面向智能代理的 Android CLI](https://android-developers.googleblog.com/2026/04/build-android-apps-3x-faster-using-any-agent.html) ⭐️ 7.0/10

Google 宣布推出 Android CLI，旨在通过以终端为中心、对智能代理更友好的工作流，加快 Android 应用的搭建与开发。该公司表示，在项目创建和开发环境配置方面，它可将相关流程提速至最高 3 倍，并可与 Android skills 以及外部编码代理配合使用。 这很重要，因为 Android 开发长期存在环境配置复杂、工具链繁琐的问题，尤其影响新项目初始化、自动化流程和脚本化搭建。一个能够良好配合 AI 代理的轻量级 CLI，有望让 Android 工作流更容易脱离 Android Studio 进行自动化，并更好地融入现代终端、CI 和代理驱动的开发方式。 这项提速主要针对项目创建和开发环境配置，而不是现有应用中的日常编码工作。Google 的开发者文档还表明，Android CLI 是更大范围代理工作流的一部分，其中 Android skills 提供了面向 AI 优化的指令，可与 Android CLI 和 Android Studio 一起使用。

hackernews · ingve · Apr 16, 18:39

**背景**: CLI 是命令行界面，开发者可以通过 shell 命令而不是图形化 IDE 与工具交互。在 Android 开发中，这种方式有利于实现可重复的环境搭建、自动化流程、CI 管道，以及如今能够执行终端命令的 AI 编码代理。Google 的 Android skills 文档描述了一组集成到 Android CLI 中、面向 AI 的指令，这表明该工具正被定位为同时服务人类开发者和智能代理的程序化接口。这也反映出行业中的更大趋势：让开发工具更容易被基于 LLM 的助手稳定调用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.thurrott.com/dev/335014/google-announces-revitalized-android-cli-for-agentic-development">Google Announces Revitalized Android CLI for Agentic Development</a></li>
<li><a href="https://developer.android.com/tools/agents/android-skills">Overview of Android skills | Android Studio | Android Developers</a></li>

</ul>
</details>

**社区讨论**: 社区讨论总体偏谨慎乐观，但观点不一。一些评论者认为它确实明显简化了初始化流程，另一些人则强调“3 倍提速”更像是针对环境和项目启动阶段，而不是日常开发本身。还有人抱怨 Windows 安装链接失效，并猜测更强的 CLI 可能会降低大家对 Android Studio 的依赖，或者推动更轻量的编辑器集成。

**标签**: `#Android`, `#Developer Tools`, `#CLI`, `#AI Agents`, `#Mobile Development`

---

<a id="item-16"></a>
## [Aphyr 警告 LLM 引发信任崩塌](https://aphyr.com/posts/420-the-future-of-everything-is-lies-i-guess-where-do-we-go-from-here) ⭐️ 7.0/10

Aphyr 在一篇新文章中指出，大语言模型正在以极低成本大规模制造欺骗、垃圾内容和合成文本，从而削弱阅读、思考和写作的社会价值。文章强调，这不是某个产品更新或模型发布，而是一个正在动摇知识工作与公共信任的更广泛转变。 这之所以重要，是因为从教育、媒体到白领工作，许多数字化制度都默认文本背后代表着人类的判断与投入。如果 AI 生成内容在这些系统中扩散的速度超过人类验证能力，就可能导致信任下降、对人类专业能力的激励被削弱，并深刻改变劳动力市场与网络讨论环境。 这篇文章关注的是自动化与欺骗的经济学，而不是某个具体基准成绩或安全实验结果：当具有说服力的文本变得充足且廉价时，筛选与验证反而会成为稀缺资源。Aphyr 即 Kyle Kingsbury，是长期撰写技术分析文章的作者，以批判性地审视计算系统闻名，因此这篇文章更像是系统层面的社会批评，而不是营销式评论。

hackernews · aphyr · Apr 16, 13:32

**背景**: Aphyr 是 Kyle Kingsbury 的笔名，他的博客在技术圈中以讨论计算系统和基础设施的文章而知名。大语言模型通过预测高概率的 token 序列来生成流畅文本，这使它们适合起草和总结任务，但也很容易被用于垃圾信息、冒充和低成本说服性内容。当前围绕 AI 社会影响的讨论，重点不仅在于模型能力本身，也在于当合成文本无处不在时，各类制度是否还能维持信任与问责。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://aphyr.com/">Aphyr - Posts</a></li>
<li><a href="https://www.huffpost.com/entry/25-practical-blogs-to-sharpen-your-coding-skills_b_584b8011e4b01713310510cd">25 Practical Blogs To Sharpen Your Coding Skills | HuffPost Contributor</a></li>

</ul>
</details>

**社区讨论**: 评论区整体上对 Aphyr 的观点表示认同，许多人认为阅读、思考和写作确实正在进入 LLM 自动化的“打击半径”。有些人把 AI 的普及比作汽车的采用：一种技术可以总体上有用，但仍然会带来严重的社会代价，因此在受限、边界清晰的场景中使用它，可能比无差别部署更合理。也有人持更悲观的看法，认为掌控这项技术的人所面对的激励，与社会操控和劳动替代是相一致的。

**标签**: `#AI societal impact`, `#LLMs`, `#misinformation`, `#future of work`, `#Hacker News discussion`

---

<a id="item-17"></a>
## [加州诉讼聚焦亚马逊价格施压](https://www.theguardian.com/us-news/ng-interactive/2026/apr/16/amazon-price-fixing-california-lawsuit) ⭐️ 7.0/10

加州针对亚马逊的反垄断案件中新近解封的法庭文件，据称详细描述了该公司如何惩罚在其他网站上提供更低价格的卖家。根据加州总检察长的主张，这些做法可能让更广泛的在线零售市场价格维持在较高水平。 这之所以重要，是因为亚马逊是主导性的电商平台，若其规则阻止其他渠道出现更低价格，影响的就不只是亚马逊卖家，而是整个互联网的价格竞争。此案也进一步强化了外界对大型数字平台如何利用平台规则塑造市场行为、并可能引发反垄断问题的审视。 亚马逊现有的平台政策已经明确表示，如果其认为某些定价做法会损害消费者信任，可能会移除 Buy Box、下架商品报价，甚至暂停卖家资格。从反垄断角度看，被指控的行为类似一种价格平价或 MFN 式施压，即平台阻止卖家在竞争渠道提供更优条件，即使具体合同机制是否完全属于 MFN 仍可能存在争议。

hackernews · kmfrk · Apr 16, 22:08

**背景**: Amazon Marketplace 是一个让第三方卖家接触亚马逊用户的平台，而像 Buy Box 这样的展示位置会显著影响销量。亚马逊的 Fair Pricing Policy 说明，如果某些报价的定价做法削弱消费者信任，平台可能采取措施，包括移除 Buy Box 或直接移除报价。围绕 MFN（即“最惠国”）条款的反垄断争议，通常关注强势平台是否借助价格平价要求，阻止竞争服务出现更低价格。加州反垄断法包括 Cartwright Act，通常被认为比联邦反垄断法覆盖更广，因此这类案件在加州具有特殊重要性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://sellercentral.amazon.com/help/hub/reference/external/G5TUVJKZHUVMN77V?locale=en-US">Amazon Marketplace Fair Pricing Policy</a></li>
<li><a href="https://m.media-amazon.com/images/G/02/rainier/help/legal/Amazon_Marketplace_Fair_Pricing_Policy_EN_161220.pdf">Amazon marketplace fair pricing policy</a></li>
<li><a href="https://www.americanbar.org/groups/business_law/resources/business-law-today/2026-february/californias-antitrust-regulations-go-beyond-federal-protections-how-consumers-benefit/">California’s Antitrust Regulations Go Beyond Federal ...</a></li>

</ul>
</details>

**社区讨论**: 有卖家经验的评论者表示，指控内容与亚马逊的实际运作方式基本一致：如果亚马逊发现其他地方价格更低，商品可能失去显著展示位置，被挤到主要购买框之外。也有人指出，此案更像是对既有认知的进一步补充，而不是重大新爆料；还有人提到“结账时才显示价格”等做法，是商家规避自动价格抓取的一种方式。

**标签**: `#antitrust`, `#Amazon`, `#e-commerce`, `#platform regulation`, `#competition policy`

---

<a id="item-18"></a>
## [Google 预览 Gemini 3.1 Flash TTS](https://simonwillison.net/2026/Apr/15/gemini-31-flash-tts/#atom-everything) ⭐️ 7.0/10

Google 已发布 Gemini 3.1 Flash TTS 预览版，作为 Gemini API 中的文本转语音模型，模型 ID 为 `gemini-3.1-flash-tts-preview`。该模型只能生成音频输出，并且可以通过详细提示词来控制语音风格、口音、语速、场景设定以及逐句表演提示。 这很重要，因为它让文本转语音从简单的声音选择进一步发展为可通过提示词控制的语音生成，开发者能够更直接地调节表现力和呈现方式。对于语音代理、媒体制作、企业旁白等场景，这种更自然且可控的音频输出有望显著提升用户体验。 根据 Google 的文档，在 Gemini API 中进行 TTS 生成时，需要将响应模态设置为 audio，并通过语音配置选择输出声音。Google 表示该模型提升了可控性、表现力和语音质量，但目前仍处于预览阶段，可通过 Gemini API 和 Google AI Studio 使用，企业侧则在 Vertex AI 预览，Workspace 也通过 Google Vids 提供接入。

rss · Simon Willison · Apr 15, 17:13

**背景**: 传统的文本转语音系统通常接收纯文本和一个选定声音，然后返回朗读音频，除了语速或音高等参数外，对表演方式的控制通常比较有限。Gemini 3.1 Flash TTS 体现了一种更新的方法：开发者可以使用自然语言提示词和 transcript tags，不仅描述“说什么”，还可以描述“怎么说”。在 Google 的语音生成文档中，输出需要被明确配置为 audio，生成结果可以保存为 wave 文件。这也说明该模型属于更广泛的生成式音频趋势，即让语音工具更像通用语言模型，而不是固定功能的语音引擎。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-3-1-flash-tts/">Gemini 3.1 Flash TTS: New text-to-speech AI model - The Keyword</a></li>
<li><a href="https://ai.google.dev/gemini-api/docs/speech-generation">Text-to-speech generation (TTS) | Gemini API | Google AI for ...</a></li>
<li><a href="https://ai.google.dev/gemini-api/docs/models/gemini-3-flash-preview">Gemini 3 Flash Preview | Gemini API | Google AI for Developers</a></li>

</ul>
</details>

**标签**: `#AI`, `#Text-to-Speech`, `#Gemini`, `#Google`, `#Generative Audio`

---

<a id="item-19"></a>
## [企业 AI 的护城河在操作层](https://www.technologyreview.com/2026/04/16/1135554/treating-enterprise-ai-as-an-operating-layer/) ⭐️ 7.0/10

MIT Technology Review 认为，企业 AI 的关键战略竞争点正从基础模型的跑分与基准测试，转向将 AI 嵌入业务流程的“操作层”。文章指出，长期优势将来自于谁能掌控模型在企业运营中的集成、治理以及持续迭代改进方式。 这很重要，因为模型性能越来越容易被比较，也更有可能被商品化，而工作流集成、治理和运营反馈闭环则更难复制。对企业而言，这意味着最具防御性的价值，可能不在于选择某个“最强模型”，而在于能够把 AI 连接到内部系统、制度约束和日常执行的平台。 文章将“操作层”定义为智能被应用、治理和持续优化的地方，强调部署架构与迭代学习的重要性高于单纯的模型分数。其核心含义是，如果企业希望 AI 系统形成持久的商业价值，就需要具备策略执行、工作流编排和持续改进的基础设施。

rss · MIT Technology Review · Apr 16, 13:00

**背景**: 在企业 AI 中，基础模型是能够生成文本、代码或其他输出的通用模型，但要在公司内部真正发挥作用，通常还需要外围系统的配合。近期行业文章常把 AI operating model 或 AI OS 描述为一个协调模型、工作流、上下文以及企业数据的层，用于支撑跨应用的运行。随着 AI 越来越深地嵌入业务流程，治理也变得更加关键，因为企业必须管理风险、合规、透明度和控制问题。因此，越来越多观察者开始区分“模型能力”和让 AI 在真实企业中可靠规模化落地的“应用层或操作层”。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.technologyreview.com/2026/04/16/1135554/treating-enterprise-ai-as-an-operating-layer/">Treating enterprise AI as an operating layer | MIT Technology ...</a></li>
<li><a href="https://www.alation.com/blog/enterprise-AI-operating-model/">How to Build an Enterprise AI Operating Model That Scales ...</a></li>
<li><a href="https://www.ibm.com/think/insights/ai-governance-implementation">Guide for Implementing an AI Governance Framework | IBM</a></li>

</ul>
</details>

**标签**: `#enterprise AI`, `#AI strategy`, `#platforms`, `#governance`, `#industry trends`

---

<a id="item-20"></a>
## [全球失衡卷土重来](https://www.economist.com/finance-and-economics/2026/04/16/global-imbalances-are-back-whos-to-blame) ⭐️ 7.0/10

《经济学人》指出，2026 年全球大型经济失衡再次扩大，关于究竟是哪些国家或结构性力量在推动这一趋势的争论重新升温。焦点在于持续经常账户顺差国家与持续大额逆差国家之间的缺口再次拉大，尤其是美国的逆差问题。 全球失衡之所以重要，是因为它会影响贸易摩擦、汇率、资本流动以及金融危机风险。若大规模顺差和逆差持续存在，政策制定者、投资者、出口商和中央银行都可能面临更大的保护主义压力、汇率调整风险以及更不稳定的跨境融资格局。 经常账户失衡本质上反映的是一国国内储蓄与投资之间的缺口，因此争论对象不仅是贸易政策，也包括财政政策、居民储蓄、企业投资和人口结构等因素。IMF 和英格兰银行的最新分析显示，这些失衡在 2008—09 年危机后曾明显收窄，但近期再次扩大，说明其深层驱动因素并未真正消失。

rss · The Economist Finance · Apr 16, 09:58

**背景**: 所谓全球失衡，通常是指主要经济体之间长期且规模较大的经常账户顺差与逆差。顺差国的国内储蓄高于本国投资，因此会向海外输出资本；逆差国则需要吸收外国资本，以支撑超过本国储蓄水平的支出。这种格局在 2008 年全球金融危机前已成为重大议题，因为许多经济学家认为它与过度借贷、资产泡沫和脆弱的金融中介体系有关。根据 IMF 和英格兰银行的最新研究，危机后曾收敛的失衡如今部分反弹，也重新点燃了关于责任究竟在国内政策还是更深层结构性力量的争论。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.bankofengland.co.uk/bank-insights/2026/global-imbalances-are-back">Global imbalances are back - Bank of England</a></li>
<li><a href="https://www.imf.org/en/publications/policy-papers/issues/2026/04/06/understanding-global-imbalances-575234">Understanding Global Imbalances</a></li>
<li><a href="https://www.cfr.org/articles/global-imbalances-tracker">Global Imbalances Tracker - Council on Foreign Relations</a></li>

</ul>
</details>

**标签**: `#macroeconomics`, `#global-trade`, `#financial-stability`, `#international-economics`, `#capital-flows`

---

<a id="item-21"></a>
## [巴基斯坦外交缓压却拖延改革](https://www.economist.com/finance-and-economics/2026/04/16/pakistans-deft-diplomacy-is-an-economic-blessing-and-a-curse) ⭐️ 7.0/10

《经济学人》指出，到 2026 年，巴基斯坦凭借娴熟的外交手腕获得了短期经济纾困和外部支持。然而，这种成功也在减轻该国统治者推进艰难结构性改革的压力，而这些改革本是实现长期稳定所必需的。 这之所以重要，是因为暂时的财政缓冲虽然能帮助巴基斯坦避免眼前危机，但也可能固化反复失稳的循环。对投资者、政策制定者和新兴市场观察者而言，这一分析很重要，因为它直接揭示了地缘政治如何影响经济改革是被推进还是被搁置。 核心观点并不是外交本身有害，而是它给巴基斯坦领导层提供了推迟高政治成本改革的空间。文章将外交成功描述为一把双刃剑：短期内有助于争取支持，但如果削弱改革激励，长期可能带来负面后果。

rss · The Economist Finance · Apr 16, 09:58

**背景**: 巴基斯坦长期面临反复出现的宏观经济压力，包括外部融资紧张以及对外部援助的周期性依赖。在这种情况下，外交关系可能帮助其争取资金、缓解市场压力，或获得外国伙伴的政治支持。所谓结构性改革，通常指更困难的国内调整，例如改善财政纪律、扩大税基，或改变国家主导的经济安排。这里所描述的矛盾在新兴市场中很常见：外部支持可以争取时间，但并不会自动解决深层脆弱性。

**标签**: `#Pakistan`, `#geopolitics`, `#macroeconomics`, `#emerging-markets`, `#economic-reform`

---

<a id="item-22"></a>
## [古老微生物防御塑造人类免疫](https://www.quantamagazine.org/the-ancient-weapons-active-in-your-immune-system-today-20260415/) ⭐️ 7.0/10

Quanta Magazine 在 2026 年发表了一篇综述性报道，汇总了近年的数十项发现，指出最早在数十亿年前由细菌和病毒演化出的微生物防御系统，至今仍构成人类先天免疫系统的重要基础。文章强调，与抗病毒感知和细胞死亡相关的机制具有非常深远的进化根源，而不是动物独有的全新发明。 这很重要，因为它把先天免疫重新理解为古老宿主—病原体战争的延续，有助于解释为何关键免疫通路会如此广泛且高度保守。它也与生物技术和医学相关，因为理解 cGAS-STING、gasdermins 等系统的微生物起源，可能为免疫工程和治疗研究提供方向。 检索结果中的近期综述指出，多个真核生物先天免疫组分都存在参与抗病毒防御的细菌同源物，包括 gasdermins、cGAS-STING 和 argonautes。更关键的结论并不是人类免疫与细菌免疫完全相同，而是病原感知、防御信号传递以及牺牲受感染细胞等核心原则，似乎在极其漫长的进化过程中被不断改造和继承下来。

rss · Quanta Magazine · Apr 15, 14:47

**背景**: 先天免疫是机体对感染作出的快速、非特异性第一道防线；相比之下，适应性免疫会形成更有针对性且持续更久的反应。近年来，研究人员发现，动物体内一些标志性的先天免疫系统在细菌中存在进化上的“亲缘系统”，它们能够帮助细菌识别病毒并启动保护性反应。Trends in Immunology 和 Current Opinion in Microbiology 的综述都指出，这些共享系统揭示了跨生命形式抗病毒防御的共同设计原则。之所以这一方向受到关注，是因为它把微生物学、进化生物学和免疫学连接成了现代免疫机制的统一起源叙事。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.quantamagazine.org/the-ancient-weapons-active-in-your-immune-system-today-20260415/">The Ancient Weapons Active in Your Immune System Today</a></li>
<li><a href="https://www.cell.com/trends/immunology/fulltext/S1471-4906(23)00208-9">Innate immunity: the bacterial connection: Trends in Immunology</a></li>
<li><a href="https://www.sciencedirect.com/science/article/pii/S0952791524000359">Principles of bacterial innate immunity against viruses</a></li>

</ul>
</details>

**标签**: `#immunology`, `#evolutionary-biology`, `#microbiology`, `#biotechnology`, `#science-journalism`

---

<a id="item-23"></a>
## [宇宙尘埃或可解释金星下层霾](https://www.nature.com/articles/d41586-026-01212-5) ⭐️ 7.0/10

《Nature》报道了一项于 2026 年 4 月发表在《Nature Astronomy》的新建模研究，认为金星长期难以解释的下层霾可能主要由进入大气层的宇宙尘埃颗粒构成。该研究提出，来自太空的亚微米颗粒会在大气中下沉，并帮助形成位于金星硫酸云层下方的不透明雾霾层。 如果这一结论成立，它将为行星科学家解释金星大气中一个长期未解之谜提供新答案，并改变人们对下层霾物质来源的既有假设。这也可能改进金星的大气与化学模型，而这对于解读探测器观测结果和规划未来金星任务都很重要。 《Nature Astronomy》论文指出，此前进入金星大气的探测器已经在地表与主云层之间的下层霾中发现了不挥发的亚微米颗粒，但其来源一直不清楚。模型表明，来自外太空的尘埃可以先在高空与硫酸云物质混合并继续下沉；当这些颗粒穿过云底进入更温暖的下层大气时，硫酸会蒸发，留下构成下层霾的颗粒群体。

rss · Nature · Apr 16, 00:00

**背景**: 金星拥有极其稠密的大气层，其厚重云层主要由硫酸液滴组成。在主云层下方，探测器还观测到由微小颗粒构成的独立雾霾层，但科学界一直在争论这些颗粒究竟是由金星本地化学过程形成，还是来自其他来源。宇宙尘埃是来自彗星、小行星和行星际空间的微小颗粒持续落入行星大气的过程，它们可以充当气溶胶或云粒形成的“种子”。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.nature.com/articles/s41550-026-02843-4">A cosmic origin of Venus’ lower haze - Nature Astronomy</a></li>
<li><a href="https://en.wikipedia.org/wiki/Atmosphere_of_Venus">Atmosphere of Venus - Wikipedia</a></li>
<li><a href="https://www.nature.com/articles/s41550-026-02843-4.pdf">A cosmic origin of Venus' lower haze - Nature</a></li>

</ul>
</details>

**标签**: `#planetary-science`, `#venus`, `#atmospheric-modeling`, `#space-science`, `#nature`

---

<a id="item-24"></a>
## [衰老或按性别重塑疾病风险](https://www.nature.com/articles/d41586-026-01213-4) ⭐️ 7.0/10

Nature 于 2026 年 4 月 16 日发表的新闻报道介绍了一项研究：与年龄相关的基因表达变化，可能有助于解释为何女性会随着衰老而更容易发生自身免疫性疾病。该研究还指出，衰老可能通过不同的性别相关免疫老化轨迹，提高男性对某些癌症的易感性。 这一发现之所以重要，是因为它把衰老、基因调控和生物性别与两大重要疾病领域联系了起来：自身免疫病和癌症。如果后续研究得到验证并进一步扩展，它可能推动老年医学和免疫相关医学中更具性别针对性的风险预测、预防和治疗策略。 更广泛的研究背景表明，免疫系统的衰老具有明显的性别二态性，即免疫细胞丰度和基因表达的年龄相关重塑在女性和男性之间并不相同。与免疫衰老和表观遗传变化相关的研究还提示，T 细胞基因调控会随年龄改变，从而提高自身免疫病和癌症的易感性，不过这里的 Nature 条目是新闻报道，而不是完整呈现原始论文内容的文章。

rss · Nature · Apr 16, 00:00

**背景**: 自身免疫性疾病是指免疫系统错误攻击人体自身组织的一类疾病，而其中许多疾病在女性中更常见。免疫衰老，也称 immunosenescence，指的是免疫细胞功能、组成和调控随年龄发生的变化。既往研究提示，免疫细胞尤其是 T 细胞中与衰老相关的表观遗传和基因表达改变，可能促进慢性炎症并破坏免疫平衡。近期研究还表明，男性和女性的免疫系统并不是以相同方式衰老的，这可能有助于解释晚年疾病风险的性别差异。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.nature.com/articles/d41586-026-01213-4">Ageing could prime women for autoimmune disorders - Nature</a></li>
<li><a href="https://www.nature.com/articles/s43587-026-01110-5">Biological sex shapes divergent trajectories of immune aging</a></li>
<li><a href="https://pmc.ncbi.nlm.nih.gov/articles/PMC6548177/">Immune Senescence, Epigenetics and Autoimmunity - PMC</a></li>

</ul>
</details>

**标签**: `#aging`, `#autoimmune-disease`, `#gene-expression`, `#cancer`, `#biomedical-research`

---

<a id="item-25"></a>
## [创纪录数量研究人员竞选美国公职](https://www.nature.com/articles/d41586-026-01134-2) ⭐️ 7.0/10

Nature 于 2026 年 4 月 16 日报道，美国中期选举中竞选公职的研究人员数量创下新高。许多民主党候选人表示，特朗普政府对科学领域的削减促使他们投身政治，而一些共和党候选人则被能源和 AI 政策所吸引。 这表明科学政策正越来越直接地成为选举议题，而不再只是大学和科研机构内部的游说问题。这可能影响立法者如何处理联邦科研经费，以及与能源和 AI 相关的监管和投资。 文章将这波候选人增长描述为跨党派现象，但两党的动机不同：科研经费削减是许多民主党人的主要推动因素，而能源和 AI 等技术与产业政策领域则吸引了一些共和党人。这篇报道关注的是研究人员参与选举，而不是新的政策宣布或立法变化。

rss · Nature · Apr 16, 00:00

**背景**: 研究人员过去也曾进入美国政坛，但与法律和商业等职业相比，他们在民选公职中的代表性历来偏低。国会和行政部门作出的联邦科研经费决定，会强烈影响大学、国家实验室以及依赖资助的研究项目。与此同时，能源和 AI 政策也已成为更受关注的政治议题，因为它们关系到经济竞争力、国家安全、基础设施和产业战略。

**标签**: `#science-policy`, `#US-politics`, `#research-funding`, `#AI-policy`, `#elections`

---

<a id="item-26"></a>
## [脑细胞性别相关基因活性图谱揭示](https://www.nature.com/articles/d41586-026-01227-y) ⭐️ 7.0/10

Nature 于 2026 年 4 月 16 日发表新闻，介绍了一项研究：男性与女性的人类脑细胞在基因表达上存在差异。相关研究使用了跨多个大脑皮层区域的单细胞转录组分析，并发现这种差异取决于细胞类型和脑区。 这些发现有助于解释为何许多神经系统和精神疾病在风险、患病率或病程上存在性别差异。它也支持更精准的脑疾病研究模型，因为具有生物学意义的差异可能出现在特定细胞类型层面，而不只是整体组织层面。 根据搜索结果中的 Science 论文，这些性别差异会随细胞类型和皮层区域而变化，其中许多还与已知疾病位点相关。作者据报道没有发现细胞类型比例存在性别偏倚变化，这表明信号主要来自细胞内部的基因活性差异，而不是由细胞组成不同所致。

rss · Nature · Apr 16, 00:00

**背景**: 基因表达指的是基因被转录成 RNA 的活跃程度，它可以反映细胞当下的生物学状态。单细胞转录组技术能够测量单个细胞中的 RNA，因此可以发现整体组织研究中容易被平均掉的差异。以往研究已提示成人大脑中存在广泛的性别相关基因表达差异，而较新的单细胞研究则能把这些差异定位到特定的神经元和非神经元细胞群。之所以重要，是因为许多脑疾病都表现出性别偏倚，而其机制可能只涉及特定脑区中的部分细胞。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.science.org/doi/10.1126/science.aea9063">Sex effects on gene expression across the human cerebral ...</a></li>
<li><a href="https://www.nature.com/articles/d41586-026-01227-y">Revealed: how male and female brain cells differ in gene activity</a></li>
<li><a href="https://www.frontiersin.org/journals/neuroscience/articles/10.3389/fnins.2024.1340108/full">Exploring sex differences: insights into gene expression ...</a></li>

</ul>
</details>

**标签**: `#neuroscience`, `#genomics`, `#sex differences`, `#brain disease`, `#biomedical research`

---

<a id="item-27"></a>
## [DeepL 推出实时语音翻译](https://techcrunch.com/2026/04/16/deepl-known-for-text-translation-now-wants-to-translate-your-voice/) ⭐️ 7.0/10

4 月 16 日，DeepL 发布了实时语音翻译套件 DeepL Voice，标志着公司从文本翻译进一步扩展到实时语音翻译领域。此次发布还包括对 Zoom 和 Microsoft Teams 的支持、实时翻译音频与字幕，以及面向呼叫中心和多语言群聊等企业场景的 API，并支持通过 QR 码快速加入。 这对一家知名翻译公司来说是一次重要的产品扩展，意味着其核心能力开始进入实时会议和企业业务流程。对于已经依赖会议软件、并希望将翻译能力直接嵌入自有系统的企业来说，这可能会显著降低跨语言协作的门槛。 DeepL 表示，这类产品的核心技术难点是在实时场景中平衡延迟与翻译准确度，目前系统采用的是“语音转文本再转语音”的处理架构，而不是端到端的直接语音翻译模型。公司还表示，该系统能够学习行业术语和专有名词，以提升专业场景下的翻译质量，目前产品已进入早期访问阶段，并开放企业候补名单。

telegram · zaihuapd · Apr 17, 03:04

**背景**: 实时语音翻译系统通常会结合自动语音识别、机器翻译和语音合成，因此必须在足够快的前提下完成处理，才能让对话保持自然流畅。实际应用中，低延迟与高准确度之间存在公认的权衡，因为可用上下文越少，语音识别和翻译结果往往越不稳定。DeepL 过去主要以文本翻译闻名，因此这次发布意味着它把原有的语言技术进一步拓展到了语音协作和企业定制集成场景。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.speechmatics.com/latency_accuracy">Exploring the trade-off between speed and accuracy in real ...</a></li>

</ul>
</details>

**标签**: `#AI语音翻译`, `#DeepL`, `#企业软件`, `#实时翻译`, `#API`

---

<a id="item-28"></a>
## [360 智能体发现两项高危漏洞](https://finance.sina.com.cn/tech/2026-04-17/doc-inhuupth6598363.shtml) ⭐️ 7.0/10

360 表示，其自研漏洞挖掘智能体发现了两项潜伏多年的重大漏洞，分别是 Windows 内核提权漏洞和 Office 远程代码执行漏洞。公司称，这两项问题已上报国家漏洞库并完成修复，全球受影响的 Windows 和 Office 用户超过 10 亿。 如果相关说法属实，这将是 AI 辅助安全研究的重要里程碑，因为它表明智能体有望帮助发现广泛部署于个人终端、企业系统和关键基础设施中的基础软件高影响漏洞。这也进一步印证了网络安全行业正在从主要依赖人工的漏洞研究，转向机器辅助甚至“机器对机器”的攻防模式。 Windows 内核提权漏洞通常意味着本地攻击者可以获取更高系统权限，而 Office 远程代码执行漏洞则可能让攻击者通过恶意文档或相关内容执行任意代码。不过，目前公开报道尚未给出 CVE 编号、利用链、受影响版本或技术成因分析，因此这一成果虽然重要，但外界暂时难以做深入独立验证。

telegram · zaihuapd · Apr 17, 05:06

**背景**: Windows 内核提权漏洞通常指操作系统核心组件中的缺陷，使已经获得一定访问权限的攻击者进一步提升到管理员或 SYSTEM 级权限。Office 远程代码执行漏洞一般意味着攻击者可通过特制的 Office 文档等内容，在目标打开或处理文件时触发任意代码执行。漏洞挖掘智能体是用于自动化代码分析、漏洞发现和验证等安全研究环节的 AI 系统，近来的公开案例显示，这类系统在速度和规模上正在快速提升。360 此次披露也属于这一趋势中的一部分，但目前仍主要是企业主导的消息发布，而非包含完整技术细节的安全通告。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.xinhuanet.com/tech/20260417/56c896ca06a34c61b3cd1eff7a944776/c.html">360发现全球高危漏洞 漏洞挖掘智能体首次披露-新华网</a></li>
<li><a href="https://cloud.tencent.com/developer/article/2227844">windows10内核态提权方法汇总-腾讯云开发者社区-腾讯云</a></li>
<li><a href="https://cloud.tencent.com/developer/article/2549773">CVE-2025-32717｜Microsoft Word 远程代码执行漏洞</a></li>

</ul>
</details>

**标签**: `#cybersecurity`, `#AI agents`, `#vulnerability research`, `#Windows`, `#Office`

---

<a id="item-29"></a>
## [科研削资与 AI 科学家零工化](https://www.thenation.com/article/society/ai-silicon-valley-andreesen-thiel-stem/) ⭐️ 7.0/10

《The Nation》的一篇评论性报道称，具有政治影响力的硅谷投资人正从美国公共科研经费削减中获益，因为被挤出的科学家被引向零工化的 AI 训练工作。文章将 NSF、NIH 等机构受到的经费收缩，与 Mercor 和 ScaleAI 等平台获得更多博士级劳动力联系起来。 这一论点之所以重要，是因为它把科研政策、劳动力市场和 AI 商业化连成了一条链条：公共科研被削弱，可能同时增强私营 AI 公司获取高技能低成本劳动力的能力。如果这种趋势持续下去，长期后果可能是国家科研能力下降，而专业人才从相对稳定的科研机构转向平台化、临时性的工作。 这篇文章属于评论性批判，而不是官方政策公告，因此其核心主张更偏向因果和政治分析，而非新的公开数据或正式规定。作为事实背景，Mercor 官网明确宣传与 frontier research、RLHF 数据和 AI agent training 相关的远程 AI 岗位，而 R&D World 与 Science News 的报道也显示，NSF 和 NIH 在 2025 年确实出现了经费冻结、裁撤和拨款削减。

telegram · zaihuapd · Apr 17, 05:51

**背景**: NSF 和 NIH 是美国最重要的公共科研资助机构之一，支持大学实验室、科研项目以及部分联邦科研岗位。当地经费被削减或冻结时，实验室可能关闭，资助项目可能终止，研究人员也可能被迫离开高校或政府体系寻找其他工作。与此同时，AI 公司越来越依赖具备专业背景的人力来完成 RLHF、模型评估、领域数据处理和训练支持等任务。像 Mercor 这样的平台将这类工作包装为灵活的远程就业，为 AI 实验室和企业匹配专家人才。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.mercor.com/">Mercor | Defining the future of work</a></li>
<li><a href="https://www.rdworldonline.com/nsf-layoffs-in-2025-deep-budget-cuts-headed-for-u-s-research-sector/">Steep budget cuts and layoffs coming to NSF - rdworldonline.com</a></li>
<li><a href="https://www.sciencenews.org/article/nih-nsf-cuts-2025-data">See the alarming extent of NIH and NSF funding cuts in 2025</a></li>

</ul>
</details>

**标签**: `#AI labor`, `#science policy`, `#public research funding`, `#Silicon Valley`, `#US politics`

---