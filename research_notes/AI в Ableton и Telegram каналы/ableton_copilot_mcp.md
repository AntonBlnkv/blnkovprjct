# LLM / AI-agent control of Ableton Live: "Ableton Copilot" and MCP servers (state as of Oct 18, 2026)

Method note: GitHub repos were shallow-cloned and inspected directly (tool names from source, last-commit dates from git log), and the npm and PyPI registries were queried for release dates. Some directories and blogs (mcp.directory, producer-pal.org, gearnews, findskill.ai, godberrystudios) could not be fetched from this environment. Facts from those sites come only from search snippets and are flagged as secondary. Star counts are from GitHub pages fetched in Oct 2026 unless marked otherwise.

## 1. Which projects exist (URLs, popularity, last update, maintenance)

### Takeaway
"Ableton Copilot" almost certainly means **xiaolaa2/ableton-copilot-mcp**. It is a small Node/TypeScript MCP server built on ableton-js (~93 stars). Last code activity was Jul 29, 2026, but the latest npm release is still 0.9.0 (Mar 14, 2026). The largest and most active project is **ahujasid/ableton-mcp** (~3.2k stars, PyPI 1.4.5 released Sep 22, 2026). The most polished and best-documented one is **Producer Pal**, a Max for Live device (v2.4.0, commits Oct 1, 2026). Ableton has no official agent that controls Live. The official "Ableton" connector Anthropic launched on Apr 28, 2026 is documentation-grounded Q&A, not session control.

### Cited Findings
**xiaolaa2/ableton-copilot-mcp ("Ableton Copilot")**: https://github.com/xiaolaa2/ableton-copilot-mcp
- 93 stars, 18 forks, 8 watchers, 84 commits, 3 open PRs. No GitHub Releases. MIT license. States it is a third-party project, not made by Ableton. — [GitHub](https://github.com/xiaolaa2/ableton-copilot-mcp)
- npm package `@xiaolaa2/ableton-copilot-mcp`: dist-tag latest = **0.9.0**, published 2026-03-14. Earlier: 0.8.0 (2025-06-21), 0.7.0 (2025-06-18), first release 0.4.0 (2025-05-06). — [npm registry](https://registry.npmjs.org/@xiaolaa2/ableton-copilot-mcp) (queried directly)
- The 0.9.0 commit is "feat: upgrade ableton-js to v4.0.4 and optimize note field abbreviations" (Mar 14, 2026). — [commits](https://github.com/xiaolaa2/ableton-copilot-mcp/commits/main)
- Later commits on main (Jul 3 and Jul 29, 2026, merged from contributor Djean3, PRs #17, #20, #21) add "batch clip note read/write", "get_track_overview, create_clips_batch, track sends" and "fix: load_device can silently land on the wrong track". **These commits are newer than the 0.9.0 npm release**, and package.json still says 0.9.0. A plain `npx @xiaolaa2/ableton-copilot-mcp` install very likely lacks these tools and the fix until a new npm release ships. — [commits](https://github.com/xiaolaa2/ableton-copilot-mcp/commits/main); package.json in a clone of the repo
- Directory listings: [Glama](https://glama.ai/mcp/servers/xiaolaa2/ableton-copilot-mcp), [mcp.so](https://mcp.so/servers/ableton-copilot-mcp?tab=tools), [PulseMCP](https://pulsemcp.com/servers/xiaolaa2-ableton-copilot), [Playbooks](https://playbooks.com/mcp/xiaolaa2-ableton-copilot). One listing cited ~550 downloads and 24 stars (an old snapshot). — search snippet via [PulseMCP/mcp.so](https://pulsemcp.com/servers/xiaolaa2-ableton-copilot)

**ahujasid/ableton-mcp ("AbletonMCP", the original)**: https://github.com/ahujasid/ableton-mcp
- ~3.2k stars, 452 forks, 14 open issues, 32 open PRs, MIT. Author: Siddharth Ahuja (https://x.com/sidahuj). "Third-party integration and not made by Ableton." — [GitHub](https://github.com/ahujasid/ableton-mcp)
- Actively maintained in 2026. Recent commits: Sep 22, 2026 "fix: scrub paths from dataset, bind bridge to loopback, fix browser tree" and "update: opt in telemetry". Aug 30 "Fix arm-state reads on group, return and main tracks (#128)". Aug 25 "Install Remote Script into User Library, not legacy User Remote Scripts". Aug 16 "Add clear_notes_from_clip", "Add delete_clip", "Add create_locator", "Add instructions for integrating Claude Code". — [commits](https://github.com/ahujasid/ableton-mcp/commits/main)
- PyPI `ableton-mcp` latest **1.4.5** (2026-09-22). Previous: 1.4.0 (Aug 30), 1.3.9 (Aug 25), 1.3.7 (Aug 16). — [PyPI](https://pypi.org/project/ableton-mcp/) (queried directly)
- Original launch demo (80s synthwave from two prompts) is from March 2025 (older info). — search snippet, [README demo video](https://youtu.be/VH9g66e42XA)

**Producer Pal (adamjmurray)**: https://github.com/adamjmurray/producer-pal · docs https://producer-pal.org
- 331 stars, 40 forks, GPL-3.0. Runs as a Max for Live device (`Producer_Pal.amxd`) hosting an MCP server in Node for Max. It also exposes a REST API, so AI is optional. — [GitHub](https://github.com/adamjmurray/producer-pal), [Cycling '74 forum](https://cycling74.com/forums/producer-pal-mcp-server-running-in-node-for-max-to-control-ableton-live)
- package.json version 2.4.0. Last commit 2026-10-01 (dependabot merges). About 6,000 commits per a search snippet. Very actively maintained. — repo clone; [search snippet](https://github.com/adamjmurray/producer-pal)

**uisato/ableton-mcp-extended**: https://github.com/uisato/ableton-mcp-extended
- Python 3.10+, Live 11+ (any edition). Has a hybrid TCP/UDP server for low-latency controllers and integrates with the ElevenLabs MCP for TTS and sound effects imported into Live. Demo video: https://www.youtube.com/watch?v=7ZKPIrJuuKk. ~167 stars and 35 forks per an aggregator. Last commit 2026-05-06. 46 `@mcp.tool` functions in server.py. — README (repo clone); [gittrend](https://gittrend.io/repo/uisato/ableton-mcp-extended); [Glama](https://glama.ai/mcp/servers/uisato/ableton-mcp-extended)

**jpoindexter/ableton-mcp**: https://github.com/jpoindexter/ableton-mcp
- Claims "200+ tools for near-complete Ableton Live Object Model (LOM) coverage". It offers three modes: MCP, REST API for Ollama, OpenAI or any LLM, and a Max for Live in-Ableton chat (needs Suite or M4L). Live 10+, Python 3.8+. Last commit 2026-05-01. My grep counted 128 `@mcp.tool` decorators in Python files, so the "200+" figure may include REST/M4L endpoints. Treat it as the author's claim. — README (repo clone); [GitHub](https://github.com/jpoindexter/ableton-mcp)

**AbletonOSC-based servers** (AbletonOSC = free Remote Script exposing the Live API over OSC/UDP: https://github.com/ideoforms/AbletonOSC)
- Simon-Kansara/ableton-live-mcp-server: Python/uv/fastmcp plus an OSC daemon. ~337 stars per SourcePulse. — [GitHub](https://github.com/Simon-Kansara/ableton-live-mcp-server), [SourcePulse](https://www.sourcepulse.org/projects/2553695)
- adindotdev/ableton-mcp: Node.js, Claude Code → stdio → OSC/UDP → AbletonOSC. Live 11+. — [Glama](https://glama.ai/mcp/servers/@adindotdev/ableton-mcp)
- mrinalghosh/ableton-mcp: targets Live 12. Bundles a forked AbletonOSC with an added BrowserHandler for list_browser and load_device. — [Glama](https://glama.ai/mcp/servers/mrinalghosh/ableton-mcp)
- Dysron/ableton-mcp: macOS only. Uses AppleScript GUI automation, so export works but needs Accessibility permission. — [Glama README](https://glama.ai/mcp/servers/@Dysron/ableton-mcp/blob/f2b285e946baca9f3b50056d6bf0b1a6f1ec7ee9/README.md)
- Many more small forks are listed on Glama, e.g. [rephlex187/Ableton-Live-MCP](https://glama.ai/mcp/servers/rephlex187/Ableton-Live-MCP) and [fabian-tinkl/AbletonMCP on LobeHub](https://lobehub.com/mcp/fabian-tinkl-abletonmcp).

**Official / vendor AI**
- Anthropic "Claude for Creative Work" (Apr 28, 2026, updated May 1): connectors for Ableton, Adobe, Affinity by Canva, Autodesk Fusion, Blender, Resolume Arena and Wire, SketchUp and Splice. The Ableton connector "grounds Claude's answers in official product documentation for Live and Push." — [Anthropic](https://www.anthropic.com/news/claude-for-creative-work)
- Secondary write-ups say the Ableton connector does NOT control Live in real time, generate or edit MIDI in your set, drive Push, or read session state. — [search snippets: findskill.ai](https://findskill.ai/blog/anthropic-claude-ableton-connector-music-producer-honest-walkthrough/), [jamesm.blog](https://jamesm.blog/music-production/claude-ableton-connector/), [Mixmag MENA](https://mixmagmena.com/read/claude-is-now-integrated-into-ableton-live-and-splice-through-anthropic-s-new-connectors-tech)
- Ableton itself: no official AI or agent control feature found. Live 12.4 shipped May 5, 2026, and 12.4.6 on Sep 15, 2026. — [Ableton blog](https://www.ableton.com/en/blog/live-12-4-is-out-now/), [Release notes](https://www.ableton.com/en/release-notes/live-12/)

### Inferences
- If the user's assistant shows tool names like `get_song_properties`, `create_midi_clip`, `rollback_by_history_id` or `init_ableton_js`, they are on xiaolaa2's Ableton Copilot. Names like `get_session_info`, `create_clip`, `load_instrument_or_effect` point to ahujasid. Names prefixed `ppal-` point to Producer Pal.
- If the "Ableton Copilot" they have is actually Claude's official Ableton connector, it only answers questions from the manual and cannot touch the set. That is the single most important distinction for them.
- Maintenance ranking (Oct 2026): Producer Pal and ahujasid are very active, xiaolaa2 is slow (one npm release in 15 months, unreleased fixes on main), and uisato and jpoindexter have been quiet since May 2026.

### Gaps
- Exact current star counts for uisato, Simon-Kansara and jpoindexter (aggregator figures only). No Reddit r/ableton threads surfaced in search, so first-hand user sentiment is missing.
- Whether the official Anthropic Ableton connector was later extended with control tools after May 2026: not found.

## 2. What each one exposes (capabilities), plus limitations and bugs

### Takeaway
All of them can read the set, create tracks and clips, write MIDI notes, load native devices from the browser, set tempo, mix values and transport. None can listen to audio or render or export a mix (except AppleScript hacks). Third-party VST/AU internals are generally not controllable. Automation and envelopes are weak or missing in most (Producer Pal: none; uisato: buggy; jpoindexter: claims clip envelopes). Ableton Copilot is distinctive for recording by time range and its note-only rollback history.

### Cited Findings
**Ableton Copilot (xiaolaa2): tool names from source (src/tools/*.ts, main branch Jul 2026)**
- Song: `get_song_properties`, `set_song_property` (tempo etc.), `get_song_view_properties`, `set_song_view_property`, `create_track` (MIDI/audio/return), `delete_track`, `duplicate_track`, `record_by_time_range` ("Opens Ableton's audio record button and starts playback from start_time to end_time"). — repo source
- Track: `get_track_properties`, `set_tracks_property` (batch mute/solo/arm/color/name), `create_midi_clip`, `create_audio_clip` (from a sample file path), `duplicate_clip_to_track`, `delete_clip`, `delete_device`. Main-only, unreleased on npm: `get_track_overview`, `create_clips_batch`, `get_track_sends`, `set_track_send`. — repo source; [commits](https://github.com/xiaolaa2/ableton-copilot-mcp/commits/main)
- Clip: `get_clip_properties`, `get_clip_notes`, `add_notes_to_clip`, `modify_clip_notes`, `replace_clip_notes`, `remove_clip_notes`, `remove_notes_by_ids`, `set_clips_property` (name, color, looping, loop start/end), `crop_clip`, `duplicate_clip_loop`, `duplicate_clip_region`. Main-only: `write_notes_to_clips`, `read_notes_from_clips` (batch). — repo source
- Devices and browser: `list_resources` (browser by type), `load_device` (audio effect, instrument, plugin, drums, MIDI effect, sounds), `get_device_properties`, `modify_device_parameter_value` (tool description: "only support built-in Live devices"). — repo source
- History: `get_operation_histories`, `get_snapshot_by_history_id`, `rollback_by_history_id`. Rollback "currently only supports note operations". Roadmap: automatic envelope adjustment and more snapshot types (track properties, device parameters). — [README](https://github.com/xiaolaa2/ableton-copilot-mcp)
- Misc: `get_application_info`, `init_ableton_js` (installs the Remote Script). — repo source
- Not present: arrangement-view clip placement, locators, automation envelopes, scenes, scene firing, playback start/stop as a dedicated tool. My tool grep found none; the song property setters may cover some transport fields via ableton-js but this is unverified.
- Known bug fixed only on main: "load_device can silently land on the wrong track" (race), fixed Jul 3, 2026. — [commits](https://github.com/xiaolaa2/ableton-copilot-mcp/commits/main)
- Warning: AI edits to MIDI clips "may result in the loss of original notes and cannot be undone with Ctrl + Z". Ask the AI to roll back instead. — [README](https://github.com/xiaolaa2/ableton-copilot-mcp)
- Compatibility: Live 12.1.10 "Tested and working". 11.x and 10.x "Not tested yet". It depends on ableton-js (v4.0.4 since 0.9.0). — [README](https://github.com/xiaolaa2/ableton-copilot-mcp)

**ahujasid/ableton-mcp: tools in MCP_Server/server.py (v1.4.5)**
- Read: `get_session_info`, `get_session_snapshot`, `get_track_info`, `get_clip_notes`, `get_device_parameters`, `get_remote_script_info`, `get_browser_tree`, `get_browser_items_at_path`, `get_arrangement_clips`. — [server.py](https://raw.githubusercontent.com/ahujasid/ableton-mcp/main/MCP_Server/server.py)
- Write: `create_midi_track`, `create_audio_track`, `set_track_name`, `create_clip`, `create_audio_clip`, `add_notes_to_clip`, `clear_notes_from_clip`, `set_clip_name`, `set_arrangement_clip_name`, `set_tempo`, `load_instrument_or_effect` (by browser URI), `load_drum_kit`, `set_device_parameter`, `delete_clip`. — same
- Transport and arrangement: `fire_clip`, `stop_clip`, `start_playback`, `stop_playback`, `switch_to_arrangement_view`, `set_arrangement_time`, `duplicate_to_arrangement`, `create_locator`. — same
- Feedback and dataset tools: `set_dataset_consent`, `submit_intent`, `rate_last_action`, `prefer_candidate`, `reject_last_action`, `record_audition`. — same
- README: two-way socket. It can create and modify MIDI/audio tracks, load instruments, effects and sounds from the library, edit MIDI clips, build arrangements (intro/buildup/drop/breakdown/outro) in Arrangement View, and control transport and tempo. "Designed for Ableton's default devices and browser items". Complex arrangements may need smaller steps, and timeouts call for simplifying requests. — [README](https://github.com/ahujasid/ableton-mcp)
- Privacy: anonymous telemetry (install ID, session ID, tool names, success, duration) is **on by default**. Dataset recording (prompts, MIDI, names, device settings, possibly published as an open dataset) is off by default and opt-in. Disable with `ABLETON_MCP_DISABLE_TELEMETRY=true`, or `ABLETON_MCP_DISABLE_DATASET=true` for dataset only. — [README](https://raw.githubusercontent.com/ahujasid/ableton-mcp/main/README.md). Note: the Sep 22 commit title "update: opt in telemetry" seems to conflict with the README's "on by default" wording. The README text was current when checked.
- Since Sep 22, 2026 the bridge binds to loopback only, a security fix. — [commits](https://github.com/ahujasid/ableton-mcp/commits/main)
- No audio export or rendering, and third-party plugins are limited. — search snippet of [mcp.directory guide](https://mcp.directory/blog/ableton-mcp-complete-guide-2026) (secondary)

**Producer Pal: tools (docs/features/tools.md)**
- `ppal-connect`, `ppal-context` (project, global and memory context), `ppal-playback`, `ppal-library` (browser; lists installed plug-ins on Live 12.4+), `ppal-select`, `ppal-delete`, `ppal-duplicate`, `ppal-read-live-set`/`ppal-update-live-set`, `ppal-create-track`/`ppal-read-track`/`ppal-update-track`, `ppal-create-scene`/`ppal-read-scene`/`ppal-update-scene`, `ppal-create-clip`/`ppal-read-clip`/`ppal-update-clip` (incl. audio clips: gain, pitch, warp), `ppal-create-device`/`ppal-read-device`/`ppal-update-device` (device-specific controls for Drift, Wavetable, Simpler, Meld, Compressor, EQ Eight, Hybrid Reverb, Roar, Spectral Resonator), `ppal-live-api` (raw Live API), `spawn_subagent`. — [docs tools](https://github.com/adamjmurray/producer-pal/blob/main/docs/features/tools.md), [examples](https://github.com/adamjmurray/producer-pal/blob/main/docs/features/examples.md)
- Documented limitations (design boundaries, not bugs): it cannot read or set VST/AU parameters, so map them via Live's Configure mode and save in a rack. It cannot read or create clip envelopes or arrangement automation; parameters are static only. No audio analysis or synthesis (no audio-to-MIDI or key detection). Looped arrangement clips are lengthened by tiling copies. Mid-arrangement time-signature changes are invisible and arrangement bar positions go wrong after them, so "don't arrange with Producer Pal in a Set that changes meter". Only one Drum Rack pitch map per track. — [limitations.md](https://github.com/adamjmurray/producer-pal/blob/main/docs/features/limitations.md)
- Known issues: Live groups all Live-API changes into **one undo step until you interact with Live's UI**, so Cmd/Ctrl+Z may undo several AI requests at once, while heavy operations may split into multiple steps. Live's memory grows slowly over very long sessions (~3 KB per object lookup). Project context can be lost when upgrading from devices older than 2.1.0. — [known-issues.md](https://github.com/adamjmurray/producer-pal/blob/main/docs/support/known-issues.md)

**uisato/ableton-mcp-extended**
- Session and transport, scenes (create, delete, rename, fire), tracks (volume, pan, mute, solo, arm), MIDI batch edits (transpose, quantize). Automation: "Add and clear automation points for any device parameter within a clip. [This feature isn't working perfectly yet.]" Roadmap: fix automation point placement bugs, VST support, Arrangement View. ElevenLabs TTS and SFX import. — README (repo clone); [Glama](https://glama.ai/mcp/servers/uisato/ableton-mcp-extended)

**jpoindexter/ableton-mcp**
- README feature list: arrangement loop, locators and scrub; clip automation envelopes (get/set/clear); session automation record and arrangement overdub; record modes; mixing; punch in/out; "AI music helpers". — [README](https://github.com/jpoindexter/ableton-mcp)

### Inferences
- In Live's API (shared by all these tools), the Ctrl+Z behavior described in Producer Pal's known-issues likely applies to every MCP server. It is consistent with Copilot's warning that note edits "cannot be undone with Ctrl+Z". Saving or versioning the set is the real safety net.
- For automation-heavy work (filter sweeps, risers), jpoindexter or uisato are the candidates, but expect bugs. Otherwise do automation by hand.
- For Copilot users, the practical gaps are arrangement view (no clip placement in the timeline) and automation. Those parts stay manual, or need a second server such as ahujasid for `duplicate_to_arrangement` and `create_locator`. Never run two servers that share the same Remote Script port.

### Gaps
- Open GitHub issues for xiaolaa2 were not enumerated (API blocked). Unknown whether the Live 12.4 update broke ableton-js; Copilot is only declared tested on 12.1.10.
- No independent benchmark of note-writing quality across models was found.

## 3. Setup requirements (Live version, Remote Script, Node/Python, client config)

### Takeaway
Each server has two halves: something inside Live (a Remote Script selected as a Control Surface, or a Max for Live device) and an MCP server process launched by the desktop client (Claude Desktop, Claude Code, Cursor, etc.). The claude.ai website cannot reach a local Live session without a tunnel. Producer Pal documents a web-tunnel route.

### Cited Findings
**Ableton Copilot (xiaolaa2)**
- Needs Node.js v20+ with npx and Ableton Live 12 (12.1.10 tested). — [README](https://github.com/xiaolaa2/ableton-copilot-mcp)
- Install the Remote Script one of three ways: `npx @xiaolaa2/ableton-copilot-mcp --install-scripts` (or `-is`); have the AI call `init_ableton_js`; or manually copy ableton-js's `midi-script` folder into User Library → Remote Scripts renamed `AbletonJS`. Then Live → Preferences → Link/MIDI → MIDI → Control Surface = **AbletonJS**. — [README](https://github.com/xiaolaa2/ableton-copilot-mcp)
- Client config (Cursor example, same shape for Claude Desktop and Cherry Studio): `"ableton-js-mcp": {"command": "npx", "args": ["-y", "@xiaolaa2/ableton-copilot-mcp"]}`. Use `@latest` to auto-update. Optional env `BASE_PATH` sets where logs, operation history and snapshots are stored (e.g. `D:\\ableton_copilot_mcp`). — [README](https://github.com/xiaolaa2/ableton-copilot-mcp)

**ahujasid/ableton-mcp**
- Needs Live 10+, Python 3.8+ and uv (`brew install uv` on macOS). — [README](https://github.com/ahujasid/ableton-mcp)
- Claude Desktop (Settings → Developer → Edit Config): `{"mcpServers": {"AbletonMCP": {"command": "uvx", "args": ["ableton-mcp"]}}}`. Cursor: command `uvx ableton-mcp`. Claude Code: `claude mcp add AbletonMCP uvx ableton-mcp`. — [README](https://github.com/ahujasid/ableton-mcp)
- Remote Script: `uvx --from ableton-mcp ableton-mcp-install-script` (`--list-targets` and `--target` are available). It installs to macOS `~/Music/Ableton/User Library/Remote Scripts/AbletonMCP/` or Windows `C:\Users\[Username]\Documents\Ableton\User Library\Remote Scripts\AbletonMCP\`, and backs up an existing `__init__.py`. In Live, go to Link, Tempo & MIDI, set Control Surface = AbletonMCP and Input/Output = None. Restart Live after installing or upgrading. Run only one MCP instance (not Cursor and Claude Desktop at once). — [README](https://github.com/ahujasid/ableton-mcp)
- Setup video: https://youtu.be/iJWJqyVuPS8. — [README](https://raw.githubusercontent.com/ahujasid/ableton-mcp/main/README.md)

**Producer Pal**
- Requires **Live 12.3+ with Max for Live** (12.4+ recommended). Download `Producer_Pal.amxd` from releases and drop it on a track. Clients: Claude Desktop (an extension is available), ChatGPT app, Antigravity (Gemini), LM Studio Bionic (offline), the built-in browser Chat UI (Gemini, OpenAI, Ollama, Anthropic, OpenRouter, Mistral via API key), Claude Code, Codex CLI, Gemini CLI and Mistral Vibe. Claude Code, Codex and Gemini CLI can use an "Agent Skill" instead of MCP. claude.ai, ChatGPT web and Le Chat work via a web tunnel. To start, say "connect to ableton". — [installation.md](https://github.com/adamjmurray/producer-pal/blob/main/docs/installation.md)

**uisato extended**: Live 11+ (any edition), Python 3.10+. Git clone, `pip install -e .`, copy the Remote Script, set Control Surface "AbletonMCP". — README (repo clone)

**AbletonOSC route**: copy AbletonOSC into User Library/Remote Scripts and select it as a Control Surface. — [Glama listing](https://glama.ai/mcp/servers/@Simon-Kansara/ableton-live-mcp-server)

### Inferences
- Remote Script MCPs (Copilot, ahujasid, AbletonOSC) work in every Live edition. Producer Pal and jpoindexter's M4L mode need Max for Live (Suite, or Standard plus the M4L add-on).
- Copilot users who want the Jul 2026 batch tools or the load_device fix must build from source (`git clone`, `npm i`, `npm run build`, point the client at `node dist/main.js`) until npm publishes a release newer than 0.9.0.
- Common first-run failure: the Control Surface was not selected, or Live was not restarted after copying the script.

### Gaps
- Official Claude Desktop config for Copilot is not shown verbatim in the README (only Cursor). The shape is standard `mcpServers`.

## 4. Practical workflows, example prompts, safety

### Takeaway
These tools work best in small, explicit, verifiable steps: read the set first, then create one part at a time, name tracks, give key/tempo/bar counts, and check results. Treat the AI as a fast MIDI and setup assistant, not a mix engineer. Save a versioned copy before each session, because undo is unreliable.

### Cited Findings
- ahujasid example prompts: "Create an 80s synthwave track" ([demo](https://youtu.be/VH9g66e42XA)); "Create a full arrangement with an intro, buildup, drop, breakdown, and outro"; "Create a new MIDI track with a synth bass instrument"; "Add reverb to my drums"; "Create a 4-bar MIDI clip with a simple melody"; "Load an 808 drum rack into the selected track"; "Add a jazz chord progression to the clip in track 1"; "Set the tempo to 120 BPM"; "Play the clip in track 2". — [README](https://github.com/ahujasid/ableton-mcp)
- Producer Pal recommended flow: start with "connect to ableton", then "what are all the things you can do with your Ableton Live tools?", then read-only questions ("what's in my Live Set?", "what devices are on the bass track, and how are they set?", "which clips are in scene 3?"). — [examples.md](https://github.com/adamjmurray/producer-pal/blob/main/docs/features/examples.md)
- Producer Pal: the "highest-leverage thing" is project context, e.g. "save this to the project context: this track is a 140bpm neurofunk tune in F minor. 'Reese' is the main bass track... Keep the intro sparse" and "add to the project context: the arrangement is intro (1-16), drop (17-48), breakdown (49-64)". Global context example: "remember globally: I work in 4-bar loops, I hate hard-quantized hi-hats, and I never want you to touch my master chain". — [examples.md](https://github.com/adamjmurray/producer-pal/blob/main/docs/features/examples.md)
- Producer Pal device-chain prompts: "create a MIDI track called 'Synth Lead'" → "add a Wavetable instrument to it" → "set the filter cutoff to 800 Hz and add an Echo after it" → "mute that track and set its color to purple". Samples: "find me a rhodes loop", "create an audio clip using that kick sample on the Drums track", "pitch shift it up 5 semitones and loop it". Most work is editing existing MIDI rather than generating new parts. — [examples.md](https://github.com/adamjmurray/producer-pal/blob/main/docs/features/examples.md)
- VST workaround: map plug-in parameters with Live's Configure mode and save as a rack preset so the AI can turn them. — [limitations.md](https://github.com/adamjmurray/producer-pal/blob/main/docs/features/limitations.md)
- Safety: "Always save your work before extensive experimentation." Break complex arrangements into smaller steps, and restart Claude and Live on persistent errors. — [ahujasid README](https://github.com/ahujasid/ableton-mcp). "Save your Live Set before big changes. Click somewhere in Live's UI between requests if you want separate undo steps." — [Producer Pal known issues](https://github.com/adamjmurray/producer-pal/blob/main/docs/support/known-issues.md). Copilot: use `rollback_by_history_id` for notes, since Ctrl+Z will not help. — [Copilot README](https://github.com/xiaolaa2/ableton-copilot-mcp)
- Privacy: set names, track and clip names, MIDI, device and plugin lists, browser and sample paths may be sent to the model. ElevenLabs integration sends data to a third-party API. — aggregator note on [heyclau.de](https://heyclau.de/entry/mcp/ableton-mcp-extended) (secondary)

### Inferences (practical playbook for an Ableton Copilot user; derived from tool sets above, not tested)
- **Session start:** "Read the song properties (tempo, key/scale, length) and give me an overview of all tracks, clips and devices." With Copilot this uses `get_song_properties` and `get_track_properties`; `get_track_overview` is only available if built from main.
- **Drums:** "Create a MIDI track named 'Drums', load a Drum Rack (e.g. 808 Core Kit) from the browser, create a 2-bar clip in slot 1, and write a 4-on-the-floor kick, claps on 2 and 4, 16th hats with velocity alternating 100/70, slight swing. List the pads you used." Use explicit pitches (C1 kick = 36, D1 snare = 38, F#1 closed hat = 42) when the rack mapping is unknown.
- **Chords and bass:** "In F minor at 124 BPM, create an 8-bar clip on a new 'Keys' track with Fm9 – Db maj7 – Ab – Eb/G voicings, one chord per 2 bars, and a separate 'Bass' clip following the roots in 8ths with octave jumps." Then: "Show me the notes you wrote," and "Humanize velocities ±10, don't touch timing."
- **Variation:** "Duplicate clip 1 to slot 2 and make a fill variation in the last bar only." For Copilot, use `duplicate_clip_to_track`, `duplicate_clip_region` and `modify_clip_notes`.
- **Sound design (native devices only):** "Load Wavetable on 'Lead', list its parameters, then set filter cutoff lower and add Echo + Reverb with 20% dry/wet." Copilot's `modify_device_parameter_value` supports built-in Live devices only.
- **Mix assist (static values):** "Set the Drums track volume to -6 dB, Bass sends to Return A at about 15%." For Copilot, sends need the main-branch build. Ask the AI to read values back.
- **Recording:** with Copilot, "arm track 'Vox' and record from bar 9 to bar 17" maps to `set_tracks_property` (arm) plus `record_by_time_range`.
- **Recovery:** "Show the last 10 operations and roll back the note change on 'Keys'." This uses `get_operation_histories` and `rollback_by_history_id`, which work for notes only.
- **Habits:** save-as a versioned copy (e.g. `song_v03_ai.als`) before each AI session. Work in Session View clips, then arrange yourself. Keep requests to one track or part per message to avoid timeouts. Name tracks so the AI can refer to them reliably.

### Gaps
- No Reddit or forum first-hand reports could be retrieved, and several blogs/tutorials were blocked from fetching: mcp.directory guide ([link](https://mcp.directory/blog/ableton-mcp-complete-guide-2026)), Daniel Raffel TIL Mar 14, 2026 ([link](https://danielraffel.me/til/2026/03/14/control-ableton-live-with-natural-language-mcp-setup/)), findskill.ai course ([link](https://findskill.ai/courses/ai-for-music-producers-claude-ableton/)), German tutorial "KI im Studio" ([link](https://sinee.de/en/index.php/moorl-magazine/article/b541f53f1a96415d9560ff328851f6dd)).
- No demo video specific to xiaolaa2's Copilot was located (the README references an uploaded video via a Jun 2025 docs commit, but no URL was extracted).
- Demo and tutorial video URLs found: ahujasid setup https://youtu.be/iJWJqyVuPS8 and synthwave demo https://youtu.be/VH9g66e42XA; uisato demo https://www.youtube.com/watch?v=7ZKPIrJuuKk; uisato channel https://www.youtube.com/@uisato_. Producer Pal docs reference "video tutorials" (at producer-pal.org) without a URL captured here.
