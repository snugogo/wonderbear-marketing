# WonderBear — Feature Highlights

*AI-Powered Children's Education for the Global Family*

---

## Core Features

### 1. AI Dialogue — Talk with a Smart Bear
Children aged 3–8 have a natural voice conversation with an AI bear that builds a personalized story around their ideas. The dialogue adapts to the child's age (5 rounds for 3–5 years, 7 rounds for 6–8 years), with **33-language support** for both voice input (Whisper ASR) and voice output (dual-engine TTS: DashScope CosyVoice + Azure Neural TTS).

### 2. AI Storybook Generation
From a short dialogue, WonderBear generates a complete **10-page illustrated storybook** with bilingual audio narration. The image pipeline uses Gemini 3 Pro for high-resolution cover art and FAL flux-pro for consistent interior illustrations. Each page has both native-language and English narration. The entire process is fully automated.

### 3. Bear Class — Systematic Literacy Curriculum
A structured reading and writing curriculum grounded in established educational standards:

- **Chinese**: 500 characters across 84 lessons — based on PEP (People's Education Press) Grade 1-2 character tables
- **English**: 200 words across 6 stages (20 lessons) — based on Jolly Phonics 42-phoneme system + Dolch Sight Words
- **13 additional languages**: Polish, Romanian, Russian, Spanish, German, French, Italian, Portuguese, Japanese, Korean, Thai, Vietnamese, Arabic

Each lesson follows a complete learning cycle: **Vocabulary Learning → Story Reading → Quiz Assessment**.

### 4. Story Library
Browse and discover AI-generated storybooks. Filter by language and category. Read with automatic page-by-page narration. Stories come from both personalized AI dialogue sessions and curated public collections.

### 5. Favorites & Downloads
Save favorite stories for quick access (synced across devices). Download complete books with images and audio for offline reading.

### 6. Multi-Child Profiles
Support for up to 4 children per device, each with independent learning progress, language preferences, and age-appropriate content (3-4, 5-6, 7-8 age brackets).

### 7. Multilingual Interface
The entire app UI is available in **33 languages** with real-time switching. Four core languages (Chinese, English, Polish, Romanian) have full translations.

### 8. Parental Controls
Device binding via QR code, password-protected parent dashboard, content safety filtering (input + output), usage limits, and multi-device family management.

---

## Technical Highlights

| Component | Technology |
|-----------|-----------|
| LLM | Gemini 2.5 Flash (dialogue + story generation) |
| Image Generation | Gemini 3 Pro → OpenAI → FAL (3-tier fallback) |
| Speech Recognition | DashScope Paraformer (Chinese) / OpenAI Whisper (other 32 languages) |
| Voice Synthesis | DashScope CosyVoice / Azure Neural TTS (33 languages) |
| Streaming TTS | Opus-encoded low-latency streaming pipeline |
| Storage | Cloudflare R2 (images: webp + HD PNG, audio: MP3) |
| Frontend | Vue 3 + TypeScript + Pinia |
| Backend | Node.js + PostgreSQL + Redis |
| Payment | Stripe (credit packages from $1.50) |
| Physical Books | Print-on-demand: 32-page paperback ($39.90) / 56-page hardcover ($59.90) |

---

## Language Coverage

| Domain | Languages |
|--------|-----------|
| UI / Interface | 33 languages (including zh, en, pl, ro, ja, de, es, ru, fr, it, pt, ar, ko, th, vi, hi and more) |
| AI Dialogue | 33 languages (voice input + TTS output) |
| Curriculum | 15 languages with structured literacy content |

---

*WonderBear — Where AI meets early childhood education.*
*Contact: partners@wonderbear.com*
