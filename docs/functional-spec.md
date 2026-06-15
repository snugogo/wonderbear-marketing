# WonderBear — 功能说明书 / Product Feature Documentation

*WonderBear is an AI-powered children's education hardware product developed for the global market. The TV app delivers an interactive, screen-based learning experience designed for children aged 3–8, combining large language model (LLM) dialogue, AI-generated personalized storybooks, systematic literacy curriculum, and multilingual support across 33 languages.*

*WonderBear 是一款面向全球市场的 AI 儿童教育硬件产品。TV 端应用为 3-8 岁儿童提供基于屏幕的交互式学习体验，融合了大语言模型（LLM）对话、AI 生成的个性化绘本、系统化识字课程以及覆盖 33 种语言的多语言支持。*

---

## 目录 / Table of Contents

1. [AI 智能对话 / AI Dialogue](#1-ai-智能对话--ai-dialogue)
2. [绘本创建 / Storybook Creation](#2-绘本创建--storybook-creation)
3. [CLASS 教学课程 / Bear Class Curriculum](#3-class-教学课程--bear-class-curriculum)
4. [首页 / Home Screen](#4-首页--home-screen)
5. [故事馆 · 图书馆 / Story Library](#5-故事馆--图书馆--story-library)
6. [收藏功能 / Favorites](#6-收藏功能--favorites)
7. [下载功能 / Downloads](#7-下载功能--downloads)
8. [我的档案 / Profile & My Den](#8-我的档案--profile--my-den)
9. [设置 / Settings](#9-设置--settings)
10. [多语言支持总览 / Language Support Overview](#10-多语言支持总览--language-support-overview)
11. [设备激活 / Device Activation](#11-设备激活--device-activation)
12. [积分系统 / Credit System](#12-积分系统--credit-system)

---

## 1. AI 智能对话 / AI Dialogue

WonderBear 的 AI 对话功能是产品的核心体验。孩子通过语音或文字与一只可爱的小熊 AI 进行最多 7 轮互动对话，AI 根据孩子的回答逐步构建一个个性化的故事框架。对话结束后，系统自动生成故事大纲，随后进入绘本创建流程。对话过程全程支持 33 种语言，采用自适应对话策略，根据孩子年龄（3-5 岁 5 轮，6-8 岁 7 轮）动态调整对话轮次。

The AI dialogue feature is the core experience of WonderBear. Children interact with a cute bear AI through voice or text for up to 7 rounds of conversation. The AI progressively builds a personalized story framework based on the child's responses. After the conversation concludes, the system generates a story outline and proceeds to the storybook creation pipeline. The entire dialogue process supports 33 languages with adaptive conversation strategies based on the child's age (5 rounds for ages 3-5, 7 rounds for ages 6-8).

**截图**: `./screenshots/tv/dialogue/dialogue-zh.png`

**功能亮点 / Feature Highlights**:
- **多轮 AI 对话 / Multi-round AI Dialogue**: 3-8 岁孩子与 AI 小熊进行 5-7 轮自适应对答，年龄越小轮次越少。Children aged 3-8 engage in 5-7 rounds of adaptive conversation with the AI bear; younger children get fewer rounds.
- **语音交互 / Voice Interaction**: 集成 Whisper ASR 语音识别，支持 33 种语言的语音输入。Integrated Whisper ASR voice recognition supporting voice input in 33 languages.
- **实时 TTS / Real-time TTS**: Azure Neural TTS + DashScope CosyVoice 双引擎，语音合成自然流畅。Dual-engine TTS (Azure Neural TTS + DashScope CosyVoice) delivers natural, fluent voice synthesis.
- **自适应对话模式 / Adaptive Dialogue Mode**: LLM 自动检测孩子参与度，在"故事讲述者"和"加油鼓励者"模式间切换。The LLM automatically detects the child's engagement level and switches between "storyteller" and "cheerleader" modes.
- **故事大纲提取 / Story Outline Extraction**: 对话结束后 AI 自动提取主角、场景、冲突三要素并生成 3-5 段故事大纲。After dialogue, the AI automatically extracts protagonist, setting, and conflict, generating a 3-5 paragraph story outline.
- **内容安全 / Content Safety**: 输入输出双重安全过滤，保障儿童内容安全。Dual-layer content safety filtering ensures child-appropriate content.
- **流式 TTS / Streaming TTS**: 支持 Opus 编码流式 TTS 管线，端到端延迟极低。Supports Opus-encoded streaming TTS pipeline with ultra-low end-to-end latency.

**DPAD 操作说明 / DPAD Controls**:
| 按键 | 功能 |
|------|------|
| DPAD 上/下/左/右 | 导航界面元素 |
| OK/确定 | 确认选择 / 触发语音录制 |
| 返回/Back | 退出对话 / 返回上一级 |
| 语音键 (Voice Key) | 按下开始录音，松开结束并发送 |

---

## 2. 绘本创建 / Storybook Creation

基于 AI 对话生成的故事大纲，WonderBear 自动创建一本完整的 10 页个性化绘本。每本绘本包含封面 + 10 页内页内容，每页配有 AI 生成的图片和双语音频旁白（母语 + 英语）。图片采用多级生成管线（Gemini Nano Banana Pro → OpenAI → FAL），确保高质量输出。整套流程完全自动化，无需家长介入。

Based on the story outline generated from the AI dialogue, WonderBear automatically creates a complete 10-page personalized storybook. Each book includes a cover + 10 pages of content, with AI-generated illustrations and bilingual audio narration (native language + English). The image pipeline uses a multi-tier generation system (Gemini Nano Banana Pro → OpenAI → FAL) to ensure high-quality output. The entire process is fully automated without requiring parental intervention.

**截图**: `./screenshots/tv/create/create-zh.png`

**功能亮点 / Feature Highlights**:
- **AI 全自动生成 / Fully Automated Generation**: 对话结束 → LLM 写故事 → 生成图片 → TTS 配音 → 组装完成，全流程自动化。Dialogue complete → LLM writes story → generates images → TTS narration → assembly complete, fully automated pipeline.
- **10 页完整绘本 / 10-Page Complete Storybook**: 封面 + 10 页故事内容，每页含精美插图。Cover + 10 pages of story content, each with beautiful illustrations.
- **双语旁白 / Bilingual Narration**: 每页自动生成母语 + 英语双语音频旁白。Automatic bilingual audio narration (native language + English) for each page.
- **多管线图片 / Multi-Tier Image Generation**: Gemini Nano Banana Pro (2K) → OpenAI → FAL 三级管线，流畅降级确保生成成功。Three-tier pipeline: Gemini Nano Banana Pro (2K) → OpenAI → FAL, graceful degradation ensures successful generation.
- **生成进度实时跟踪 / Real-Time Progress Tracking**: 后台生成时可实时查看进度（LLM → 图片 → TTS → 组装）。Real-time progress tracking during background generation (LLM → Image → TTS → Assembly).
- **故事续写 / Story Sequel**: 支持基于现有绘本续写新故事。Supports generating new stories as sequels to existing books.
- **故事分享 / Story Sharing**: 生成后可分享给家人，支持打印实体书（32页平装 $39.90 / 56页精装 $59.90）。Share stories with family, support physical book printing (32-page paperback $39.90 / 56-page hardcover $59.90).

**DPAD 操作说明 / DPAD Controls**:
| 按键 | 功能 |
|------|------|
| DPAD 上/下/左/右 | 浏览绘本页面 |
| OK/确定 | 进入绘本阅读 / 查看大图 |
| 返回/Back | 退出绘本 / 返回创建界面 |

---

## 3. CLASS 教学课程 / Bear Class Curriculum

WonderBear CLASS 是一个系统化的识字与阅读学习课程。中文课程基于中国教育部人教版（PEP）小学 1-2 年级字表，含 500 个常用汉字、84 课；英文课程基于 Jolly Phonics 42 音素系统 + Dolch Sight Words，含 200 个核心词汇、6 个阶段 20 课；另有 13 种语言的课程内容。每课包含：词汇学习 → 故事阅读 → 小测验 三个环节。

WonderBear CLASS is a systematic literacy and reading curriculum. The Chinese curriculum is based on PEP (People's Education Press) Grade 1-2 character tables, containing 500 common Chinese characters across 84 lessons. The English curriculum is based on the Jolly Phonics 42-phoneme system + Dolch Sight Words, containing 200 core words across 6 stages (20 lessons). An additional 13 languages have curriculum content. Each lesson includes: vocabulary learning → story reading → quiz assessment.

**截图**: `./screenshots/tv/class/class-hub-zh.png`

**功能亮点 / Feature Highlights**:
- **中文 500 字课程 / Chinese 500-Character Curriculum**: 基于人教版标准，84 课逐步覆盖 500 个常用汉字。Based on PEP standards, 84 lessons progressively covering 500 common Chinese characters.
- **英文自然拼读 / English Phonics Curriculum**: Jolly Phonics 42 音素体系 + Dolch 高频词，6 阶段 200 词。Jolly Phonics 42-phoneme system + Dolch Sight Words, 6 stages, 200 words.
- **多语言课程 / Multi-Language Curriculum**: 支持 15 种语言的系统化识字课程。Systematic literacy curriculum supporting 15 languages.
- **三环节学习 / Three-Step Learning**: 每课包含识字 → 故事 → 测验完整闭环。Each lesson includes a complete cycle: character/word learning → story reading → quiz.
- **AI 共创故事 / AI Co-Create Story**: 每课结束后，基于刚学的 6 个字通过 AI 生成 5 页定制故事。After each lesson, generate a 5-page customized story via AI based on the 6 newly learned characters.
- **进度追踪 / Progress Tracking**: 跨设备同步学习进度。Cross-device learning progress synchronization.
- **学习积分 / Learning Rewards**: 完成课程获得积分奖励。Earn points for completing lessons.
- **透明图资源 / Tracing Resources**: 中文汉字提供描红图（miaohong）资源用于书写练习。Chinese characters include tracing (miaohong) images for writing practice.

**DPAD 操作说明 / DPAD Controls**:
| 按键 | 功能 |
|------|------|
| DPAD 上/下/左/右 | 选择课程 / 浏览内容 |
| OK/确定 | 进入课程 / 确认答案 |
| 返回/Back | 返回课程选择 / 退出当前环节 |

### 3a. 词汇学习 / Vocabulary Learning

每课包含 6 个汉字/单词的学习，展示字/词的书写、拼音/音素、例句和相关图片资源。

Each lesson covers 6 characters/words, displaying writing, pinyin/phonemes, example sentences, and related image resources.

**截图**: `./screenshots/tv/class/learn-char-zh.png`

### 3b. 课程故事 / Lesson Story

基于当前课学到的字/词编写的定制故事，在语境中巩固学习成果。

A custom story written using the characters/words from the current lesson, reinforcing learning through context.

**截图**: `./screenshots/tv/class/lesson-story-zh.png`

### 3c. 测验系统 / Quiz System

每课结束后的互动测验，测试孩子对所学字/词的掌握程度。支持选择题、正误判断等多种题型。

Interactive quiz at the end of each lesson, testing the child's mastery of learned characters/words. Supports multiple question types including multiple choice and true/false.

**截图**: `./screenshots/tv/class/lesson-quiz-zh.png`

---

## 4. 首页 / Home Screen

首页是 WonderBear TV 应用的导航中枢，采用大图标 + 文字标签的简洁布局设计，专为电视遥控器（DPAD）操作优化。孩子可以通过方向键轻松导航到 AI 对话、绘本创建、课程学习、故事馆等核心功能。首页还集成了快速开始入口和最近活动推荐。

The Home screen is the navigation hub of the WonderBear TV app, featuring a clean layout with large icons and text labels optimized for TV remote (DPAD) control. Children can easily navigate to core features including AI dialogue, storybook creation, curriculum learning, and story library. The home screen also integrates quick-start entry points and recent activity recommendations.

**截图**: `./screenshots/tv/home/home-zh.png`

**功能亮点 / Feature Highlights**:
- **大图标导航 / Large Icon Navigation**: 专为儿童设计的清晰大图标，易于识别。Clear, large icons designed for children, easy to recognize.
- **DPAD 全支持 / Full DPAD Support**: 方向键 + 确认键即可完成所有导航操作。All navigation achievable with directional keys + OK button.
- **快速入口 / Quick Access**: 直接从首页进入对话、课程继续上次进度。Direct access to dialogue and continuing lessons from the home screen.
- **活动推荐 / Activity Recommendations**: 展示最近的绘本和推荐内容。Display recent storybooks and recommended content.

**DPAD 操作说明 / DPAD Controls**:
| 按键 | 功能 |
|------|------|
| DPAD 上/下/左/右 | 在功能入口间导航 |
| OK/确定 | 进入选中的功能 |
| 返回/Back | 退出应用确认提示 |

---

## 5. 故事馆 · 图书馆 / Story Library

故事馆是浏览和发现 AI 生成绘本的集中地。孩子可以按语言或类别筛选故事列表，在线阅读带旁白朗读的绘本。故事来源包括 AI 对话生成的个性化绘本和公共库中的精选内容。

The Story Library is the central place for browsing and discovering AI-generated storybooks. Children can filter stories by language or category and read books online with narration. Stories come from both personalized AI dialogue-generated books and curated public library content.

**截图**: `./screenshots/tv/library/library-zh.png`

**功能亮点 / Feature Highlights**:
- **多维度筛选 / Multi-Dimensional Filtering**: 按语言、类别、排序方式浏览故事。Browse stories by language, category, and sort order.
- **在线朗读 / Online Reading**: 每页自动旁白朗读，支持翻页、暂停、双语模式。Automatic narration on each page with page turning, pause, and bilingual mode support.
- **公共图书馆 / Public Library**: 浏览所有公开分享的 AI 绘本。Browse all publicly shared AI-generated storybooks.
- **游标分页 / Cursor Pagination**: 大量故事数据流畅加载。Smooth loading for large story collections.

**DPAD 操作说明 / DPAD Controls**:
| 按键 | 功能 |
|------|------|
| DPAD 上/下 | 滚动故事列表 |
| DPAD 左/右 | 切换筛选类别 |
| OK/确定 | 进入故事详情 / 开始阅读 |
| 返回/Back | 返回首页 |

---

## 6. 收藏功能 / Favorites

收藏功能允许孩子将喜欢的绘本保存到收藏夹，方便随时回看。收藏状态与服务器同步，跨设备保持一致性。

The Favorites feature allows children to save their favorite storybooks for quick access. The favorite status syncs with the server, maintaining consistency across devices.

**截图**: `./screenshots/tv/favorites/favorites-zh.png`

**功能亮点 / Feature Highlights**:
- **一键收藏 / One-Click Favorites**: 在阅读或浏览时随时收藏故事。Favorite stories anytime while reading or browsing.
- **收藏列表管理 / Favorites List Management**: 集中查看和管理所有收藏故事。Centralized view and management of all favorited stories.
- **跨设备同步 / Cross-Device Sync**: 收藏状态与服务器实时同步。Favorites status syncs with the server in real time.
- **乐观更新 / Optimistic Updates**: 收藏操作即时反馈，网络失败时自动回滚。Instant feedback on favorite actions with automatic rollback on network failure.

**DPAD 操作说明 / DPAD Controls**:
| 按键 | 功能 |
|------|------|
| DPAD 上/下 | 滚动收藏列表 |
| OK/确定 | 进入故事阅读 |
| 返回/Back | 返回首页 |

---

## 7. 下载功能 / Downloads

下载功能支持将绘本离线保存到本地设备，即使在没有网络的环境下也能阅读。下载内容包括封面图片、内页图片和音频旁白。下载状态实时追踪，支持删除管理。

The Downloads feature enables offline storage of storybooks on the local device, allowing reading even without a network connection. Downloaded content includes cover images, page images, and audio narration. Download status is tracked in real time with delete management support.

**截图**: `./screenshots/tv/downloads/downloads-zh.png`

**功能亮点 / Feature Highlights**:
- **离线阅读 / Offline Reading**: 下载后无需网络即可阅读完整绘本。Read complete storybooks offline after download.
- **全量资源下载 / Full Resource Download**: 包含图片 + 音频的所有资源。Includes all resources: images + audio.
- **进度追踪 / Progress Tracking**: 实时显示下载进度和状态。Real-time display of download progress and status.
- **存储空间检测 / Storage Check**: 自动检测可用存储空间，确保下载可行。Automatically checks available storage space to ensure feasible downloads.
- **IndexedDB 存储 / IndexedDB Storage**: 使用浏览器 IndexedDB 高效存储离线资源。Efficiently stores offline resources using browser IndexedDB.

**DPAD 操作说明 / DPAD Controls**:
| 按键 | 功能 |
|------|------|
| DPAD 上/下 | 滚动下载列表 |
| OK/确定 | 开始下载 / 进入阅读 |
| 返回/Back | 返回首页 |

---

## 8. 我的档案 / Profile & My Den

我的档案是孩子个人中心，包含孩子档案管理、学习进度统计、积分系统等功能。支持多子女档案切换，每个孩子有独立的学习记录和偏好设置。本界面通过 TV 端过渡到 H5 页面实现更丰富的信息展示。

The Profile section is the child's personal center, including child profile management, learning progress statistics, and a points system. It supports multi-child profile switching, with each child having independent learning records and preference settings. This interface transitions from the TV app to H5 pages for richer information display.

**截图**: `./screenshots/tv/profile/profile-zh.png`

**功能亮点 / Feature Highlights**:
- **多子女管理 / Multi-Child Management**: 支持最多 4 个孩子档案，独立学习记录。Supports up to 4 child profiles with independent learning records.
- **年龄分段 / Age Bracketing**: 3-4 岁、5-6 岁、7-8 岁三档年龄适配内容。Three age brackets: 3-4, 5-6, and 7-8 years old.
- **学习进度统计 / Learning Progress Statistics**: 展示课程完成情况和绘本阅读记录。Display curriculum completion status and storybook reading records.
- **积分系统 / Points System**: 完成学习任务获得积分奖励。Earn points for completing learning tasks.
- **H5 扩展页面 / H5 Extension Pages**: 通过 H5 页面提供更丰富的设置和管理功能。Richer settings and management features through H5 extension pages.

**DPAD 操作说明 / DPAD Controls**:
| 按键 | 功能 |
|------|------|
| DPAD 上/下/左/右 | 在档案信息间导航 |
| OK/确定 | 进入详情 |
| 返回/Back | 返回首页 |

---

## 9. 设置 / Settings

设置界面提供应用级配置，包括 UI 语言切换（33 种）、对话语言设置、家长控制等功能。家长控制通过独立的 Web 管理界面完成，TV 端提供扫码绑定入口。

The Settings screen provides app-level configuration including UI language switching (33 languages), dialogue language settings, and parental controls. Parental controls are managed through a separate web interface, with the TV app providing a QR code binding entry point.

**截图**: `./screenshots/tv/settings/settings-zh.png`

**功能亮点 / Feature Highlights**:
- **33 种 UI 语言 / 33 UI Languages**: 应用界面支持 33 种语言实时切换。Real-time UI language switching across 33 languages.
- **对话语言设置 / Dialogue Language Settings**: 独立设置孩子对话使用的语言。Independently configure the child's dialogue language.
- **家长控制 / Parental Controls**: 通过 H5 后台管理设备绑定、内容权限、使用时间限制。Manage device binding, content permissions, and usage limits through the H5 admin panel.
- **设备信息 / Device Info**: 显示固件版本、设备 ID 等系统信息。Display firmware version, device ID, and other system information.

**DPAD 操作说明 / DPAD Controls**:
| 按键 | 功能 |
|------|------|
| DPAD 上/下 | 滚动设置项列表 |
| DPAD 左/右 | 调整设置值 / 切换选项 |
| OK/确定 | 确认设置变更 |
| 返回/Back | 返回首页 |

---

## 10. 多语言支持总览 / Language Support Overview

### UI 语言 / UI Languages (33)

WonderBear 的应用界面支持 33 种语言。4 种核心语言（zh/en/pl/ro）具有完整翻译，其余语言随社区和 OEM 需求持续完善。默认语言为简体中文。

The application UI supports 33 languages. 4 core languages (zh/en/pl/ro) have full translations, with others continuously improved based on community and OEM demand. The default language is Simplified Chinese.

| 代码 | 语言 | 翻译状态 | 代码 | 语言 | 翻译状态 |
|------|------|----------|------|------|----------|
| zh | 简体中文 | 完整 | hr | Hrvatski (克罗地亚语) | 基础 |
| en | English | 完整 | hu | Magyar (匈牙利语) | 基础 |
| pl | Polski (波兰语) | 完整 | id | Bahasa Indonesia | 基础 |
| ro | Română (罗马尼亚语) | 完整 | it | Italiano | 基础 |
| ja | 日本語 (日语) | 基础 | ko | 한국어 (韩语) | 基础 |
| de | Deutsch | 基础 | ms | Bahasa Melayu (马来语) | 基础 |
| es | Español | 基础 | nb | Norsk Bokmål (挪威语) | 基础 |
| ru | Русский (俄语) | 基础 | nl | Nederlands (荷兰语) | 基础 |
| ar | العربية (阿拉伯语) | 基础 | pt | Português | 基础 |
| bg | Български (保加利亚语) | 基础 | sk | Slovenčina (斯洛伐克语) | 基础 |
| cs | Čeština (捷克语) | 基础 | sl | Slovenščina (斯洛文尼亚语) | 基础 |
| da | Dansk (丹麦语) | 基础 | sv | Svenska (瑞典语) | 基础 |
| el | Ελληνικά (希腊语) | 基础 | th | ไทย (泰语) | 基础 |
| fi | Suomi (芬兰语) | 基础 | tr | Türkçe (土耳其语) | 基础 |
| fr | Français | 基础 | uk | Українська (乌克兰语) | 基础 |
| he | עברית (希伯来语) | 基础 | vi | Tiếng Việt (越南语) | 基础 |
| hi | हिन्दी (印地语) | 基础 | | | |

### 对话语言 / Dialogue Languages (33)

AI 对话支持全部 33 种语言，每种语言均配有对应的 Azure Neural TTS 语音。语言设置基于孩子档案中的 `primaryLang` 字段。

AI dialogue supports all 33 languages, each with a corresponding Azure Neural TTS voice. Language settings are based on the child profile's `primaryLang` field.

### 课程语言 / Curriculum Languages (15)

CLASS 教学课程支持 15 种语言的系统化识字内容：

| 语言 | 课程基础 | 内容量 |
|------|----------|--------|
| 中文 (zh) | 人教版小学 1-2 年级字表 | 500 字, 84 课 |
| English (en) | Jolly Phonics + Dolch Sight Words | 200 词, 6 阶段 20 课 |
| Polski (pl) | 音节教学法 (Sylabowa) | 完整课程 |
| Română (ro) | 基于英文课程结构本地化 | 完整课程 |
| Русский (ru) | 基于英文课程结构本地化 | 完整课程 |
| Español (es) | 基于英文课程结构本地化 | 完整课程 |
| Deutsch (de) | 基于英文课程结构本地化 | 完整课程 |
| Français (fr) | 基于英文课程结构本地化 | 完整课程 |
| Italiano (it) | 基于英文课程结构本地化 | 完整课程 |
| Português (pt) | 基于英文课程结构本地化 | 完整课程 |
| 日本語 (ja) | 基于英文课程结构本地化 | 完整课程 |
| 한국어 (ko) | 基于英文课程结构本地化 | 完整课程 |
| ไทย (th) | 基于英文课程结构本地化 | 完整课程 |
| Tiếng Việt (vi) | 基于英文课程结构本地化 | 完整课程 |
| العربية (ar) | 基于英文课程结构本地化 | 完整课程 |

---

## 11. 设备激活 / Device Activation

设备首次开机时进入激活流程：显示 6 位绑定码和二维码，家长通过手机扫描二维码或访问 H5 页面完成设备与家长账号的绑定。绑定后自动设置孩子档案并进入首页。支持跳过激活进入游客模式（有限免费体验）。

On first boot, the device enters the activation flow: displaying a 6-character bind code and QR code. Parents complete device-to-parent-account binding by scanning the QR code with their phone or visiting the H5 page. After binding, the child profile is automatically set up and the home screen is shown. Supports skipping activation for guest mode (limited free experience).

**截图**: `./screenshots/tv/activation/activation-zh.png`

**功能亮点 / Feature Highlights**:
- **扫码绑定 / QR Code Binding**: TV 端显示二维码，手机一扫即绑定。TV displays a QR code, instant binding by scanning with phone.
- **绑定码绑定 / Bind Code Binding**: 同时支持 6 位字母数字绑定码输入。Also supports 6-character alphanumeric bind code entry.
- **实时状态推送 / Real-Time Status Push**: 绑定成功后 TV 端即时响应，播放欢迎动画。Instant TV response on successful binding with welcome animation.
- **自动恢复 / Automatic Recovery**: 设备重启后自动恢复绑定状态，无需重新操作。Automatic binding state recovery after device reboot.
- **游客模式 / Guest Mode**: 跳过激活直接体验有限功能。Skip activation to experience limited features directly.
- **OEM 配置 / OEM Configuration**: 支持不同品牌的定制化激活体验。Supports customized activation experiences for different OEM brands.

**DPAD 操作说明 / DPAD Controls**:
| 按键 | 功能 |
|------|------|
| 返回/Back | 在开发模式下跳过激活 |

---

## 12. 积分系统 / Credit System

WonderBear 采用双池积分系统（设备积分 + 家长积分）。设备积分来自激活/绑定时的欢迎礼包，家长积分通过 Stripe 沙盒购买获取。每次 AI 绘本生成消耗 150 积分。积分不足时引导家长购买。

WonderBear uses a dual-pool credit system (device credits + parent credits). Device credits come from welcome gifts at activation/binding, while parent credits are purchased via Stripe sandbox. Each AI storybook generation costs 150 credits. Insufficient credits prompt parents to purchase more.

**功能亮点 / Feature Highlights**:
- **双池积分 / Dual-Pool Credits**: 设备积分优先消耗，不足时自动切换到家长积分。Device credits consumed first, automatically switches to parent credits when depleted.
- **欢迎礼包 / Welcome Gift**: 首次绑定设备获赠 150 默认积分。First-time device binding grants 150 default credits.
- **Stripe 购买 / Stripe Purchase**: 通过 Stripe 沙盒购买积分包。Purchase credit packages through Stripe sandbox.
- **积分包 / Credit Packages**: BOOK_1 (150 积分/$1.50), BOOK_10 (990 积分/$9.90)。BOOK_1 (150 credits/$1.50), BOOK_10 (990 credits/$9.90).
- **失败退款 / Failure Refund**: 故事生成失败自动退还 100 积分。Automatic 100-credit refund on story generation failure.

---

## 技术规格 / Technical Specifications

### AI 模型栈 / AI Model Stack
| 组件 | 主要服务 | 备用服务 |
|------|---------|---------|
| LLM 对话 | Gemini 2.5 Flash | — |
| LLM 故事生成 | Gemini 2.5 Flash (thinkingBudget 1024) | OpenAI gpt-4o-mini |
| 图片生成（封面） | Gemini 3 Pro (Nano Banana Pro) → OpenAI gpt-image-1.5 | FAL flux/dev |
| 图片生成（内页） | FAL flux-pro/kontext → Gemini 2.5 Flash | OpenAI gpt-image-1.5 |
| 语音合成 (TTS) | DashScope CosyVoice | Azure Neural TTS |
| 语音识别 (ASR) | DashScope Paraformer (中文) / OpenAI Whisper | — |
| 图片存储 | Cloudflare R2 (webp + HD PNG) | — |
| 音频存储 | Cloudflare R2 (MP3) | — |

### 前端技术 / Frontend Stack
| 组件 | 技术 |
|------|------|
| 框架 | Vue 3 (Composition API) + TypeScript |
| 状态管理 | Pinia |
| 国际化 | vue-i18n (33 种语言) |
| 导航 | 自定义 Screen Manager（无 Vue Router） |
| 焦点管理 | 自定义 DPAD Focus System |
| 通信桥梁 | JSBridge（WonderBear Android APK） |
| 音频流 | Web Audio API (PCM) / Opus 原生解码 |

### 后端技术 / Backend Stack
| 组件 | 技术 |
|------|------|
| 运行环境 | Node.js |
| 数据库 | PostgreSQL (via Prisma ORM) |
| 缓存 | Redis |
| 队列 | 进程内 FIFO 队列（含年费用户优先通道） |
| 认证 | JWT (Device Token + Parent Token) |
| 支付 | Stripe 沙盒 |
| 部署 | Docker |

---

*Document version: 1.0 — Generated from source code analysis, 2026-06-15*
