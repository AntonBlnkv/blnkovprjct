# StudioPilot (studiopilotmusic.com): AI copilot for Ableton Live, product reference as of Oct 2026

> **Method note (read first):** studiopilotmusic.com could NOT be fetched directly from this research environment. WebFetch returned DNS failure (`ENOTFOUND`) and curl got a proxy `403 CONNECT`. The same happened for youtube.com, maestralabs.com, studiopilot.tech and web.archive.org. Everything below comes from **web-search snippets/summaries of the vendor's own pages** (/, /app, /terms, /privacy, /stemsplitter, /free-presets) and a few third-party listings. Nearly all of it is vendor marketing copy. Exact wording may differ slightly from the live page, so treat any figure marked "conflicting" as unverified. Pages seen by search: https://www.studiopilotmusic.com/ , https://www.studiopilotmusic.com/app , https://www.studiopilotmusic.com/terms , https://www.studiopilotmusic.com/privacy , https://www.studiopilotmusic.com/stemsplitter , https://www.studiopilotmusic.com/free-presets

## 1. What is StudioPilot, who makes it, how does it connect to Ableton, and which AI does it use?

### Takeaway
StudioPilot is an AI control layer for Ableton Live sold in **two forms**:
- **Setup Kit:** a one-time purchase that connects your *own* Claude or Codex (ChatGPT) agent to Live through a small "bridge" (a control surface you enable in Live).
- **StudioPilot App:** a monthly subscription for a standalone macOS/Windows app with an unnamed AI built in.

The only identified person is "Danny" (danny@studiopilotmusic.com). No company name, launch date or explicit MCP/Remote Script documentation was found.

### Cited Findings
- StudioPilot lets an AI agent control Ableton Live through plain-language requests, for example starting playback, setting tempo and editing clips. — [studiopilotmusic.com](https://www.studiopilotmusic.com/)
- **Two products:**
  - (a) A standalone app "with the AI built in, no Claude or Codex needed", available "now on macOS and Windows", sold as a monthly subscription. — [StudioPilot App](https://www.studiopilotmusic.com/app); [Terms](https://www.studiopilotmusic.com/terms)
  - (b) A one-time **Setup Kit** that "connects your own AI assistant (Claude or Codex) to Ableton Live". You need your own paid AI plan, which is "separate from us and outside our control". — [Terms](https://www.studiopilotmusic.com/terms)
- **Connection mechanism:** "Ableton needs a small bridge so StudioPilot, Claude or Codex (ChatGPT) can send actions into Live." The setup folder includes "the right files and a guided connection test", but "the user may still need to enable the control surface inside Ableton". — [studiopilotmusic.com](https://www.studiopilotmusic.com/); [App](https://www.studiopilotmusic.com/app)
- **Setup Kit workflow:** you open the kit's setup folder with Claude or Codex (ChatGPT), and the agent guides the connection to Ableton. The kit is pitched at producers "who want Ableton control from Claude or Codex (ChatGPT) without figuring out the technical setup alone." — [studiopilotmusic.com](https://www.studiopilotmusic.com/)
- **App vs kit:** "The app sets up the Ableton bridge and runs a connection test for you; with the DIY kit you do the same steps yourself with your agent." — [App](https://www.studiopilotmusic.com/app)
- **YouTube:** the vendor's video describes the product as connecting an AI agent (Claude or Codex) directly to Ableton Live. Videos found: "What is StudioPilot? AI control for Ableton Live" (Short), "Control Ableton Live with AI agents (StudioPilot)", "I made a beat just by talking to AI (StudioPilot + Ableton)" and "AI is now your sound engineer inside Ableton" (Short). — [YouTube Short 7AqFlciw3zo](https://www.youtube.com/shorts/7AqFlciw3zo); [YouTube 7ZX5Ljl8n9M](https://www.youtube.com/watch?v=7ZX5Ljl8n9M); [YouTube 03oONd_sbDM](https://www.youtube.com/watch?v=03oONd_sbDM); [YouTube Short YL458AtRMRA](https://www.youtube.com/shorts/YL458AtRMRA)
- **AI model in the app:** the app page says the AI is "built in" and "tuned for music production" but does **not name the model**. — [App](https://www.studiopilotmusic.com/app)
- The privacy policy lists "an AI provider" among its processors, alongside Stripe, a database host and an email provider. The provider is not named in the snippets. — [Privacy](https://www.studiopilotmusic.com/privacy)
- **Maker/contact:** support and terms point to **danny@studiopilotmusic.com**. — [App](https://www.studiopilotmusic.com/app); [Terms](https://www.studiopilotmusic.com/terms)
- **Social:** TikTok account @studiopilotmusic. — [TikTok](https://www.tiktok.com/@studiopilotmusic)
- **Dates:** the Terms and Privacy Policy are dated **27 July 2026**. — [Terms](https://www.studiopilotmusic.com/terms); [Privacy](https://www.studiopilotmusic.com/privacy)
- **Third-party listing:** Maestra's comparison article ("AI for Ableton Live: MCP servers, Max for Live devices and apps") lists StudioPilot. A search summary of it gave the Setup Kit as a one-time founder price of EUR 29.99; this could not be fetched to verify. — [Maestra](https://maestralabs.com/learn/ai-for-ableton-live-options)

### Name collisions (do not confuse)
- **StudioPilot at studiopilot.tech** ("StudioPilot 2.0") is a different product: a browser-based AI music studio with an optional VST3/AU plugin for Ableton, Logic and FL.
  - Its site says it is by DCD development (Netherlands) and is "not affiliated with studiopilotmusic.com or any other product named StudioPilot".
  - Its compatibility page lists Ableton Live 11/12 (VST3). That requirement applies to *that* product, not this one. — [studiopilot.tech](https://www.studiopilot.tech/); [press](https://www.studiopilot.tech/press); [plugin](https://www.studiopilot.tech/plugin); [compatibility](https://www.studiopilot.tech/compatibility); [vst.studiopilot.tech](https://vst.studiopilot.tech/)
- **LivePilot (dreamrec/livepilot)** is an open-source MCP server for Ableton Live 12 with roughly 91–104 tools. — [mcpservers.org](https://mcpservers.org/servers/dreamrec/livepilot); [mcpmarket](https://mcpmarket.com/server/livepilot)
- **"Ableton Copilot"** is an MCP server built on ahujasid/ableton-mcp. — [glama](https://glama.ai/mcp/servers/nbpjfme3at); [mcpmarket](https://mcpmarket.com/server/ableton-copilot)
- **xiaolaa2/ableton-copilot-mcp** and **freekmurze/ableton-ai** are other open-source MCP projects (freekmurze/ableton-ai uses a remote script and needs Live 11+ and uv). None of them is StudioPilot. — [freekmurze/ableton-ai](https://github.com/freekmurze/ableton-ai)

### Inferences
- "Bridge" plus "enable the control surface inside Ableton" strongly suggests a **MIDI Remote Script** (Python control surface) installed into Live's Remote Scripts folder. It does not look like a Max for Live device. **Unverified.**
- The Setup Kit is driven "by your agent" (Claude Code / Codex reading a setup folder), which suggests an agent-side tool layer, likely an MCP server or a CLI/script set, that talks to that remote script over a local socket. This is the same pattern as ahujasid/ableton-mcp. **Unverified.** No source explicitly says "MCP" or "Claude Desktop".
- Because Codex (ChatGPT) is supported alongside Claude, the kit is probably agent-agnostic, built around coding-agent CLIs. Whether claude.ai / Claude Desktop (as opposed to Claude Code) works is **unconfirmed**.
- Pricing in £ and "Danny" suggest a UK-based solo developer or small team. **Unverified.**

### Gaps
- Legal entity, jurisdiction, founder full name and public launch date were not found. The earliest dated evidence is the Terms/Privacy dated 27 Jul 2026.
- Technical architecture: MCP vs custom protocol, remote script name, port and transport are not documented in any accessible snippet.
- Which LLM powers the subscription app is not named.
- Compatibility with Claude Desktop / claude.ai is not stated.
- There are no Product Hunt, KVR, Gearspace, Ableton forum or Reddit threads specifically about studiopilotmusic.com StudioPilot in the results.

## 2. Full feature list: what it can and cannot do in Live

### Takeaway
The vendor claims 200+ Ableton actions covering most areas of Live: transport, tracks, clips, MIDI, audio clips/warp, devices, scenes, arrangement, sends/returns, browser loading and recording. On top of that it advertises:
- MIDI/drum/bass generation
- a built-in audio analyser
- mix and master workflows (including LUFS and reference matching)
- third-party plugin control
- your-own-sample-folder loading
- a stem splitter

No explicit "cannot do" list was found.

### Cited Findings
- **Scope:** "200+ Ableton actions across clips, tracks, devices, MIDI, arrangement, mixing, and audio clip data." — [studiopilotmusic.com](https://www.studiopilotmusic.com/)
- **Controllable areas:** playback, tempo, tracks, clips, MIDI notes, audio clip pitch and gain, warp markers, devices, scenes, arrangement, sends, returns, browser loading, recording, "and more". — [studiopilotmusic.com](https://www.studiopilotmusic.com/) (via search summary)
- **Generation:** "Generate drum patterns, basslines, MIDI clips, scenes, and starting points without building every part manually." — [studiopilotmusic.com](https://www.studiopilotmusic.com/)
- **Audio analyser:** a "built-in audio analyser that reads the waveform and spectrogram of your loops: band energy, brightness, rhythmic density, and key". It is used to pick layers that don't clash. — [studiopilotmusic.com](https://www.studiopilotmusic.com/); [App](https://www.studiopilotmusic.com/app)
- **Mixing:** "Balance levels, pan for stereo width, send tops and percussion to reverb and delay, high-pass the lows out of your tops, and side-chain the bass under the kick." — [studiopilotmusic.com](https://www.studiopilotmusic.com/)
- **Mastering:** "Match the loudness and tone of any reference track, real EQ, glue compression, limiting and LUFS targeting on your master bus." — [studiopilotmusic.com](https://www.studiopilotmusic.com/)
- **Arrangement:** builds intros, builds, drops, breakdowns, variations, locators and arrangement passes. — [App](https://www.studiopilotmusic.com/app)
- **Third-party plugins:** claims it "drives your 3rd-party plugins (Serum, FabFilter…)". — [App](https://www.studiopilotmusic.com/app)
- **Your samples:** points at your own sample folder and pulls your sounds into the session. — [App](https://www.studiopilotmusic.com/app)
- **Sample packs:** the app can generate sample packs, which uses credits. Browsing or downloading packs does not use credits. — [App](https://www.studiopilotmusic.com/app)
- **Stem splitter** (also offered as a free web tool, "Split Any Song Into Stems + a Sample Pack"). It sends the chosen audio to a third-party separation service. — [Stem Splitter](https://www.studiopilotmusic.com/stemsplitter); [Privacy](https://www.studiopilotmusic.com/privacy)
- **Freebies:** free Ableton and Diva presets and free MIDI packs. — [Free presets](https://www.studiopilotmusic.com/free-presets); [studiopilotmusic.com](https://www.studiopilotmusic.com/)
- **Setup Kit contents:**
  - "Full feature masterclass"
  - "Guided Ableton setup & connection test"
  - "Premium template file"
  - "Producer command library"
  - "Free MIDI packs & presets"
  - the analyser, the mix and master workflow, and the app
  - a setup walkthrough and a troubleshooting vault
  - "Community & full support"
  — [studiopilotmusic.com](https://www.studiopilotmusic.com/)

### Inferences
- The listed actions (warp markers, clip gain/pitch, browser loading, sends/returns, recording) map closely onto what Live's Python Live Object Model API exposes. That fits the Remote Script inference.
- Automation-envelope writing is **not explicitly listed**.
- "Drives 3rd-party plugins" likely means setting exposed/configured device parameters via the LOM, not opening plugin GUIs. **Unverified.**
- The analyser features (spectrogram, key, band energy) imply audio files are analysed locally or by the app. Live's API cannot read audio samples, so this is done outside Live. **Inference.**

### Gaps
- No official "limitations" / "cannot do" list was found.
- It is unknown whether it writes automation, edits audio destructively, renders/exports or freezes tracks, works in Session vs Arrangement equally, or controls Max for Live devices.
- No independent reviews verify the marketing claims.

## 3. Setup, system requirements, licensing, credits and pricing

### Takeaway
Supported on macOS (Intel and Apple Silicon) and Windows with the same steps on both. The desktop app "needs a fairly new computer", and the kit "runs anywhere Ableton Live does". No minimum Live version or edition is published.

| Product | Price | What you get / need |
|---|---|---|
| Setup Kit | one-time "founder price"; shown as $34.99 and also as 24.99 GBP (conflicting) | Requires your own paid Claude or Codex plan |
| App, Starter | $27.99/mo | 2,000 credits, ~5–10 tracks/month |
| App, Pro | $54.99/mo | 8,000 credits, ~20–40 tracks/month |
| App, Studio | $88.99/mo | 20,000 credits, 50+ tracks/month |

The app is also advertised "from £19.99/mo" (conflicting). Credits reset monthly and don't roll over. No standard refunds.

### Cited Findings
- **Platforms:** the standalone app runs on macOS (Intel and Apple Silicon) and Windows. — [App](https://www.studiopilotmusic.com/app)
- **Setup steps** are the same on either OS. — [studiopilotmusic.com](https://www.studiopilotmusic.com/)
- **Hardware:** "desktop AI apps need a fairly new computer, but StudioPilot still works on older machines using an alternative setup". The app FAQ recommends the one-time Setup Kit for older machines that struggle with the app. — [studiopilotmusic.com](https://www.studiopilotmusic.com/); [App](https://www.studiopilotmusic.com/app)
- **Kit compatibility:** "The Setup Kit runs anywhere Ableton Live does." — [studiopilotmusic.com](https://www.studiopilotmusic.com/) (via search summary)
- **Live version and edition:** no Live version (11/12) or edition (Intro/Standard/Suite) requirement appears in any indexed page. Searches for these terms on the domain returned nothing. — [search of studiopilotmusic.com](https://www.studiopilotmusic.com/)
- **Install steps:**
  1. **Setup Kit:** open the setup folder with Claude or Codex; the agent installs the bridge files and runs a guided connection test. **App:** the app installs the bridge and runs the test itself.
  2. You may need to enable the control surface in Live's preferences once.
  — [studiopilotmusic.com](https://www.studiopilotmusic.com/); [App](https://www.studiopilotmusic.com/app)
- **Setup Kit price:** "one-time founder price" for the "analyser, mix and master workflow, command library, and app". Search summaries show **$34.99**, while the page's structured data shows **24.99 GBP**, and Maestra cites **EUR 29.99**. The amounts conflict and may be localised currency. — [studiopilotmusic.com](https://www.studiopilotmusic.com/); [Maestra](https://maestralabs.com/learn/ai-for-ableton-live-options)
- **App tiers (credits and estimated tracks):**
  - **Starter:** $27.99/mo, 2,000 AI credits, ~5–10 tracks/mo
  - **Pro:** $54.99/mo, 8,000 credits, ~20–40 tracks/mo
  - **Studio:** $88.99/mo, 20,000 credits, 50+ tracks/mo
  — [App](https://www.studiopilotmusic.com/app)
- **Conflicting app price:** the same site also says the app is "from £19.99 a month", and the homepage structured data lists GBP 19.99 as the low price. — [App](https://www.studiopilotmusic.com/app); [studiopilotmusic.com](https://www.studiopilotmusic.com/)
- **Credits:** they cover AI work (building, mixing, mastering, generating sample packs). Marketing says a full track uses only a small part of the allowance and you're "never cut off mid-track". — [App](https://www.studiopilotmusic.com/app)
- **Credit and subscription terms:**
  - Credits "reset at the start of each billing period and don't roll over".
  - Subscriptions renew monthly until cancelled.
  - You can upgrade, downgrade or cancel from the members area or inside the app, with pro-rated changes.
  - After cancelling, access lasts to the end of the paid period.
  — [Terms](https://www.studiopilotmusic.com/terms)
- **Refunds:** not offered as standard, since both products give immediate access to digital files. The terms say: "If something genuinely does not work for you, or you have been charged in error, email us and we will look at it properly". Liability is limited to the amount paid. — [Terms](https://www.studiopilotmusic.com/terms)
- **Payments** go through Stripe. — [Privacy](https://www.studiopilotmusic.com/privacy)

### Inferences
- Because the user bought the product, the actual invoice or checkout shows which product (Kit vs App) and currency apply. Pricing on the site appears to be geo-localised and/or changed over time, with founder pricing.
- On the Setup Kit path, the AI usage limits are those of the user's own Claude/Codex plan (e.g., Claude Pro/Max limits). StudioPilot credits apply only to the App.

### Gaps
- Minimum OS versions, Ableton Live version and edition, and RAM/CPU specs for "fairly new computer" are not published in accessible snippets.
- Whether the Setup Kit's "and app" bundle includes an App subscription period is unclear.
- Licence seat limits (number of machines) were not found.

## 4. Documentation, FAQ, tutorials, changelog, community and support

### Takeaway
There are no public docs site, changelog or release notes in search results. Documentation appears to be **bundled inside the paid Setup Kit** (masterclass, setup walkthrough, troubleshooting vault, command library) plus an FAQ on the /app page. Support is by email to Danny. Public tutorials are a handful of YouTube videos and TikTok clips.

### Cited Findings
- The homepage footer links only to Terms and Privacy. No docs, changelog or blog pages were indexed. — [Terms](https://www.studiopilotmusic.com/terms); [Privacy](https://www.studiopilotmusic.com/privacy)
- **Kit-bundled materials:** feature masterclass, setup walkthrough, troubleshooting vault, producer command library, "Community & full support". — [studiopilotmusic.com](https://www.studiopilotmusic.com/)
- **FAQ:** the /app page contains an FAQ, including the older-computers question. — [App](https://www.studiopilotmusic.com/app)
- **Support email:** danny@studiopilotmusic.com ("Email ... and we will answer"). — [Terms](https://www.studiopilotmusic.com/terms); [App](https://www.studiopilotmusic.com/app)
- **Video tutorials/demos:**
  - [Control Ableton Live with AI agents (StudioPilot)](https://www.youtube.com/watch?v=7ZX5Ljl8n9M)
  - [I made a beat just by talking to AI (StudioPilot + Ableton)](https://www.youtube.com/watch?v=03oONd_sbDM)
  - [What is StudioPilot?](https://www.youtube.com/shorts/7AqFlciw3zo)
  - [AI is now your sound engineer inside Ableton](https://www.youtube.com/shorts/YL458AtRMRA)
  - [TikTok @studiopilotmusic](https://www.tiktok.com/@studiopilotmusic)
- **Other free web tools/resources:** [Stem Splitter](https://www.studiopilotmusic.com/stemsplitter); [Free Ableton & Diva presets](https://www.studiopilotmusic.com/free-presets)

### Inferences
- "Community" is likely a private group (Discord/Skool or similar) accessed after purchase. **Unverified.** No public Discord link was found.

### Gaps
- No Discord or other community URL was found.
- No public changelog, versioning or release notes were found.
- No YouTube upload dates or channel name were obtained (YouTube could not be fetched).
- No Product Hunt, KVR, Gearspace, Ableton forum or Reddit coverage was found.

## 5. Privacy: does project data go to the cloud?

### Takeaway
The vendor states that audio, samples, project files and finished tracks **stay on your computer** and are not used for AI training. Data does leave the machine in these cases:
- **Stem splitting** uploads the chosen file to a third-party separation service.
- **AI requests** go to an AI provider: the unnamed app provider, or Anthropic/OpenAI on the Setup Kit path. These requests presumably include session state and text.
- **Purchases** send a hashed email to ad platforms.

### Cited Findings
- "Your audio files, samples, project files and finished tracks stay on your own computer". They are not used to train AI models. — [Privacy](https://www.studiopilotmusic.com/privacy)
- **Stem splitting exception:** the stem-split feature uploads the chosen audio file to "the specialist service that performs the stem split". That service reportedly doesn't use uploads for training or share them. — [Privacy](https://www.studiopilotmusic.com/privacy)
- **Processors listed:** Stripe (payments), a database host, an email provider and an AI provider. A hashed email is sent to ad platforms at purchase. — [Privacy](https://www.studiopilotmusic.com/privacy)
- **Ownership:** "Anything you create using StudioPilot belongs entirely to you". StudioPilot claims no ownership, royalties or rights. Rights in tracks you split or sample stay with their owners, and clearing them is the user's responsibility. — [Terms](https://www.studiopilotmusic.com/terms)
- The policy is dated 27 July 2026. — [Privacy](https://www.studiopilotmusic.com/privacy)

### Inferences
- On the Setup Kit path, prompts and Live session state (track names, device parameters, MIDI notes) read by Claude/Codex go to Anthropic/OpenAI under the user's own account terms, not StudioPilot's.
- In the App, they go to StudioPilot's unnamed "AI provider".
- Audio itself likely stays local unless analysed or stem-split remotely. Whether the App's analyser runs locally is **not stated**.

### Gaps
- The AI provider is not named.
- Retention periods and whether the app sends audio for analysis were not found.
- No telemetry details were found.
