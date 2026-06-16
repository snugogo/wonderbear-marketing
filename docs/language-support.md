# WonderBear 支持语言一览（2026-06-16）

## 能力与口径

- **ASR 语音识别**：OpenAI `gpt-4o-transcribe`。OpenAI 把 whisper-1 / gpt-4o-transcribe / gpt-4o-mini-transcribe 的支持语言归为**同一张列表（~98 种）**；gpt-4o-transcribe 语种相同、识别更准。
- **TTS 语音合成**：Azure 神经语音（140+ 语言 / 500+ 音色），统一**年轻女性**音色（旁白）+ 童声（对话）。
- **可用语言 = ASR 支持 ∩ Azure 有女声 = 75 种**。其中 **33 种已在后端接好**，**42 种为"加一行声音映射即可启用"**。另有 22 种 ASR 支持但 Azure 无女声，暂不能上 TTS。
- **CLASS 识字 + QUIZ**：需逐语言预建课程，目前 **15 种**具备；其余为 Story/对话线。

## 语言选择机制

- **默认**：用户在 **H5 注册表**选语言 → 写入设备 `primaryLang` → 决定该设备 **ASR 识别语言 + TTS 音色**（不改 App UI）。
- **覆盖**：用户在**设备上手动切 UI 语言**时，ASR/TTS 改以**当前 UI 语言**为准。

---

## A. 可用语言表（75 种，按英文名排序）

> Story+对话 = ASR + TTS；CLASS = 识字课堂+QUIZ。voice ID 逐字取自 Azure 官方语音列表。

| 语言 | Language | ISO | Azure 女声 | Story+对话 | CLASS+QUIZ | 状态 |
|---|---|---|---|:---:|:---:|---|
| 南非荷兰语 | Afrikaans | af | af-ZA-AdriNeural | ✅ | ➖ | 新增 |
| 阿尔巴尼亚语 | Albanian | sq | sq-AL-AnilaNeural | ✅ | ➖ | 新增 |
| 阿姆哈拉语 | Amharic | am | am-ET-MekdesNeural | ✅ | ➖ | 新增 |
| 阿拉伯语 | Arabic | ar | ar-SA-ZariyahNeural | ✅ | ✅ | 已配 |
| 亚美尼亚语 | Armenian | hy | hy-AM-AnahitNeural | ✅ | ➖ | 新增 |
| 阿萨姆语 | Assamese | as | as-IN-YashicaNeural | ✅ | ➖ | 新增 |
| 阿塞拜疆语 | Azerbaijani | az | az-AZ-BanuNeural | ✅ | ➖ | 新增 |
| 巴斯克语 | Basque | eu | eu-ES-AinhoaNeural | ✅ | ➖ | 新增 |
| 孟加拉语 | Bengali | bn | bn-IN-TanishaaNeural | ✅ | ➖ | 新增 |
| 波斯尼亚语 | Bosnian | bs | bs-BA-VesnaNeural | ✅ | ➖ | 新增 |
| 保加利亚语 | Bulgarian | bg | bg-BG-KalinaNeural | ✅ | ➖ | 已配 |
| 缅甸语 | Burmese | my | my-MM-NilarNeural | ✅ | ➖ | 新增 |
| 加泰罗尼亚语 | Catalan | ca | ca-ES-JoanaNeural | ✅ | ➖ | 新增 |
| 中文 | Chinese | zh | zh-CN-XiaoxiaoNeural | ✅ | ✅ 识字 | 已配 |
| 克罗地亚语 | Croatian | hr | hr-HR-GabrijelaNeural | ✅ | ➖ | 已配 |
| 捷克语 | Czech | cs | cs-CZ-VlastaNeural | ✅ | ➖ | 已配 |
| 丹麦语 | Danish | da | da-DK-ChristelNeural | ✅ | ➖ | 已配 |
| 荷兰语 | Dutch | nl | nl-NL-FennaNeural | ✅ | ➖ | 已配 |
| 英语 | English | en | en-US-JennyNeural | ✅ | ✅ | 已配 |
| 爱沙尼亚语 | Estonian | et | et-EE-AnuNeural | ✅ | ➖ | 新增 |
| 波斯语 | Persian | fa | fa-IR-DilaraNeural | ✅ | ➖ | 新增 |
| 菲律宾语 | Filipino | tl | fil-PH-BlessicaNeural | ✅ | ➖ | 新增 |
| 芬兰语 | Finnish | fi | fi-FI-SelmaNeural | ✅ | ➖ | 已配 |
| 法语 | French | fr | fr-FR-DeniseNeural | ✅ | ✅ | 已配 |
| 加利西亚语 | Galician | gl | gl-ES-SabelaNeural | ✅ | ➖ | 新增 |
| 格鲁吉亚语 | Georgian | ka | ka-GE-EkaNeural | ✅ | ➖ | 新增 |
| 德语 | German | de | de-DE-KatjaNeural | ✅ | ✅ | 已配 |
| 希腊语 | Greek | el | el-GR-AthinaNeural | ✅ | ➖ | 已配 |
| 古吉拉特语 | Gujarati | gu | gu-IN-DhwaniNeural | ✅ | ➖ | 新增 |
| 希伯来语 | Hebrew | he | he-IL-HilaNeural | ✅ | ➖ | 已配 |
| 印地语 | Hindi | hi | hi-IN-SwaraNeural | ✅ | ➖ | 已配 |
| 匈牙利语 | Hungarian | hu | hu-HU-NoemiNeural | ✅ | ➖ | 已配 |
| 冰岛语 | Icelandic | is | is-IS-GudrunNeural | ✅ | ➖ | 新增 |
| 印尼语 | Indonesian | id | id-ID-GadisNeural | ✅ | ➖ | 已配 |
| 意大利语 | Italian | it | it-IT-ElsaNeural | ✅ | ✅ | 已配 |
| 日语 | Japanese | ja | ja-JP-NanamiNeural | ✅ | ✅ | 已配 |
| 爪哇语 | Javanese | jv | jv-ID-SitiNeural | ✅ | ➖ | 新增 |
| 卡纳达语 | Kannada | kn | kn-IN-SapnaNeural | ✅ | ➖ | 新增 |
| 哈萨克语 | Kazakh | kk | kk-KZ-AigulNeural | ✅ | ➖ | 新增 |
| 高棉语 | Khmer | km | km-KH-SreymomNeural | ✅ | ➖ | 新增 |
| 韩语 | Korean | ko | ko-KR-SunHiNeural | ✅ | ✅ | 已配 |
| 老挝语 | Lao | lo | lo-LA-KeomanyNeural | ✅ | ➖ | 新增 |
| 拉脱维亚语 | Latvian | lv | lv-LV-EveritaNeural | ✅ | ➖ | 新增 |
| 立陶宛语 | Lithuanian | lt | lt-LT-OnaNeural | ✅ | ➖ | 新增 |
| 马其顿语 | Macedonian | mk | mk-MK-MarijaNeural | ✅ | ➖ | 新增 |
| 马来语 | Malay | ms | ms-MY-YasminNeural | ✅ | ➖ | 已配 |
| 马拉雅拉姆语 | Malayalam | ml | ml-IN-SobhanaNeural | ✅ | ➖ | 新增 |
| 马耳他语 | Maltese | mt | mt-MT-GraceNeural | ✅ | ➖ | 新增 |
| 马拉地语 | Marathi | mr | mr-IN-AarohiNeural | ✅ | ➖ | 新增 |
| 蒙古语 | Mongolian | mn | mn-MN-YesuiNeural | ✅ | ➖ | 新增 |
| 尼泊尔语 | Nepali | ne | ne-NP-HemkalaNeural | ✅ | ➖ | 新增 |
| 挪威语 | Norwegian | nb | nb-NO-PernilleNeural | ✅ | ➖ | 已配 |
| 普什图语 | Pashto | ps | ps-AF-LatifaNeural | ✅ | ➖ | 新增 |
| 旁遮普语 | Punjabi | pa | pa-IN-VaaniNeural | ✅ | ➖ | 新增 |
| 波兰语 | Polish | pl | pl-PL-AgnieszkaNeural | ✅ | ✅ | 已配 |
| 葡萄牙语 | Portuguese | pt | pt-BR-FranciscaNeural | ✅ | ✅ | 已配 |
| 罗马尼亚语 | Romanian | ro | ro-RO-AlinaNeural | ✅ | ✅ | 已配 |
| 俄语 | Russian | ru | ru-RU-SvetlanaNeural | ✅ | ✅ | 已配 |
| 塞尔维亚语 | Serbian | sr | sr-RS-SophieNeural | ✅ | ➖ | 新增 |
| 僧伽罗语 | Sinhala | si | si-LK-ThiliniNeural | ✅ | ➖ | 新增 |
| 斯洛伐克语 | Slovak | sk | sk-SK-ViktoriaNeural | ✅ | ➖ | 已配 |
| 斯洛文尼亚语 | Slovenian | sl | sl-SI-PetraNeural | ✅ | ➖ | 已配 |
| 索马里语 | Somali | so | so-SO-UbaxNeural | ✅ | ➖ | 新增 |
| 西班牙语 | Spanish | es | es-ES-ElviraNeural | ✅ | ✅ | 已配 |
| 巽他语 | Sundanese | su | su-ID-TutiNeural | ✅ | ➖ | 新增 |
| 斯瓦希里语 | Swahili | sw | sw-KE-ZuriNeural | ✅ | ➖ | 新增 |
| 瑞典语 | Swedish | sv | sv-SE-SofieNeural | ✅ | ➖ | 已配 |
| 泰米尔语 | Tamil | ta | ta-IN-PallaviNeural | ✅ | ➖ | 新增 |
| 泰卢固语 | Telugu | te | te-IN-ShrutiNeural | ✅ | ➖ | 新增 |
| 泰语 | Thai | th | th-TH-PremwadeeNeural | ✅ | ✅ | 已配 |
| 土耳其语 | Turkish | tr | tr-TR-EmelNeural | ✅ | ➖ | 已配 |
| 乌克兰语 | Ukrainian | uk | uk-UA-PolinaNeural | ✅ | ➖ | 已配 |
| 乌尔都语 | Urdu | ur | ur-PK-UzmaNeural | ✅ | ➖ | 新增 |
| 乌兹别克语 | Uzbek | uz | uz-UZ-MadinaNeural | ✅ | ➖ | 新增 |
| 越南语 | Vietnamese | vi | vi-VN-HoaiMyNeural | ✅ | ✅ | 已配 |
| 威尔士语 | Welsh | cy | cy-GB-NiaNeural | ✅ | ➖ | 新增 |

**合计 75 种**：33 已配 + 42 新增（加一行声音映射即可启用）。CLASS+QUIZ 共 15 种：zh, en, es, de, fr, it, pt, ja, ko, th, vi, ar, pl, ro, ru。

---

## B. ASR 支持但 Azure 无女声（22 种，暂不能上 TTS）

ba 巴什基尔, be 白俄罗斯, bo 藏语, br 布列塔尼, fo 法罗, ha 豪萨, ht 海地克里奥尔, la 拉丁, lb 卢森堡, ln 林加拉, mg 马达加斯加, mi 毛利, nn 新挪威, oc 奥克, sa 梵语, sd 信德, sn 绍纳, tg 塔吉克, tk 土库曼, tt 鞑靼, yi 意第绪, yo 约鲁巴

---

## 备注

- voice ID 逐字取自 Azure 官方 TTS 语言列表；多地区取主流地区（ar→沙特, es→西班牙, pt→巴西, en→美式, zh→普通话）。如需调整地区（如葡语改欧洲 `pt-PT-RaquelNeural`、孟加拉改 `bn-BD-NabanitaNeural`），改对应一行即可。
- 启用"新增"语言：在后端 `server-v7/src/services/tts.js` 的 `narrationVoiceId/dialogueVoiceId` 映射 + 注册白名单各加一行；ASR 已按 `primaryLang` 自动传 language，无需改。
- CLASS/QUIZ 扩语言需另建识字课程（词表+句子+词图+词音+语音UI），成本高，按市场优先级补。
