# Learning Materials on AI in Ableton Live Production (EN/RU), as of October 2026

Method note: these notes come from 23 web searches and a few fetches, done on 2026-10-18. Several fetches failed with DNS errors (gearnews.com, mcp.directory, push-music.ru, abletonprohelp.ru). For those pages the details come from search snippets and could not be checked against the full page. They are marked "(snippet only)". Searches returned YouTube titles but not channel names, so channels are attributed only where a source names them.

## 1. YouTube creators and videos on AI + Ableton

### Takeaway
Most AI + Ableton video content from 2025-2026 comes from smaller creators. The main topics are hands-on MCP demos (Claude controlling Live) and "ChatGPT writes MIDI or scripts" tutorials. The big production channels (Andrew Huang, Venus Theory, You Suck at Producing, Mr. Bill) have no AI-workflow tutorials from 2024-2026 that I could find.

### Cited Findings
**Claude/LLM + Ableton MCP demos (EN, 2025-2026):**
- "Ableton MCP Demo: Creating a lush 80s synthwave track": Claude creates tracks and adds instruments and effects in Live through MCP (EN) — [YouTube](https://www.youtube.com/watch?v=VH9g66e42XA)
- "AI controls my ABLETON LIVE Project, AbletonMCP installation Tutorial and Testing": an install walkthrough (EN) — [YouTube](https://www.youtube.com/watch?v=QXSImhfS15k)
- "Claude AI & MCPs Music Production in ABLETON LIVE" (EN) — [YouTube](https://www.youtube.com/watch?v=pnOPZsRuRPY)
- "Using Claude + Ableton MCP to generate MIDI tracks: Psychedelic Lounge Music" (EN) — [YouTube](https://www.youtube.com/watch?v=zpqF-94MVxg)
- "Ableton and Claude integration using OSC and MCP" (EN) — [YouTube](https://www.youtube.com/watch?v=M28OsWDEgyA)
- "KI Co-Pilot in Ableton: was mit Claude Code und MCP heute schon geht" (DE) and a matching DE Short — [YouTube](https://www.youtube.com/watch?v=mw8n5e1ydFM), [Short](https://www.youtube.com/shorts/VDmujAGm1g8)
- "Cómo conectar Claude AI a Ableton Live 12 – Sin saber programación" (ES) — [YouTube](https://www.youtube.com/watch?v=xwL7bZZJ7Xc)

**ChatGPT → MIDI/scripts (EN):**
- "ChatGPT Writes COMPLEX Melodies with PYTHON?! (MIDI into Ableton)": ChatGPT writes Python that outputs MIDI, which is then imported into Live — [YouTube](https://www.youtube.com/watch?v=q7leDrXdAII)
- "Make An Ableton MIDI Controller Script With Chat GPT… In Under 8 Minutes!" — [YouTube](https://www.youtube.com/watch?v=g6STQOh91kc)

**Big creators (AI-specific content is limited or old):**
- You Suck at Producing: "I Turned Myself Into An AI That Finishes Music!" (#73) aired 18 July 2022, so it predates the 2024-2026 window — [TheTVDB](https://thetvdb.com/series/you-suck-at-producing/episodes/9897686)
- Venus Theory has commentary videos on AI's effect on musicians (for example a 2022 video on AI and creative professionals). These are not AI-in-Ableton tutorials — [TheTVDB](https://thetvdb.com/series/venus-theory/seasons/official/2024)
- Andrew Huang: Ableton blog feature on his experimental production techniques (not AI) — [Ableton blog](https://www.ableton.com/en/blog/andrew-huang-experimental-production-techniques/). He also made a brainwave-controlled synth video with Maylee Todd (MindMonitor → Ableton), which is adjacent to ML/biosignal control but is not generative AI — [MusicTech](https://musictech.com/news/andrew-huang-maylee-todd-manipulate-synths-with-brainwaves/)
- Ableton's own YouTube: Ableton says the free "Building Max Devices" pack (not AI) has video walkthroughs on the Ableton YouTube channel. It is a useful base before generating M4L devices with LLMs — [Ableton Packs](https://www.ableton.com/en/packs/building-max-devices)

**Ableton Loop / conference talks:**
- I found no Loop 2025 talk focused on AI. Google's Magenta Studio (free ML MIDI devices for Live) was first shown at Ableton Loop in Los Angeles. That is older history (2019) but still the canonical "AI devices in Live" reference — [Electronic Beats](https://electronicbeats.net/the-feed/you-can-now-use-open-source-machine-learning-tools-in-your-ableton-sessions); [Google Research paper](https://research.google/pubs/pub48280)

### Inferences
- The most practical "AI in Ableton" video content in 2025-2026 is MCP demos made by individual creators, often in German or Spanish as well as English. Expect varied quality. Prefer videos dated after the April 2026 Claude connector launch.
- Ableton has run no "AI" tutorial series of its own that I could find. Ableton's AI-related material is feature documentation (Stem Separation, Sound Similarity, MIDI Generators).

### Gaps
- Channel names for the MCP demo videos were not visible in search results.
- I found no AI-specific videos from Mr. Bill (2024-2026). This is unverified, not a confirmed absence.
- I could not find a recorded Loop 2025 or 2026 session list.

## 2. Official Ableton resources and the Claude connector

### Takeaway
Ableton's own AI features are Stem Separation (Live 12.3, Nov 2025, powered by Music AI/Moises), Splice integration with "Search with Sound", Sound Similarity Search and the MIDI Generators. Since 28 April 2026 there has also been an official Claude connector. It is a documentation assistant built on the Live and Push manuals. It does not control the DAW. Direct control still needs community MCP servers.

### Cited Findings
- Live 12.3 is a free update for Live 12 users. Stem Separation (Suite only) splits audio into vocals, drums, bass and other, in High Quality or High Speed modes. It runs locally on algorithms from Music AI (makers of Moises) — [MusicTech](https://musictech.com/news/music/ableton-live-12-3/); [Mixdown](https://mixdownmag.com.au/news/ableton-live-12-3-drops-overnight-with-stem-separation-and-splice-integration/)
- Official Ableton page: "Stem separation in Ableton Live". Right-click a clip and choose "Separate Stems to New Audio Tracks" (EN) — [Ableton](https://www.ableton.com/en/stem-separation-in-ableton-live/)
- Splice appears inside Live's browser. "Search with Sound" finds rhythmically and harmonically compatible samples from a dragged-in clip. The public beta started in Sept 2025 — [MusicTech beta](https://musictech.com/news/gear/ableton-live-12-3-public-beta/); [Attack Magazine](https://www.attackmagazine.com/news/splice-integration-and-stem-seperation-arrive-in-ableton-live-12-3-beta/)
- Dubspot blog walkthrough of the Live 12.3 update (EN) — [Dubspot](https://blog.dubspot.com/ableton-live-12-3-update)
- Sound Similarity Search uses a neural network that analyses timbre to find similar samples — [matthewess.com guide](https://matthewess.com/?p=5984)
- Ableton advertised a Senior Machine Learning Research Engineer role to expand its ML capabilities — [Ableton Jobs](https://www.ableton.com/en/jobs/apply/2286113). RU coverage says Ableton is looking for "ways to introduce AI-based features" — [SAMESOUND (RU)](https://samesound.ru/soft/179558-razrabotchiki-ableton-live-ishhut-sposoby-vnedreniya-funkcij-na-osnove-iskusstvennogo-intellekta-v-programmu)
- Anthropic released 9 creative connectors on 28 April 2026, with Adobe, Autodesk, Blender, Ableton and Splice as launch partners. The Ableton connector grounds Claude's answers in the Live and Push documentation and is docs-only, with no session control — [Unite.AI](https://www.unite.ai/anthropic-wires-claude-into-photoshop-blender-and-ableton/); [Mixmag MENA](https://mixmagmena.com/read/claude-is-now-integrated-into-ableton-live-and-splice-through-anthropic-s-new-connectors-tech); [findskill.ai walkthrough](https://findskill.ai/blog/anthropic-claude-ableton-connector-music-producer-honest-walkthrough/); [GearNews (snippet only)](https://www.gearnews.com/claude-ai-ableton-live-tech/)
- One blog says the connectors are available on all Claude plans, including free. This is secondary and unverified against Anthropic's help pages — [buildfastwithai](https://www.buildfastwithai.com/blogs/claude-connectors-creative-tools-2026)
- A Japanese essay on how DTM changes with "Claude x Ableton" (JP) — [note.com](https://note.com/kingtiptoe/n/naedd720da304?hl=en)

### Inferences
- For learners, the official connector is effectively an "AI manual tutor" (how do I do X in Live 12). Composition and session automation still happen through MCP or Max for Live.

### Gaps
- I could not reach the primary Anthropic or Ableton announcement pages. All connector details are from secondary press.
- Ableton Learn (learningmusic.ableton.com, Learning Synths) has no AI-specific module that I could find.

## 3. Hands-on guides: LLM control of Live (MCP) and Max for Live with AI

### Takeaway
The main written guides are GitHub READMEs and 2026 blog guides for Ableton MCP servers (ahujasid/ableton-mcp is the original), plus tools that generate Max for Live devices from prompts (ChatDSP, MaxPy Studio).

### Cited Findings
- ahujasid/ableton-mcp is the original open-source project (MIT) by Siddharth Ahuja. It has two parts: a Remote Script inside Live and a Python MCP server launched by Claude Desktop or Cursor (`uvx ableton-mcp`, which needs uv and Python 3.8+). Its features include arrangement-view composition — [GitHub](https://github.com/ahujasid/ableton-mcp); [README mirror](https://cdn.jsdelivr.net/gh/ahujasid/ableton-mcp@main/README.md)
- Setup gotchas: copy the Remote Script into the MIDI Remote Scripts folder and select it as a Control Surface. Run only one client (Claude Desktop or Cursor), because two MCP servers compete for the same socket — [README mirror](https://cdn.jsdelivr.net/gh/ahujasid/ableton-mcp@main/README.md); [Glama listing](https://glama.ai/mcp/servers/itsuzef/ableton-mcp)
- Forks and alternatives:
  - jpoindexter/ableton-mcp (200+ tools; MCP, REST and M4L; works with Claude, Ollama, OpenAI and Groq) — [GitHub](https://github.com/jpoindexter/ableton-mcp)
  - freekmurze/ableton-ai (150+ commands, per-note probability, includes a Claude Code skill) — [GitHub](https://github.com/freekmurze/ableton-ai)
  - uisato/ableton-mcp-extended — [Glama](https://glama.ai/mcp/servers/uisato/ableton-mcp-extended)
  - MCPBlender/ableton-mcp — [GitHub](https://github.com/MCPBlender/ableton-mcp)
- Daniel Raffel, "How to Control Ableton Live with Natural Language (MCP Setup)", 14 Mar 2026. Registers the server with Claude Code and Codex, with prompts such as "create a MIDI track with a drum rack" (EN) — [Daniel's Journal](https://danielraffel.me/til/2026/03/14/control-ableton-live-with-natural-language-mcp-setup/)
- MCP.Directory "Ableton MCP Server: Complete Guide (2026)" lists limits: timeouts, third-party plugins, no audio export (EN, snippet only) — [MCP.Directory](https://mcp.directory/blog/ableton-mcp-complete-guide-2026)
- Harish Garg, "Ableton Live + Claude.ai: MCP Setup Guide (2026)", updated Sept 2026 (EN) — [link](https://mcp.harishgarg.com/use/ableton-live/mcp-server/with/claudeai)
- LIA, "How to Control Ableton with AI: 5 Methods (2026)". Rates MCP 4/5 in difficulty. A vendor blog — [liaplugin.com](https://liaplugin.com/blog/how-to-control-ableton-with-ai-2026/)
- ChatDSP (Dillon Bastan) generates Max for Live devices from text prompts inside Live, using OpenAI or Anthropic models with the user's own API credits — [GearNews](https://www.gearnews.com/?p=246061); [LetsDataScience](https://letsdatascience.com/news/chatdsp-generates-max-for-live-devices-843eace1)
- MaxPy Studio is a web platform that generates M4L audio effects and MIDI instruments from prompts, free during beta — [Cycling '74 forum](https://cycling74.com/forums/maxpy-studio-generate-max-for-live-devices-from-prompts)
- MIDI Agent is a commercial plugin that generates MIDI (melodies, chords, drums) inside Live using ChatGPT, Claude or Gemini — [midiagent.com](https://www.midiagent.com/ai-midi-generator-for-ableton-live)
- Magenta Studio is a set of free ML MIDI devices (Generate, Continue, Interpolate, Groove, Drumify) for Live — [Google Research](https://research.google/pubs/pub48280). M4L.RhythmVAE is a rhythm-generation VAE device from Keio University — [Keio CCLab](https://cclab.sfc.keio.ac.jp/en/projects/m4l-rhythmvae-en/)

### Inferences
- A sensible learning path: Ableton's "Building Max Devices" pack first (basics) → ChatDSP or MaxPy (prompt-to-device) → MCP servers (session control). The MCP route is aimed at technically comfortable users.

### Gaps
- I found no independent benchmark of MCP server reliability.

## 4. Courses (EN and RU)

### Takeaway
Formal AI-in-production courses exist at Berklee Online (EN) and in Russian at Skillbox, HSE and an Ableton-specific RU video course (abletonprohelp.ru). I found no dedicated AI course from Point Blank, Moscow Music School or Sound Academy.

### Cited Findings
- Berklee Online:
  - OLMSC-100 "AI for Music and Audio": 4 weeks, 1 credit, $525, marked new
  - OLMSC-160 "AI in Music: Composition, Production, and Analysis": 3 credits, $1,575
  - Pages listed a semester start of 12 Jan 2026. Check the current schedule — [Berklee Online](https://online.berklee.edu/courses/interest/music-production)
- Point Blank's online programs are DAW-based (Ableton or Logic). Their blog mentions AI only in passing — [Point Blank blog](https://www.pointblankmusicschool.com/blog/?p=83332); [UCAS listing](https://www.ucas.com/explore/courses/4cc1eb23-bf79-4647-acc0-e5f642e84c46/music-production-dj-performance-online)
- RU: "Нейросети для музыки в Ableton Live 12" (abletonprohelp.ru), a paid video course. Covers setting up AI tools for chords and melodies and AI chord generators in Live 12 (RU, snippet only, page unreachable) — [abletonprohelp.ru](https://www.abletonprohelp.ru/video_courses/neural_networks_for_music_in_aleton_live/)
- RU: Skillbox "Продюсер музыкальных проектов" and "Music Producer Pro". The programme lists generating and processing music with neural networks. Includes briefs from real clients (Кофемания) and a possible release on Powerhouse Moscow — [Skillbox](https://skillbox.ru/course/producer-of-musical-projects/); [Skillbox Pro](https://skillbox.ru/course/music-producer-pro)
- RU: HSE (ВШЭ) has courses on generative neural networks in music, including Python and chatbots — [HSE course 1](https://www.hse.ru/edu/courses/919040466); [HSE course 2](https://www.hse.ru/edu/courses/1048980139)
- RU: Habr Career has a music course aggregator (Skillbox electronic music course etc.) — [Хабр Карьера](https://career.habr.com/courses/creativity-hobby/music); Habr article "Музыка как хобби: 7 курсов…" — [Habr](https://habr.com/ru/articles/1059534/)

### Gaps
- Moscow Music School, Sound Academy, Skillshare and Udemy AI-in-Ableton courses: none surfaced in search. Unverified, possibly absent.

## 5. Russian-language articles (Habr, VC.ru, others)

### Takeaway
RU coverage is mostly about tools (Suno, AI mixing and mastering, stem separation, MIDI generators). I found no Habr article specifically on LLM or MCP control of Ableton. The closest is a Habr post on a live-coding music platform with an AI agent.

### Cited Findings
- Habr: "Пишешь код, а звучит музыка. Как я сделал бесплатную лайвкодинг-платформу для создания музыки с ИИ-агентом". Mentions taking Suno samples into DAWs like Ableton (RU) — [Habr](https://habr.com/ru/articles/1006070/)
- Habr (SberDevices): "Live SymFormer Show". An AI music show in which the DAW served as the master clock (RU) — [Habr](https://habr.com/ru/companies/sberdevices/articles/826118/)
- Habr (2017, historical): "Как мы музицировали с нейронными сетями". Magenta responding to MIDI played on Push 2 (RU) — [Habr](https://habr.com/ru/post/342306/)
- push-music.ru: "Нейросеть для мелодии и аккордов: MIDI-генераторы в DAW 2026". Covers Live 12's built-in generators (Seed, Rhythm, Shape, Stacks) and Magenta Studio (RU, snippet only) — [push-music.ru](https://push-music.ru/blog/neyroset-dlya-melodii-i-akkordov)
- melodica.ru: stem separation overview. Notes that Ableton + Music AI is fast but can produce artifacts on dense mixes (RU) — [melodica.ru](https://melodica.ru/tpost/5544p6bf21-stems-kak-iskusstvennii-intellekt-nauchi)
- stemsplit.io RU page on stem separation in Ableton (RU, vendor) — [stemsplit.io/ru](https://stemsplit.io/ru/blog/ableton-stem-separation)
- VC.ru: "ТОП-5 ИИ для сведения треков" (RU, listicle) — [VC.ru](https://vc.ru/eksperts/2741545-top-5-ii-dlya-svedeniya-trekov); similar on DTF — [DTF](https://dtf.ru/kursfinder/4790028-ii-dlya-svedeniya-trekov); Timeweb — [Timeweb](https://timeweb.com/ru/community/articles/ii-dlya-svedeniya-trekov-top-5-neyrosetey-dlya-svedeniya-muzyki-i-masteringa)
- DTF/Kursfinder: "Чат GPT для музыки". Have ChatGPT propose structure and chord progressions as text, then build them in the DAW. ChatGPT cannot output an audio file (RU) — [DTF](https://dtf.ru/kursfinder/4747386-sozdanie-muzyki-s-chatgpt)
- Postium: Suno Studio exports stems and MIDI for finishing in Ableton, Logic and FL (RU) — [postium.ru](https://postium.ru/suno-zapustila-suno-studio/)
- Upsound: "Нейросети для артистов" (RU) — [Upsound](https://we.upsound.org/neroartist)

### Gaps
- I could not identify specific Russian YouTube channels focused on AI + Ableton. Searches returned none. A YouTube search in Russian ("нейросети Ableton", "Ableton MCP на русском") would be needed.
- I found no RU Habr or VC.ru article on Ableton MCP or the Claude connector.

## 6. Podcasts, talks and communities

### Takeaway
There are few Ableton-specific AI podcasts. The best 2025 audio is general AI-music discussion featuring Holly Herndon. Communities are general producer Discords (the official Ableton Discord) plus AI-music Discords (Producer.ai/Riffusion) and the Vi-Control "AI for Music Producers" group.

### Cited Findings
- FT Tech Tonic, "AI Music: The Infinite Jukebox" (3 Sept 2025): Holly Herndon, Tom Furse (AI-generated samples) and Ed Newton-Rex (copyright critic) (EN) — [Podwise](https://podwise.ai/episodes/5111951)
- Ableton Music Producer Podcast (Dan Giffin):
  - 1 Apr 2025 episode with Rob Late covers AI vs human creativity (EN) — [Podengine](https://podengine.ai/podcasts/ableton-music-producer-podcast)
  - #17 with Andrew Huang (not AI-specific) — [Spotify](https://creators.spotify.com/pod/profile/AbletonLive/episodes/17---Creative-Producing--Insights-with-Andrew-Huang-e2r9uu)
- "Making Music With AI", Nicholas Thompson with Holly Herndon (date unconfirmed) — [Pocket Casts](https://pocketcasts.com/podcasts/e1273fb0-958d-013d-1a28-0acc26574db2/6dbd3a79-5fd9-4afc-b600-cf0fdbdbdf50)
- Official Ableton Discord, about 29k members. General production, not AI-specific — [Discord directory](https://discord.com/servers/music?query=ins)
- Producer.ai (formerly Riffusion) Discord, an AI-generated music community — [DiscordHunt](https://discordhunt.com/en/servers/producerai-formerly-riffusion-1053034685590143047)
- Vi-Control "AI for Music Producers (AMP)" community thread — [Vi-Control](https://vi-control.net/community/threads/new-ai-for-music-producers-a-community.140664/)
- Ableton Forum thread "Best AI Tools for Ableton in 2023" — [Ableton Forum](https://forum.ableton.com/viewtopic.php?p=1807731)
- Large general producer Discord list (Busy Works Beats, 85k+) — [beatsyncpro](https://beatsyncpro.ai/blog/music-producer-discord-servers)

### Gaps
- Searches did not surface Reddit threads (r/ableton, r/WeAreTheMusicMakers, r/SunoAI) on Ableton MCP or the Claude connector. These subreddits are known to discuss AI, but I have no cited threads.
- I found no Russian Telegram, Discord or VK communities in this pass. They are likely covered by the separate Telegram research.

## 7. Recurring workflows, best practices and ethical/copyright cautions

### Takeaway
The recurring workflows are:
1. Use an LLM as a theory and chord assistant, then enter or edit MIDI by hand.
2. Use prompt-to-MIDI generation (MIDI Agent, Magenta, Live 12 generators, ChatGPT → Python → MIDI).
3. Separate stems locally in Live 12.3 for sampling and remixing.
4. Use AI mixing and mastering services as a reference that still needs manual correction.
5. Use LLMs to write Max for Live devices and Remote Scripts, or control Live through MCP.

On copyright, purely AI-generated audio is not protected in the US. Human arrangement and modification can be.

### Cited Findings
- LLM for chords and structure: ask for progressions with key, tempo and style, then transfer them to the piano roll. The LLM gives text, not audio or MIDI — [DTF (RU)](https://dtf.ru/kursfinder/4747386-sozdanie-muzyki-s-chatgpt)
- MIDI generation in DAW: Live 12 built-in generators plus Magenta Studio, free — [push-music.ru (RU, snippet)](https://push-music.ru/blog/neyroset-dlya-melodii-i-akkordov); MIDI Agent outputs editable MIDI notes — [midiagent.com](https://www.midiagent.com/ai-midi-generator-for-ableton-live)
- Stem separation: local processing, Suite only. Artifacts are possible on complex mixes — [MusicTech](https://musictech.com/news/music/ableton-live-12-3/); [melodica.ru (RU)](https://melodica.ru/tpost/5544p6bf21-stems-kak-iskusstvennii-intellekt-nauchi)
- AI mixing and mastering: online services balance and normalize but may need manual correction — [DTF (RU)](https://dtf.ru/kursfinder/4790028-ii-dlya-svedeniya-trekov); [Timeweb (RU)](https://timeweb.com/ru/community/articles/ii-dlya-svedeniya-trekov-top-5-neyrosetey-dlya-svedeniya-muzyki-i-masteringa)
- Suno → Ableton: Suno Studio exports stems and MIDI for finishing in a DAW. The free Suno tier is for personal or non-commercial use only — [postium.ru (RU)](https://postium.ru/suno-zapustila-suno-studio/); [Habr (RU)](https://habr.com/ru/articles/1006070/)
- A producer's blog treats AI (Suno) as "one instrument" within an Ableton Live 12 compose, arrange, mix and master process — [matthewess.com](https://matthewess.com/?p=5984)
- MCP best practices: run one client at a time, expect timeouts and weak third-party plugin control, no audio export — [README mirror](https://cdn.jsdelivr.net/gh/ahujasid/ableton-mcp@main/README.md); [MCP.Directory (snippet)](https://mcp.directory/blog/ableton-mcp-complete-guide-2026)
- Ableton frames ML as assistive, helping musicians realise ideas faster rather than composing for them (press interpretation of the job posting) — [LetsDataScience](https://letsdatascience.com/news/ableton-hires-machine-learning-engineer-to-enhance-live-0e727647)
- Copyright: the US Copyright Office's Part 2 report (Jan 2025) says purely AI-generated music without sufficient human control over expressive elements is not copyrightable. Human "creative arrangements or modifications" can be. Decisions are made case by case — [Manatt](https://manatt.com/insights/newsletters/copyright-office-releases-new-report-on-copyrightability-of-ai-works); [Rimon Law](https://www.rimonlaw.com/how-copyright-office-guidance-applies-to-music-that-includes-ai-generated-material/); [LoC Copyright blog](https://blogs.loc.gov/copyright/2025/05/a-i-art-and-copyright-the-human-element-that-makes-all-the-difference/)
- Ethics: Ed Newton-Rex frames AI music as a threat because of training-data copyright infringement and job displacement — [FT Tech Tonic via Podwise](https://podwise.ai/episodes/5111951)

### Inferences
- Shared best practice: keep the human in the loop. Use AI for ideas, MIDI drafts, stems and docs lookup, and keep the arrangement, sound design and final mix human. This also strengthens the copyright position.
- Check each service's licence (Suno free tier, Splice sample licences) before commercial release. Avoid separating stems from copyrighted records for release without clearance. Stem separation does not clear a sample.

### Gaps
- I found no Russian-law (ГК РФ) analysis of copyright for AI music in this pass.
- I did not verify whether Part 3 of the USCO report (training) changes guidance for producers.
