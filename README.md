# 实用项目记录

[English](README.en.md) · **简体中文** · [繁體中文](README.zh-TW.md)

整理学术科研、作品集与设计、英语阅读学习、商业观察相关的项目与工具。所有介绍直接放在本页，按分类阅读。

[学术科研](#学术科研) · [作品集与设计](#作品集与设计) · [英语阅读学习](#英语阅读学习) · [商业观察](#商业观察)

## 学术科研

课程学习、文献整理、研究设计、数据分析与学术表达。

### Frontend Slides · 演示文稿设计

- **介绍**：由 Zara Zhang 开发的演示制作 Skill，帮助 AI 编程助手从文字大纲创建 HTML 幻灯片，也能把已有 PowerPoint 内容转换为网页演示。
- **主要功能**：生成视觉风格预览供选择；提供多种配色、字体和版式；制作带动画的单文件 HTML 演示；提取 PPTX 中的文字、图片和备注；提供 PDF 导出与网页分享脚本。
- **适用场景**：课堂汇报、论文分享、研究展示，以及确定演示文稿的视觉方案。
- **使用说明**：提供文字大纲与图片，选择风格后生成网页演示。Claude Code 可安装为插件，其他能读写文件和运行命令的编程助手可按 SKILL.md 使用。原生输出为 HTML；若需要可编辑 PPTX，可参考截图作者分享的方法：先让 AI 按该技能给出字体、配色与版式方案，再用单独的 PPTX 制作工具实现。此方法需要额外制作步骤，不能把 HTML 或截图 PDF 当作可编辑 PPTX。
- **GitHub**：[zarazhangrui/frontend-slides](https://github.com/zarazhangrui/frontend-slides)

### paper-logic-graph · 论文变逻辑图

- **介绍**：将一篇论文拆解为可交互的论证结构图，把研究问题、理论、方法、发现、贡献和局限串联起来，并保留主张所依据的原文位置。
- **主要功能**：文字导读与论证图联动；嵌套论点卡片；支持、因果与中介、反驳等逻辑关系；侧栏查看原文、翻译、批注和定位；拖动布局、分支聚焦、路径高亮；中文、双语和英文切换；带节点上下文的提问。
- **适用场景**：论文精读、梳理论证链、比较理论关系，以及为文献讨论和研究汇报整理逻辑图。
- **使用说明**：先基于论文抽取 graph.json，再用 build_viewer.py 渲染为可直接打开和分享的单文件 HTML。Claude 可通过 SKILL.md 使用，其他 Agent 可参考仓库的 AGENTS.md 和集成说明。渲染只需 Python 3.8+ 标准库；自动抽取需模型或兼容接口。尽量提供全文，检查引文与关系类型，尤其区分相关、预测、中介与因果。
- **GitHub**：[salt-byte/paper-logic-graph](https://github.com/salt-byte/paper-logic-graph)

### TextFold · 分层阅读工具

- **介绍**：面向论文、网页和长文的分层阅读工具，在全文、简述、关键句、要点和主题五个层级之间切换，先浏览文章结构，再展开具体段落阅读。
- **主要功能**：导入论文链接、网页和 PDF、Word、EPUB 等文件；逐段折叠与展开；原文对照；高亮与页边笔记；翻译和带段落引用的 AI 问答；文献库搜索与分类，并提供 Zotero、Obsidian 和浏览器接入方式。
- **适用场景**：浏览论文结构、阅读长篇资料、对照原文整理笔记，以及在不同信息层级之间切换阅读。
- **使用说明**：可下载 macOS 或 Windows 桌面版，也可通过 Python 包运行本地阅读器。导入材料后连接模型生成阅读层级，再按需展开段落；简述层保留选取的原句，关键句、要点和主题层由 AI 生成。详见[中文说明](https://github.com/chenxiachan/textfold/blob/main/README.zh-CN.md)与[下载页面](https://chenxiachan.github.io/textfold/zh.html#download)。
- **GitHub**：[chenxiachan/textfold](https://github.com/chenxiachan/textfold)

### Study Buddy 学习搭子

- **介绍**：面向大学课程的 AI 陪学 Skill，把课件、教材和往年题整理成知识点讲义，衔接学期规划、逐节学习和考前复习。
- **主要功能**：材料转写与讲义整理；每周学习清单；自定义讲解风格；小测与错题本；模拟卷和考试提纲；演示、课程论文及作业文件制作辅助。
- **适用场景**：同时学习多门课程、整理分散课件、准备期末考试或课程汇报。
- **使用说明**：初始化课程目录后，将材料放入各课的 `原始资料/`，再提出整理或学习需求。当前依赖 Windows、Word / PowerPoint、Node.js ≥ 22.20 和 Python ≥ 3.10；OCR、图片理解及 TeX 提纲需相应配置。Office 转换使用 Windows COM。详见[安装说明](https://github.com/Liunian06/study-buddy#快速开始)。
- **GitHub**：[Liunian06/study-buddy](https://github.com/Liunian06/study-buddy)

### K-Dense Scientific Agent Skills

- **介绍**：覆盖科学研究、数据分析和科研表达的 Agent Skills 集合。
- **主要功能**：文献综合、研究思考、科学数据库与分析工具使用，以及科研写作、图表和汇报。
- **适用场景**：寻找文献处理、数据分析与研究表达所需的专门技能。
- **使用说明**：按具体任务选择模块，并查看模块的 SKILL.md、依赖和安装说明。库内大量内容面向自然科学，社科研究应按方法和任务选择。
- **GitHub**：[K-Dense-AI/scientific-agent-skills](https://github.com/K-Dense-AI/scientific-agent-skills)

### Anthropic Skills · 文档与数据处理

- **介绍**：Anthropic 发布的 Agent Skills 示例集合，包含文档、PDF、演示和表格处理模块。
- **主要功能**：Word 文档处理、PDF 提取与制作、演示文稿制作、电子表格处理。
- **适用场景**：整理研究材料、制作报告和汇报文件、处理表格数据。
- **使用说明**：在仓库中选择 docx、pdf、pptx 或 xlsx 等模块，按原说明配置环境；文档处理模块与其他示例的授权条件需分别查看。
- **GitHub**：[anthropics/skills](https://github.com/anthropics/skills)

### interview-script · 访谈提纲

- **介绍**：用于产品研究的结构化用户访谈提纲技能。
- **主要功能**：组织热身、核心追问与收尾问题，围绕实际经历和既往行为提问。
- **适用场景**：准备用户访谈，或为学术访谈提纲提供初步结构。
- **使用说明**：提供研究目的、访谈对象和关注问题。用于学术研究时，需要依据研究问题和方法调整，原框架采用产品研究与 JTBD 思路。
- **GitHub**：[phuryn/pm-skills · interview-script](https://github.com/phuryn/pm-skills/tree/main/pm-product-discovery/skills/interview-script)

### summarize-interview · 访谈摘要

- **介绍**：把访谈转写稿整理成结构化摘要的技能。
- **主要功能**：提炼用户需求、满意度信号、JTBD 和行动项。
- **适用场景**：整理访谈材料，快速回看主要内容。
- **使用说明**：提供访谈原稿和研究背景；摘要可辅助整理材料，正式质性编码和主题分析需另行开展。
- **GitHub**：[phuryn/pm-skills · summarize-interview](https://github.com/phuryn/pm-skills/tree/main/pm-product-discovery/skills/summarize-interview)

### sql-queries · SQL 查询

- **介绍**：根据自然语言问题和数据库结构生成 SQL 的技能。
- **主要功能**：读取表结构、生成查询，并适配 PostgreSQL、MySQL、BigQuery 等方言。
- **适用场景**：探索数据库、提取研究数据、制作分析报表。
- **使用说明**：提供数据库方言、表结构、字段含义与所需结果，执行时检查查询条件和结果。
- **GitHub**：[phuryn/pm-skills · sql-queries](https://github.com/phuryn/pm-skills/tree/main/pm-data-analytics/skills/sql-queries)

### grammar-check · 文字校对

- **介绍**：检查文本语法、逻辑与衔接，提供局部修改建议。
- **主要功能**：识别语法错误、表达不清和论述衔接问题。
- **适用场景**：校对论文草稿、研究报告和英文摘要。
- **使用说明**：提交文本并说明写作目的与读者；引文准确性和研究结论需根据原始证据核查。
- **GitHub**：[phuryn/pm-skills · grammar-check](https://github.com/phuryn/pm-skills/tree/main/pm-toolkit/skills/grammar-check)

## 作品集与设计

作品案例整理、视觉表达、游戏广告创意与展示材料制作。

### Anthropic Skills · 创意与设计

- **介绍**：包含创意、艺术、设计和文档制作示例的 Agent Skills 集合。
- **主要功能**：提供设计及内容制作的技能示例，支持了解技能组织方式与制作流程。
- **适用场景**：寻找视觉制作方法、设计任务参考和展示材料工具。
- **使用说明**：浏览仓库的创意与设计模块，按具体技能说明确认所需工具、依赖与授权。
- **GitHub**：[anthropics/skills](https://github.com/anthropics/skills)

### ian-xiaohei-illustrations · 小黑正文配图

- **介绍**：将中文文章的观点、流程和隐喻转成手绘解释图的技能。
- **主要功能**：提炼正文观点、设计视觉隐喻、编写配图提示词并检查画面；以小黑角色、白底和少量彩色批注组织画面。
- **适用场景**：文章正文、方法说明和工作流程的辅助配图。
- **使用说明**：提供正文与配图位置，结合核心观点确定画面表达，再生成和检查图片。
- **GitHub**：[helloianneo/ian-xiaohei-illustrations](https://github.com/helloianneo/ian-xiaohei-illustrations)

### block-creative · 游戏广告创意

- **介绍**：面向 Block、重力与休闲解谜游戏的广告创意与脚本评审技能。
- **主要功能**：竞品素材拆解、创意变体、分镜脚本、逐段审稿与投放测试设计。
- **适用场景**：制作游戏广告创意案例、分析竞品素材、修改分镜脚本。
- **使用说明**：提供视频、截图或脚本及任务要求；基于素材证据分析，投放表现需要通过实际数据判断。
- **GitHub**：个人本地技能，未提供公开仓库链接。

### review-resume · 经历与成果梳理

- **介绍**：面向产品经理简历的评审和岗位匹配技能。
- **主要功能**：检查结构、成果表达、关键词与岗位相关性。
- **适用场景**：梳理个人经历、提炼项目贡献，为作品集案例叙事准备素材。
- **使用说明**：提供简历或经历文本，可同时提供目标岗位；具体作品的设计过程与视觉展示需另行整理。
- **GitHub**：[phuryn/pm-skills · review-resume](https://github.com/phuryn/pm-skills/tree/main/pm-toolkit/skills/review-resume)

## 英语阅读学习

英文阅读后的表达练习与文本校对。

### grammar-check · 英文表达反馈

- **介绍**：用于英文阅读后摘要和表达练习的辅助校对技能。
- **主要功能**：检查语法、句间逻辑和表达衔接，给出针对性的修改建议。
- **适用场景**：读完文章后写英文摘要、复述或个人评论。
- **使用说明**：提供自己写的英文与表达目标；如需核对摘要是否符合文章，应一并提供原文。
- **GitHub**：[phuryn/pm-skills · grammar-check](https://github.com/phuryn/pm-skills/tree/main/pm-toolkit/skills/grammar-check)

## 商业观察

产品收入、商业模式、获客方式与增长案例。

### How Profitable Startups Grow · BizPeel 产品收入与获客清单

- **介绍**：汇集创业产品的收入区间、增长趋势、赛道和获客线索，关联 BizPeel 的商业研究报告。
- **主要功能**：按收入、增长速度、近期新增和赛道查看产品；提供创始人或官方账号、增长问题与研究报告入口。2026-11-05 的仓库说明收录 742 个产品，作者说明按周更新。
- **适用场景**：独立开发选题、竞品观察，以及 SEO、社交媒体和其他获客渠道的案例学习。
- **使用说明**：GitHub 清单可公开阅读，[中文入口](https://github.com/yihui-dev/how-profitable-startups-grow/blob/main/README.zh-CN.md)和 [BizPeel 产品库](https://bizpeel.com/library)可进一步浏览。完整报告涉及解锁或付费；收入区间来自公开信息，需结合日期和来源理解，MRR 与近 30 天收入应分别看待。代码采用 MIT，表格内容版权归 BizPeel，引用需署名。
- **GitHub**：[yihui-dev/how-profitable-startups-grow](https://github.com/yihui-dev/how-profitable-startups-grow)

## 关于本记录

项目介绍根据各项目公开说明和提供的资料整理。安装、依赖、授权及费用以原项目为准。

参考 [Awesome Short Drama Skills](https://github.com/UnderleveledBuilder/awesome-short-drama-skills) 的分类方式整理，持续补充实用项目。
