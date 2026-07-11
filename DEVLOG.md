# AI-Literate — Dev Log

A milestone tracker for the AI Aware project. One entry per completed step or feature.

---

## Feedback: shared Benjuicey Apps standard

Feedback follows the cross-app standard — see `benjuicey-apps/docs/feedback-standard.md` (the single source of truth). Submissions land in the one shared backend, stamped with this app's trigram **`LIT`**.

- **Mechanism:** this app has its own styled modal (`index.html`, "Got feedback?"), which POSTs the uniform schema (`appId: 'ai-literate'`, name, email, type, message) to the shared Worker (`benjuicey-feedback.benjuicemcjuice.workers.dev/submit`). Predates the shared widget; kept because it matches the app's design.
- **Categories** aligned to canonical `bug`/`content`/`request`/`general` on 2026-07-11 (was `hi`, now `general`).
- **Possible future tidy-up:** migrate to the shared `/widget.js` drop-in so there's one less bespoke form to maintain — optional, not required for compliance since the schema already matches.

---

## Milestones

### v1.2 — Renamed to AI-Literate (2026-05-21)
- Project renamed from AIAware → AI-Literate (AIAware is an existing company)
- Title, logo, hero, and footer updated in index.html
- GitHub repo renamed to BenjuiceMcJuice/ai-literate

### v1.1 — Renamed to AIrony (2026-05-08)
- Project renamed from AI Sense → AIrony across all files
- GitHub repo renamed to BenjuiceMcJuice/AIrony
- Local folder renamed to AIrony/

### v1.0 — Initial launch (2026-05-08)
- Single HTML file app built from the GenAI best practices guide PDF
- 11 sections covering GenAI basics, hallucinations, privacy, prompting, use cases
- Sticky header with progress bar
- Sidebar nav with active section highlighting
- Callout boxes (warning, tip, info), compare panels, step lists, chip tags
- Fully mobile responsive
- Deployed to Cloudflare Pages at aisense.pages.dev
- Source doc added as `docs/genai_guide.md`

---

## Backlog / Ideas

- **Interactive exercises section** — a new section (or standalone page) where readers work through practical scenarios before seeing a worked answer. Show/hide toggle, no backend needed. Proposed exercises:
  - *Fix the prompt* — given a vague/bad prompt, improve it, then reveal a better version with explanation (ties to S4)
  - *Spot the hallucination* — plausible AI response with a subtle error baked in; what would you check? (ties to S6)
  - *Break it down* — given a complex goal, sketch the steps before seeing a worked example (ties to S11)
  - *What not to share* — a realistic prompt with something the person shouldn't have included; spot it (ties to S7)
- Quiz / self-assessment at the end of the guide
- Dark mode toggle
- Shareable section links (anchor URLs)
- Print stylesheet
- Custom domain
