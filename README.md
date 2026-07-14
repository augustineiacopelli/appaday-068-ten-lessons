# Ten Lessons

**AppADay — App #068**
Category: Educational (E) — AI-Powered
Date: 2026-07-14

Name any subject and Claude designs a ten-lesson path that carries you from first principles to real working proficiency. Each lesson is a selectable module that generates on demand, and your progress saves durably in the browser so you can stop and pick up anytime. Finish all ten to earn a Commencement certificate, collected on a Skills page.

## How It Works

1. Type what you want to learn and tap **Build my course**. Claude designs a ten-lesson syllabus in sequence — lesson one assumes no prior knowledge, lesson ten represents practical proficiency.
2. Tap any station on the path to open that lesson. Claude writes a focused teaching module (orientation, key ideas, a worked example, and a self-check) and caches it so reopening is instant.
3. Tap **Mark complete** to fill the station. The recommended-next lesson glows so you always know where you are.
4. Complete all ten lessons to trigger **Commencement** — a certificate conferring proficiency in your topic.
5. Every graduated course lands on the **Skills** page as a permanent credential.

## Durable Storage

Progress is stored in **IndexedDB**, not localStorage, so a full course library survives closing the tab and restarting the device, with room to spare for generated lesson content. One-tap **Export** downloads your entire library as a JSON file, and **Import** restores it — so a cleared browser or a new phone never costs you your work. If a browser blocks IndexedDB, the app falls back to in-memory storage for the session.

## Technical Details

- **AI Model:** Claude Sonnet 5 via the Anthropic API. Your API key is stored locally through the settings gear and used to call Claude directly from the browser; it is never committed or uploaded anywhere but Anthropic.
- **Storage:** IndexedDB primary store with JSON export/import backup and an in-memory fallback.
- **Lesson generation:** The syllabus is one structured JSON call; each lesson's content is generated on demand and cached, keeping calls small and reopened lessons instant and offline.
- **Rendering:** Lesson markdown is HTML-escaped before formatting, so model output can never inject markup.
- **No build step, no dependencies.** Single-file vanilla HTML/CSS/JS. Type set in Fraunces, Public Sans, and Space Mono.

## Part of AppADay

One complete, functional, mobile-friendly web app shipped every day.

[View all apps →](https://augustineiacopelli.github.io/appaday/)
