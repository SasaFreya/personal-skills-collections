# Practical Project Notes

**English** · [简体中文](README.md) · [繁體中文](README.zh-TW.md)

Projects and tools for academic research, portfolios and design, English reading, and business observation. All descriptions are on this page, organized by category.

[Academic Research](#academic-research) · [Portfolios and Design](#portfolios-and-design) · [English Reading](#english-reading) · [Business Observation](#business-observation)

## Academic Research

Course learning, literature organization, research design, data analysis, and academic communication.

### Frontend Slides · Presentation Design

- **Introduction**: A presentation skill by Zara Zhang that helps coding agents create HTML slides from an outline or convert existing PowerPoint content into a web presentation.
- **Key features**: Visual style previews; color, typography, and layout presets; animated single-file HTML decks; extraction of text, images, and notes from PPTX; scripts for PDF export and web sharing.
- **Use cases**: Class presentations, paper discussions, research talks, and developing a presentation’s visual direction.
- **Usage**: Provide an outline and images, choose a visual style, and generate a web deck. Claude Code supports plugin installation; other coding agents with file and shell access can follow SKILL.md. Native output is HTML. For editable PPTX, the screenshot’s author suggests first requesting a typography, color, and layout plan, then implementing it with a separate PPTX authoring tool. This requires an additional production step; HTML and screenshot-based PDFs are not editable PPTX files.
- **GitHub**: [zarazhangrui/frontend-slides](https://github.com/zarazhangrui/frontend-slides)

### paper-logic-graph · Papers into Argument Maps

- **Introduction**: Turns a paper into an interactive argument map connecting research questions, theory, methods, findings, contributions, and limitations, with source locations for the claims.
- **Key features**: Linked reading guide and argument map; nested claim cards; support, causal, mediating, and opposing relations; a sidebar for source passages, translations, annotations, and locations; draggable layouts, branch focus, and path highlighting; Chinese, bilingual, and English views; questions with node context.
- **Use cases**: Close reading, tracing arguments, comparing theoretical relationships, and preparing logical diagrams for literature discussions and research presentations.
- **Usage**: Extract graph.json from a paper, then render it with build_viewer.py into a self-contained HTML file for viewing and sharing. Claude can use SKILL.md; other agents can follow the repository’s AGENTS.md and integration guide. Rendering uses only the Python 3.8+ standard library; automated extraction needs a model or compatible API. Prefer full text and check quotations and relationship labels, particularly the distinctions between correlation, prediction, mediation, and causation.
- **GitHub**: [salt-byte/paper-logic-graph](https://github.com/salt-byte/paper-logic-graph)

### TextFold · Layered Reading

- **Introduction**: A layered reader for papers, web pages, and long documents. Switch between full text, abridged text, key sentences, key points, and topics to explore the structure before expanding individual paragraphs.
- **Key features**: Import paper links, web pages, and files such as PDF, Word, and EPUB; fold and expand paragraphs; compare with original pages; add highlights and margin notes; translate and ask AI questions with paragraph references; search and organize a library, with Zotero, Obsidian, and browser integration options.
- **Use cases**: Exploring paper structure, reading long documents, taking notes alongside the original text, and moving between different levels of detail.
- **Usage**: Download the macOS or Windows desktop app, or run the local reader through the Python package. Import materials and connect a model to generate reading layers, then expand paragraphs as needed. The abridged layer preserves selected original sentences; key sentences, key points, and topics are AI-generated. See the [project documentation](https://github.com/chenxiachan/textfold) and [download page](https://chenxiachan.github.io/textfold/).
- **GitHub**: [chenxiachan/textfold](https://github.com/chenxiachan/textfold)

### Study Buddy

- **Introduction**: An AI study companion Skill for university courses. It turns slides, textbooks, and past exam papers into topic-based notes, connecting semester planning, guided study, and exam revision.
- **Key features**: Material transcription and note organization; weekly study lists; customizable teaching styles; quizzes and error logs; mock exams and revision outlines; support for presentations, course papers, and assignment files.
- **Use cases**: Managing several courses, organizing scattered slides, and preparing for final exams or course presentations.
- **Usage**: Initialize a course directory, put materials in each course’s `原始资料/` folder, and describe your study or organization needs. Currently requires Windows, Word / PowerPoint, Node.js ≥ 22.20, and Python ≥ 3.10. OCR, image interpretation, and TeX outlines require additional configuration. Office conversion uses Windows COM. See the [installation instructions](https://github.com/Liunian06/study-buddy#快速开始).
- **GitHub**: [Liunian06/study-buddy](https://github.com/Liunian06/study-buddy)

### K-Dense Scientific Agent Skills

- **Introduction**: A collection of Agent Skills covering scientific research, data analysis, and research communication.
- **Key features**: Literature synthesis, research reasoning, scientific databases and analysis tools, scientific writing, figures, and presentations.
- **Use cases**: Finding specialized skills for literature processing, data analysis, and communicating research.
- **Usage**: Choose modules for your task and read their SKILL.md files, dependencies, and installation instructions. Much of the collection concerns natural sciences; select social science applications by method and task.
- **GitHub**: [K-Dense-AI/scientific-agent-skills](https://github.com/K-Dense-AI/scientific-agent-skills)

### Anthropic Skills · Documents and Data

- **Introduction**: Anthropic’s collection of Agent Skills examples, including document, PDF, presentation, and spreadsheet modules.
- **Key features**: Word document processing, PDF extraction and creation, presentation creation, and spreadsheet processing.
- **Use cases**: Organizing research materials, preparing reports and presentations, and working with tabular data.
- **Usage**: Select modules such as docx, pdf, pptx, or xlsx and configure the environment following their instructions. Check the licensing terms for document modules separately from other examples.
- **GitHub**: [anthropics/skills](https://github.com/anthropics/skills)

### interview-script · Interview Guides

- **Introduction**: A skill for creating structured user interview guides for product research.
- **Key features**: Warm-up questions, core follow-ups, and closing questions grounded in actual experiences and past behavior.
- **Use cases**: Preparing user interviews or outlining an initial academic interview guide.
- **Usage**: Provide the research goal, interview participants, and questions of interest. For academic research, adapt the guide to your research question and methodology; the original framework uses product research and JTBD approaches.
- **GitHub**: [phuryn/pm-skills · interview-script](https://github.com/phuryn/pm-skills/tree/main/pm-product-discovery/skills/interview-script)

### summarize-interview · Interview Summaries

- **Introduction**: A skill for turning interview transcripts into structured summaries.
- **Key features**: Extracting user needs, satisfaction signals, JTBD, and action items.
- **Use cases**: Organizing interview materials and reviewing their main points.
- **Usage**: Provide the original transcript and research context. Summaries can help organize materials; formal qualitative coding and thematic analysis are separate tasks.
- **GitHub**: [phuryn/pm-skills · summarize-interview](https://github.com/phuryn/pm-skills/tree/main/pm-product-discovery/skills/summarize-interview)

### sql-queries · SQL Queries

- **Introduction**: A skill that generates SQL from natural-language questions and database schemas.
- **Key features**: Reading schemas and generating queries for dialects including PostgreSQL, MySQL, and BigQuery.
- **Use cases**: Exploring databases, extracting research data, and preparing analytical reports.
- **Usage**: Provide the SQL dialect, schema, field definitions, and desired output. Check query conditions and results when running queries.
- **GitHub**: [phuryn/pm-skills · sql-queries](https://github.com/phuryn/pm-skills/tree/main/pm-data-analytics/skills/sql-queries)

### grammar-check · Text Proofreading

- **Introduction**: Checks grammar, logic, and flow, with targeted editing suggestions.
- **Key features**: Identifying grammatical errors, unclear wording, and gaps in the flow of an argument.
- **Use cases**: Proofreading paper drafts, research reports, and English abstracts.
- **Usage**: Submit the text with its purpose and intended readers. Verify citations and research conclusions against the original evidence.
- **GitHub**: [phuryn/pm-skills · grammar-check](https://github.com/phuryn/pm-skills/tree/main/pm-toolkit/skills/grammar-check)

## Portfolios and Design

Case studies, visual communication, game advertising concepts, and presentation materials.

### Oil UI · Interface Design

- **Introduction**: An AI interface design skill by Oil (Lin Zhihuang) for websites, apps, dashboards, and components. It translates product positioning and visual tone into typography, color, spacing, and layout decisions.
- **Key features**: Research visual references from comparable products; propose design directions; compare distinct alternatives side by side when requested; refine from feedback; recreate interfaces from screenshots; inspect actual desktop and mobile views.
- **Use cases**: Portfolio websites, product showcases, application interfaces, component design, and choosing a project’s visual direction.
- **Usage**: Install with `npx skills add oil-oil/oil-ui`, then provide project goals, brand assets, or reference screenshots. It recommends one direction by default, or compares several on request before implementation and refinement. GitHub hosts the open-source edition; Oil UI Pro is a separate paid version with its own feature set.
- **GitHub**: [oil-oil/oil-ui](https://github.com/oil-oil/oil-ui)

### Oil Motion · Interactive Web Animation

- **Introduction**: An interactive animation skill by Oil (Lin Zhihuang). It turns AI-generated or existing video and frame sequences into web animation driven by scrolling, pointers, dragging, touch, or device orientation.
- **Key features**: Plan motion and keyframes; generate continuous action; inspect and clean problematic frames; compress video or build atlases; arrange timelines; integrate interactions, mobile loading, and static fallbacks.
- **Use cases**: Animated portfolio showcases, product teardowns, character turns, camera fly-throughs, and continuous section transitions.
- **Usage**: Install with `npx skills add oil-oil/oil-motion` and describe the assets, motion goal, and control input. Local processing of existing assets requires Python 3.10+ and FFmpeg. AI image and video generation defaults to ZenMux, requires an API key, and incurs generation charges. Simple button feedback and standard interface transitions can be implemented directly with CSS, JavaScript, or similar tools.
- **GitHub**: [oil-oil/oil-motion](https://github.com/oil-oil/oil-motion)

### Anthropic Skills · Creative Work and Design

- **Introduction**: A collection of Agent Skills examples for creative work, art, design, and document creation.
- **Key features**: Examples of design and content creation skills, illustrating skill organization and production workflows.
- **Use cases**: Finding visual production methods, design references, and tools for presentation materials.
- **Usage**: Browse the creative and design modules, then check each skill’s required tools, dependencies, and licensing terms.
- **GitHub**: [anthropics/skills](https://github.com/anthropics/skills)

### ian-xiaohei-illustrations · Xiaohei Article Illustrations

- **Introduction**: A skill that turns ideas, processes, and metaphors in Chinese articles into hand-drawn explanatory illustrations.
- **Key features**: Extracting key ideas, designing visual metaphors, writing illustration prompts, and reviewing images; compositions use the Xiaohei character, white backgrounds, and a few colored annotations.
- **Use cases**: Supporting illustrations for articles, method explanations, and workflows.
- **Usage**: Provide the article and illustration placement. Identify the central idea, develop the visual expression, then generate and review the image.
- **GitHub**: [helloianneo/ian-xiaohei-illustrations](https://github.com/helloianneo/ian-xiaohei-illustrations)

### block-creative · Game Advertising Concepts

- **Introduction**: An advertising ideation and script review skill for Block, gravity-based, and casual puzzle games.
- **Key features**: Competitor creative analysis, concept variations, storyboards, segment-by-segment script review, and ad test design.
- **Use cases**: Developing game advertising case studies, analyzing competitor creatives, and revising storyboards.
- **Usage**: Provide videos, screenshots, or scripts and describe the task. Ground analysis in the supplied materials; evaluate advertising performance using actual data.
- **GitHub**: A personal local skill; no public repository link is provided.

### review-resume · Experience and Achievements

- **Introduction**: A resume review and job matching skill for product managers.
- **Key features**: Reviewing structure, achievement descriptions, keywords, and relevance to a role.
- **Use cases**: Organizing experience and personal contributions as source material for portfolio case studies.
- **Usage**: Provide a resume or experience summary, optionally with a target job description. Design processes and visual presentation for individual projects require separate work.
- **GitHub**: [phuryn/pm-skills · review-resume](https://github.com/phuryn/pm-skills/tree/main/pm-toolkit/skills/review-resume)

## English Reading

Writing practice and proofreading after reading in English.

### grammar-check · English Writing Feedback

- **Introduction**: A proofreading skill for summaries and writing exercises after English reading.
- **Key features**: Checking grammar, logic between sentences, and flow, with targeted revision suggestions.
- **Use cases**: Writing an English summary, retelling, or personal response after reading an article.
- **Usage**: Provide your English text and writing goal. Include the original article when checking whether the summary accurately reflects it.
- **GitHub**: [phuryn/pm-skills · grammar-check](https://github.com/phuryn/pm-skills/tree/main/pm-toolkit/skills/grammar-check)

## Business Observation

Product revenue, business models, customer acquisition, and growth case studies.

### How Profitable Startups Grow · BizPeel Revenue and Acquisition Directory

- **Introduction**: A directory of startup revenue bands, growth trends, categories, and acquisition leads, linked to BizPeel’s business research reports.
- **Key features**: Browse by revenue, growth, recent additions, and category; find founder or official accounts, growth questions, and research reports. The repository description dated 2026-11-05 lists 742 products and states that updates are weekly.
- **Use cases**: Exploring independent development ideas, researching competitors, and studying SEO, social media, and other acquisition channels.
- **Usage**: The GitHub directory is publicly readable. Browse the [English README](https://github.com/yihui-dev/how-profitable-startups-grow) or [BizPeel library](https://bizpeel.com/library) for more. Full reports involve unlocking or payment. Interpret revenue bands alongside their dates and sources; distinguish MRR from revenue over the last 30 days. Code is MIT-licensed; table content is copyrighted by BizPeel and requires attribution when quoted.
- **GitHub**: [yihui-dev/how-profitable-startups-grow](https://github.com/yihui-dev/how-profitable-startups-grow)

## About These Notes

Descriptions are compiled from project documentation and supplied materials. Refer to each original project for installation, dependencies, licensing, and pricing.

The organization takes inspiration from [Awesome Short Drama Skills](https://github.com/UnderleveledBuilder/awesome-short-drama-skills), with more practical projects added over time.
