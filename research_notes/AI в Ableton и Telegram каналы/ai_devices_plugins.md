# AI-powered features, Max for Live devices and third-party plugins for Ableton Live (as of October 2026)

Method note: research date 2026-10-18. Direct page fetches were blocked by the sandbox egress proxy (ableton.com, vixsound.com, releasebot.io and others returned connect errors), so findings below come from search-engine result summaries of the cited pages. Treat prices as indicative; several were reported by third-party retailers or blogs and conflict across sources. Vendor-written "best AI tools" roundups (VIXSOUND, LIA, MIDI Agent, MixingGPT) rank their own products first and should be weighed accordingly.

## 1. Built-in Ableton Live 12.x AI/ML-adjacent features (what's new 2025-2026)

### Takeaway
Ableton's own "AI" is modest and local: ML-based Sound Similarity search and auto-tagging in the browser (12.0/12.1), algorithmic MIDI Generators/Transformations (12.0, extendable via Max for Live), and, the big 2026 addition, built-in Stem Separation in Live 12 Suite (12.3, powered by Music.AI/Moises tech, runs locally). There is no officially announced Live 13 as of October 2026.

### Cited Findings
**Live 12.0 (2024) — baseline ML/generative features**
- MIDI Transformations reshape existing clips (ornaments, acceleration curves, guitar-style strums); MIDI Generators create new material with controls for density, rhythm, pitch range, etc. Additional Max for Live Transformations/Generators are available and users can build their own — [Ableton: What's coming in Live 12](https://www.ableton.com/en/blog/whats-coming-in-live-12/); [Ableton: All new features in Live 12](https://www.ableton.com/en/live/all-new-features/)
- Sound Similarity Search starts from a sample and uses machine learning to find comparable sounds and presets; it can also find and swap similar samples inside Simpler or Drum Rack — [CDM: Live 12 guide](https://cdm.link/2023/11/ableton-live-12-everything-new/); [EDM.com: Generative MIDI tools and AI-powered samples in Live 12](https://edm.com/gear-tech/ableton-live-12/)

**Live 12.1 (2024)**
- Live 12.1 auto-assigns tags to any library sample under 60 seconds; VST3 plugins get tags from metadata — [Editors Keys: Live 12 best new features](https://www.editorskeys.com/blogs/news/ableton-live-12-best-new-features-for-producers)

**Live 12.2 (released June 11, 2025, free for Live 12 users)** — not AI, but workflow context
- Bounce to New Track (bounce clips/time selections incl. processing to a new audio track); overhauled Auto Filter (new Resampling, Comb, Vowel, DJ filter types; now also on Move and Note); Expressive Chords, a new MPE-capable Max for Live device to play chord progressions with one key/pad — [Ableton: Live 12.2 is out now](https://www.ableton.com/blog/live-12-2-is-out-now); [MusicTech: Live 12.2 release](https://musictech.com/news/gear/ableton-live-12-2-release-date-features/); [DJ Mag](https://djmag.com/tech/ableton-announces-latest-update-live-122-new-auto-filter-and-more)
- Edition availability of Expressive Chords conflicts: Ableton says Intro/Standard/Suite; MusicTech says all editions incl. Push — [Ableton blog](https://www.ableton.com/en/blog/live-12-2/); [MusicTech](https://musictech.com/news/gear/ableton-live-12-2-release-date-features/)

**Live 12.3 (public beta ~January 2026; now released) — the main AI addition**
- Built-in Stem Separation splits vocals, drums, bass (and remainder) from any audio clip; Live 12 **Suite only** (not Standard/Intro/Lite); powered by technology from Music.AI (the company behind Moises); runs locally on the user's machine — [Ableton: Live 12.3 is out now](https://www.ableton.com/en/blog/live-12-3-is-here/); [Ableton Help: Stem Separation FAQ](https://help.ableton.com/hc/en-us/articles/23730994755996-Stem-Separation-in-Ableton-Live-FAQ); [DJ Mag](https://djmag.com/news/ableton-unveils-stem-separation-tool-live-123-update)
- Reported to offer a fast mode (sketching) and a higher-quality mode — [LiveSchool: 12.3 review](https://liveschool.net/blog/ableton-12-3-is-here/)
- 12.3 also adds Splice integration (Splice sample browsing inside Live), Bounce Groups, Paste Bounced Audio, a new Auto Pan-Tremolo, and Push 3 standalone support for stem separation and bounce tools — [Ableton: Live 12.3](https://www.ableton.com/en/blog/live-12-3-is-here/); [Dubspot: Live 12.3 update](https://blog.dubspot.com/ableton-live-12-3-update); [Revolution 935: 12.3 beta, Jan 9 2026](https://www.revolution935.com/2026/01/09/splice-integration-and-stem-separation-arrive-in-ableton-live-12-3-beta/)

**Later 2026 updates (version number unconfirmed)**
- A release-notes aggregator (~September 2026) lists: Learn View replacing Help View, ability to remove specific stems from a track in Arrangement View, a dedicated Link page with new Link Audio options, and a Windows option for more audio threads — [Releasebot: Ableton release notes, Sept 2026](https://releasebot.io/updates/ableton) (secondary aggregator; version not stated)

**Live 13**
- No official announcement found; online "Live 13" content is speculation/wish lists, and one 2026 article calls Live 13 rumours internet gossip — [boost.audio: Ableton Live 13 in 2026](https://boost.audio/en/news/ableton-live-13-w-2026-roku-rzeczywistosc-vs-spekulacje); [Ableton Forum: New feature for 13](https://forum.ableton.com/viewtopic.php?t=248860)

### Inferences
- Several 2026 third-party roundups (e.g. VIXSOUND's "Live has no built-in equivalent" for stem separation, as summarised from [vixsound.com](https://vixsound.com/best/best-ai-vst-plugins)) are outdated or self-serving — built-in stems exist since 12.3 for Suite owners. Standard/Intro users still need a third-party splitter.
- Ableton's stance is "assistive, local, non-generative-audio": no text-to-music or LLM assistant is built in; LLM control comes from community M4L/MCP projects (see section 2).

### Gaps
- Exact Live 12.3 final release date, and whether a 12.4 exists and what it contains, could not be confirmed (ableton.com fetch blocked).
- Number/kind of stems in 12.3 beyond vocals/drums/bass (e.g. "other"/"instruments") not confirmed from primary source.

## 2. Max for Live AI devices (Magenta Studio, Magenta RT/Lyria, RAVE/nn~, IRCAM, DDSP, drum generators, LLM-in-Max)

### Takeaway
The free Max for Live AI layer is: Magenta Studio (aging but still the free MIDI-generation baseline), IRCAM's nn~ external running RAVE and other TorchScript models in Max, and a fast-growing set of LLM/MCP bridges (Producer Pal, AbletonMCP variants) that let Claude/ChatGPT/Gemini/local models drive Live. Google's Magenta RealTime 2 (June 2026) ships as an AUv3 plugin (macOS/Apple Silicon), not a Max for Live device.

### Cited Findings
**Magenta Studio (Google Magenta) — free, M4L**
- Suite of free Ableton Live tools: Generate, Continue, Interpolate, Groove, Drumify; installed by dragging the .amxd into a MIDI track; download via g.co/magenta/studio — [Google Research paper](https://research.google/pubs/magenta-studio-augmenting-creativity-with-deep-learning-in-ableton-live/); [Ableton blog: Magenta Studio](https://www.ableton.com/en/blog/magenta-studio-free-ai-tools-ableton-live); [Magenta: Studio for Ableton Live](https://magenta.tensorflow.org/v1/studio/ableton-live)
- Limitations: monophonic melody input, fixed drum MIDI mapping; very limited active development in recent years — [aitoolsatlas.ai](https://aitoolsatlas.ai/tools/magenta-studio/pricing) (low-authority directory)
- Still cited in 2026 roundups as "the free baseline", built for Max for Live — [LIA: Best in-DAW AI assistants for Ableton 2026](https://liaplugin.com/blog/best-ai-tools-ableton-2026/)

**Magenta RealTime 2 (MRT2) — Google DeepMind, open weights, June 2026**
- Open-weights live music model (2.4B params; smaller 230M variant) with audio, MIDI and text control; released with a series of Mac apps; 2.4B needs a recent Apple Silicon Mac — [GitHub magenta/magenta-realtime](https://github.com/magenta/magenta-realtime); [Magenta RT 2 site](https://magenta.github.io/magenta-realtime/); [Omar Sanseviero (Google) on X](https://x.com/osanseviero/status/2062598679735763304)
- Repo includes an "All-in-one AUv3 plugin for DAWs" (examples/mrt2/auv3), placed on a MIDI track; macOS/Apple Silicon only; latest tag v2.0.3 — [GitHub releases](https://github.com/magenta/magenta-realtime/releases)
- A third-party guide claims a free AU/VST3 plugin usable in Ableton; VST3 not confirmed by official repo — [mcp.directory MRT2 guide](https://mcp.directory/blog/magenta-realtime-2-open-live-music-model-2026)

**DDSP-VST (Magenta) — free**
- Realtime DDSP neural synth & effect (timbre transfer), verified on Ableton, Logic, FL Studio, Reaper — [GitHub magenta/ddsp-vst](https://github.com/magenta/ddsp-vst)

**RAVE / nn~ (IRCAM ACIDS) — free, open source**
- RAVE is available as a VST plugin or a Max/MSP / PureData external with downloadable models; nn~ deploys serialized TorchScript models as a Max/MSP external (originally RAVE, now other real-time architectures too) — so it runs inside Max for Live — [IRCAM ACIDS projects](https://acids-ircam.github.io/projects/); [Neutone SDK paper (arXiv)](https://arxiv.org/html/2508.09126v1)
- IRCAM released a RAVE VST (beta) with models sol_ordinario_fast, sol_full, musicnet, isis — [IRCAM Forum: RAVE VST release](https://discussion.forum.ircam.fr/t/new-release-rave-vst-plugin-rave-models/76271); [IRCAM Forum project page](https://forum.ircam.fr/projects/detail/rave-vst/)
- A 2025 guide says the RAVE VST source repo was archived and the Windows build is standalone only — [neuralanalog.com RAVE docs](https://neuralanalog.com/docs/rave-model-ircam) (secondary; status should be treated as "possibly unmaintained")
- IRCAM ran a "RAVE Model Challenge 2025" — [Neutone FX models](https://neutone.ai/fx/models)

**LLM-in-Max / MCP devices (2025-2026, mostly free/open source)**
- Producer Pal: an Ableton MCP server packaged as a Max for Live device (Node for Max); works with Claude, Gemini, ChatGPT, Ollama, and local models via LM Studio (experimental) — [producer-pal.org](https://producer-pal.org/); [Cycling '74 forum thread](https://cycling74.com/forums/producer-pal-mcp-server-running-in-node-for-max-to-control-ableton-live)
- AbletonMCP (jpoindexter fork): 200+ tools via MCP, REST API and a Max for Live chat-UI device; supports Ollama, OpenAI, Claude API, Groq — [GitHub jpoindexter/ableton-mcp](https://github.com/jpoindexter/ableton-mcp)
- Other: ableton-and-max-mcp — [GitHub TropinAlexey/ableton-and-max-mcp](https://github.com/TropinAlexey/ableton-and-max-mcp); comparison of Ableton MCP servers incl. Jamu (Ableton-only MCP, free demo tier) — [Jamu: Best Ableton MCP servers 2026](https://www.jamu.ai/blog/best-ableton-mcp-servers)
- Commercial in-DAW chat assistants: LIA (controls Live via "LIA Bridge" helper; prompt routing needs internet; waitlist) — [LIA blog](https://liaplugin.com/blog/best-ai-tools-ableton-2026/); VIXSOUND (chat panel inside Live writing editable MIDI, local Demucs stem separation, audio-to-MIDI) — [VIXSOUND: 12 best AI tools for Ableton 2026](https://vixsound.com/blog/best-ai-tools-for-ableton-2026) (vendor-ranked)

### Inferences
- For "AI inside Max for Live" specifically, the practical 2026 stack is: Magenta Studio (MIDI ideas), nn~ + RAVE models (neural timbre/synthesis in Max), and Producer Pal / AbletonMCP (LLM controlling the Live Set). MRT2 is the most notable new generative model but enters Live as a plugin (Mac) rather than as M4L.
- Magenta Studio should be flagged "legacy / low maintenance" — still works but not evolving.

### Gaps
- No source found for a dedicated Lyria RealTime Max for Live device, or for a 2025-2026 DDSP M4L device.
- Could not verify Magenta Studio 2.0 (the native M4L rebuild) details or current Live 12 compatibility from a primary source.
- No specific maxforlive.com AI drum-generator devices were surfaced by search; maxforlive.com itself was not reachable.

## 3. Third-party AI plugins commonly used in Ableton

### Takeaway
The mature, widely-used AI plugin categories are: assistive mixing/mastering (iZotope Ozone 12 / Neutron 5, sonible smart:), sound design via resynthesis (Synplant 2, Neutone FX, Audialab), MIDI/harmony generation (Scaler 3, Orb Producer Suite 3, Captain, MIDI Agent), sample discovery (XO, Output Co-Producer, Splice), and stem separation (Ableton 12.3 Suite built-in vs. RipX DAW, LALAL.AI VST, Demucs-based tools).

### Cited Findings
**Mixing / mastering assistants**
- iZotope Ozone 12: Advanced $499, Standard $219, Elements $55; also included in a $25/month subscription with 100+ plugins — [iZotope Ozone Advanced](https://www.izotope.com/products/ozone-advanced); [iZotope Ozone Standard](https://www.izotope.com/products/ozone-standard)
- Ozone 12 Advanced lowest recorded price $366 (Thomann, Mar 2026); Elements $26 (Plugin Boutique, May 2026) — [plugindeals.net Advanced](https://plugindeals.net/price-history/iZotope-Ozone-12-Advanced/reci3E9m1S3zItE6B/); [Elements](https://plugindeals.net/price-history/iZotope-Ozone-12-Elements/recz5tDz4QrsbpddI/)
- iZotope Neutron 5 (AI-assisted mixing): $299 regular; Neutron 5 Elements $55 — [Native Instruments Neutron 5 pricing](https://www.native-instruments.com/en/products/izotope/neutron-5/pricing/); DJ Mag reported an intro price of $174 rising to $249 at launch (older promo; conflicts) — [DJ Mag](https://djmag.com/tech/izotope-announces-new-version-of-ai-powered-mixing-tool-neutron-5)
- sonible smart:EQ 4 is "the usual adaptive EQ pick"; sonible smart:chain lists at 179 USD/EUR regular (99 intro) — [MixingGPT per-DAW stack guide](https://mixinggpt.com/blog/best-ai-mixing-plugins-logic-ableton-pro-tools-2026); [Dubspot: Neutron 5 vs smart:chain](https://blog.dubspot.com/plugins/compare/neutron-5-vs-sonible-smart-chain)

**Sound design / neural synthesis**
- Synplant 2 (Sonic Charge): Genopatch AI creates synth patches from samples; $149, $50 upgrade from v1, 3-week trial — [Sonic Charge Synplant](https://soniccharge.com/synplant); [Sonic Charge products](https://soniccharge.com/products); [Synthtopia launch article](https://www.synthtopia.com/content/2023/10/04/synplant-2-lets-you-create-synth-patches-from-samples-using-artificial-intelligence/)
- Neutone FX (Qosmo): free VST3/AU host for real-time neural audio models (many RAVE timbre-transfer models, e.g. RAVE.amen, RAVE.choir, RAVE.drumkit); models download in-plugin; some experimental — [Neutone FX models](https://neutone.ai/fx/models); [KVR: Neutone](https://www.kvraudio.com/product/neutone-by-qosmo); [Neutone SDK paper](https://arxiv.org/html/2508.09126v1)
- Audialab: "ethical AI", local, one-time purchase; Deep Sampler 2 is free; Everything Bundle ~$99 during recurring 50% sales — [audialab.net](https://audialab.net/)

**MIDI / harmony / composition**
- Scaler 3 (Scaler Music): $99 (launch intro $79, March 2025); upgrade $39; Scaler 3 + Scaler EQ bundle $158 — [Plugin Boutique: Scaler 3](https://www.pluginboutique.com/product/3-Studio-Tools/93-Music-Theory-Tools/14563-Scaler-3); [Sound On Sound news](https://www.soundonsound.com/news/scaler-music-introduce-scaler-3)
- Orb Producer Suite 3.0 (Hexachords): 4 AI-powered plugins; price reported variously at €99 (with €39 upgrade from v2) or starting €49 — conflicting — [Rekkerd](https://rekkerd.org/hexachords-releases-orb-producer-suite-3-0-with-4-ai-powered-plugins/); [opentools.ai](https://opentools.ai/tools/orb-producer)
- Captain Plugins: rule-based (not technically AI) MIDI chord/melody/bass generation in any DAW; MIDI Agent pitched as AI MIDI plugin — [MIDI Agent: Best AI plugins for Ableton, FL, Logic, Studio One](https://www.midiagent.com/blog/best-ai-plugins-for-ableton-fl-studio-logic-pro-studio-one) (vendor list)
- Other names in 2026 roundups that "fit in Ableton": Staccato, LANDR Composer, Output Co-Producer, Synplant, smart:EQ, Neutron, Ozone — [MIDI Agent blog](https://www.midiagent.com/blog/best-ai-plugins-for-ableton-fl-studio-logic-pro-studio-one)

**Samples / drums / discovery**
- XLN Audio XO (ML-mapped drum sample space): ~$149 list; from $132, avg ~$144 (Equipboard, Oct 11 2026) — [Black Octopus: XLN XO](https://blackoctopus-sound.com/product/xln-xo/); [Equipboard](https://equipboard.com/items/xln-audio-xo)
- Output Co-Producer (AI sample suggestions from your session): $9.99/month alone, or in Output One bundle (Arcade, Co-Producer, Portal, Thermal, Movement) $14.99/month or $119.99/year — [Gearspace thread](https://gearspace.com/threads/output-co-producer.1445305/); [toolmage: Co-Producer](https://www.toolmage.com/en/tool/co-producer/)
- Splice: Sounds+ $12.99/month for 100 credits; Splice browsing now integrated inside Live 12.3 — [Wikipedia: Splice](https://en.wikipedia.org/wiki/Splice_(platform)); [Ableton 12.3](https://www.ableton.com/en/blog/live-12-3-is-here/)

**Stem separation (beyond Ableton built-in)**
- LALAL.AI VST plugin (VST/AU, all major DAWs; 7 stems locally via its Lyra model per one source); free 10-min tier, Lite $7.50/mo billed annually, Pro $15/mo billed annually, minute packs — [loop.fans LALAL.AI review 2026](https://music.loop.fans/ai/lalal-ai-in-depth-review-the-new-standard-in-ai-audio-separation); [VIXSOUND: Best AI VST plugins](https://vixsound.com/best/best-ai-vst-plugins)
- RipX DAW: separates and shows each instrument as editable notes; $99 / Pro $198 per one source, ~$179 per others; no subscription — [MixingGPT: 8 stem engines compared](https://mixinggpt.com/blog/best-ai-stem-separation-tools-2026); [Chartlex comparison](https://www.chartlex.com/blog/marketing/ai-stem-separation-tools-2026)
- Moises: practice-oriented app, ~$4–5.99/month, no VST in results — [stemsplitterai.com](https://stemsplitterai.com/best-stem-splitter); note Moises' parent Music.AI powers Ableton's built-in separator — [DJ Mag](https://djmag.com/news/ableton-unveils-stem-separation-tool-live-123-update)
- Other engines compared in 2026: Demucs (open source), SpectraLayers, Logic Stems, Audioshake, iZotope RX 12 Music Rebalance — [MixingGPT](https://mixinggpt.com/blog/best-ai-stem-separation-tools-2026)

### Inferences
- For a Live 12 Suite user, built-in stems cover most remix/sampling needs; RipX remains the choice for note-level editing of separated audio, LALAL/UVR5/Demucs for more stem types.
- Free AI entry points for an Ableton producer: Neutone FX, Audialab Deep Sampler 2, DDSP-VST, Magenta Studio, nn~/RAVE, Producer Pal.

### Gaps
- No verified 2026 prices found for: sonible smart:EQ 4, LANDR mastering plugin, Captain Plugins (Mixed In Key), Audiomodern Playbeat 4, Sononym, Neutone FX premium models (if any), MIDI Agent. Vendor sites were not reachable.
- Output Co-Producer and Splice "Create"/CoSo current status (Splice Create mobile app) not verified.

## 4. Generative music services (Suno, Udio, Stable Audio, ElevenLabs Music, Lyria) and bringing stems/MIDI into Ableton

### Takeaway
Suno is the most DAW-friendly service (Suno Studio exports up to 12 time-aligned WAV stems plus MIDI via "Get MIDI"; Studio 2.0 reported Aug 2026). Stable Audio now has a beta DAW instrument plugin (Aug 2026) that runs inside Ableton. ElevenLabs Music offers post-hoc 2/4/6-stem separation. Udio has disabled all downloads since its October 2025 UMG settlement, so it is effectively unusable for Ableton workflows. Lyria has no stem export.

### Cited Findings
**Suno / Suno Studio**
- Suno Studio exports up to 12 time-aligned WAV stems (Auto Split); MIDI via "Get MIDI" on an extracted stem (~10 credits/operation); plan access (Pro vs Premier) conflicts across sources — [techjacksolutions Suno Studio guide](https://techjacksolutions.com/ai-tools/suno/suno-studio/); [Genx Notes: Suno MIDI export](https://blog.genxnotes.com/en/suno-midi-export/); [soundtomidi.com](https://soundtomidi.com/blog/suno-to-midi/)
- Suno Studio 2.0 reported shipped Aug 13 2026: MIDI recording, built-in wavetable synth, uncapped 32-bit/48kHz multitrack/stem export for Premier; still no VST/AU hosting or DAW sync — [Dubspot: Suno Studio 2.0](https://blog.dubspot.com/suno-studio-2-0) (secondary; verify with Suno)
- Community tool suno-to-ableton generates an .als with grid-aligned, tempo-matched, cleaned stems — [GitHub steven-ahfu/suno-to-ableton](https://github.com/steven-ahfu/suno-to-ableton)
- Ableton import tip: dropping Suno MIDI prompts to apply tempo/time signature — [Undetectr: Suno stems to DAW](https://undetectr.com/blog/suno-stems-daw-workflow)

**Udio — flag: downloads disabled**
- Udio disabled audio, video and stem downloads after its Oct 2025 UMG settlement (Help Center updated Feb 17 2026); not restored as of late Sept 2026; future licensed "walled garden" platform — [aitools-directory Udio review 2026](https://www.aitools-directory.com/blog/udio-ai-review-2026/); [Undetectr: Udio download](https://undetectr.com/blog/udio-download); [Replayed Studio: Suno-Warner & Udio-UMG deals](https://replayedstudio.com/blog/suno-warner-udio-universal-deals)
- Conflicting report that Udio signed DRM provider BuyDRM (July 2026) for a licensed app "Starstruck" — [audiwave.ai](https://audiwave.ai/music-tools/how-to-download-from-udio) (unverified)

**Stable Audio (Stability AI)**
- Stable Audio DAW plugin announced ~Aug 18 2026, early beta: loads as instrument (macOS AU/VST3) on an Ableton instrument track, syncs to session BPM, generates up to 6 min; Windows "coming soon"; commercially-safe models, users own outputs (> $1M revenue needs Enterprise licence) — [Dubspot: Stable Audio plugin](https://blog.dubspot.com/stable-audio-daw-plugin-2026); [claypier.com](https://claypier.com/en/stable-audio-daw-plugin-beta/); [musicproductionwiki review](https://musicproductionwiki.com/articles/stable-audio-3-review)
- Stable Audio 3.0 generates isolated parts via prompt tags; web app supports audio-to-audio, inpainting, experimental stem export — [Stability AI explainer](https://stability.ai/explainers/ai-music-stems-and-audio-inpainting-generating-parts-instead-of-finished-songs)
- Stability AI raised $76M (Series B), music labels received equity — [TechTimes, Aug 26 2026](https://www.techtimes.com/articles/325673/20260826/stability-ai-raises-76m-music-labels-get-equity-artists-still-get-nothing.htm)
- A Stable Audio 3.0 challenge winner built an Ableton plugin for microtonal (Arabic maqam) style transfer running locally — [Stability AI on X](https://x.com/StabilityAI/status/2072423193927668193)

**ElevenLabs Music**
- Music v2.5 default; 2-, 4- or 6-stem separation of a finished mix (not natively generated parts); MP3 44.1kHz and WAV export — [sunofix.app](https://sunofix.app/blog/how-to-improve-elevenlabs-music-audio-quality/); [aixploria](https://www.aixploria.com/en/elevenlabs-music-v2-5/)

**Google Lyria / Magenta RT**
- Lyria has no stem separation/export (via Vertex AI or Flow) — [lyria3-pro.com comparison](https://lyria3-pro.com/blog/lyria-3-vs-elevenlabs); [teamday.ai Sept 2026](https://www.teamday.ai/blog/best-ai-music-models-2026)
- Open Magenta RealTime 2 can run as an AUv3 plugin directly in a DAW (see section 2) — [GitHub magenta-realtime](https://github.com/magenta/magenta-realtime)

### Inferences
- Typical 2026 workflow: generate in Suno (or Stable Audio plugin directly in Live) → export stems/MIDI → drag into Live → warp/clean, or run full mixes through Live 12.3 Stem Separation / audio-to-MIDI conversion.
- Rights/licensing (Suno–Warner, Udio–UMG deals, Stable Audio "commercially safe") is a selection factor for producers releasing music.

### Gaps
- Official Suno release notes for Studio 2.0 and per-plan pricing not verified.
- Stable Audio plugin price not found.

## 5. Voice / timbre transfer tools (Kits.ai, ACE Studio, Synthesizer V, Vocaloid AI) in Ableton workflows

### Takeaway
AI vocal synthesis enters Live mostly via bridge plugins (ACE Studio 2 via ACE Bridge 2) or full plugins (Synthesizer V Studio 2 Pro, Dreamtonics Vocoflex); voice conversion of recorded vocals is done with Kits.ai-type services, and real-time timbre transfer with Neutone FX/RAVE/DDSP-VST.

### Cited Findings
- ACE Studio 2.0 released Dec 8, 2025: more AI voices, AI instruments, generative kits, DAW-style Canvas; no third-party VST/AU hosting — [ACE Studio blog](https://acestudio.ai/blog/ace-studio-2-released/); [Sound On Sound review](https://www.soundonsound.com/reviews/ace-studio-2); [Rekkerd](https://rekkerd.org/ace-studio-2-0-all-in-one-ai-music-studio-released/)
- ACE Studio connects to DAWs via ACE Bridge 2 (VST3/AU/AAX) per a third-party listing — [LinkStart AI](https://www.linkstartai.com/en/agents/ace-studio-2-0); a review headlined "Is ACE Studio worth $398?" — [musicseed.ai](https://www.musicseed.ai/reviews/acestudio-ai-review)
- MusicTech (July 2026) found ACE Studio 2 heavy on CPU (two AI instrument tracks + a few plugins push an M4 Pro over 100%) — [MusicTech review](https://musictech.com/reviews/digital-audio-workstations/ace-studio-2-review/)
- Synthesizer V Studio 2 Pro runs as a full plugin in the DAW (vs ACE's bridge), per a KVR user comparison (Jan 2026; opinion) — [KVR forum](https://www.kvraudio.com/forum/viewtopic.php?t=626750)
- Dreamtonics Vocoflex loads inside any DAW for voice transformation — [AudioCipher: AI voice generators](https://www.audiocipher.com/post/ai-voice-generators)
- Kits.ai: best for voice conversion of recorded vocals — [AudioCipher](https://www.audiocipher.com/post/ai-voice-generators)
- Real-time neural timbre transfer plugins: Neutone FX (free), DDSP-VST (free), RAVE VST — see section 2/3 sources ([Neutone](https://neutone.ai/fx/models); [DDSP-VST](https://github.com/magenta/ddsp-vst))

### Inferences
- In Ableton, the most "native" vocal-AI option is Synthesizer V (instrument plugin on a MIDI track); ACE Studio is better treated as a separate app synced via bridge.

### Gaps
- No 2026 pricing verified for Kits.ai, Synthesizer V Studio 2 Pro, or Vocaloid 6 / Vocaloid AI; Vocaloid's current status not researched due to tool-call budget.
- Kits.ai VST/plugin availability not confirmed.
