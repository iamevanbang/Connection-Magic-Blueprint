# Connection Magic Blueprint

An audience-first, skills-only ChatGPT and Codex plugin for researching what people currently care about and turning those insights into high-retention Instagram Reels and TikTok scripts.

Connection Magic Blueprint separates **who creates the content** from **who the content is meant to serve**. It researches the end audience before suggesting ideas, then guides the user from audience clarity to a platform-specific production script with one intentional call to action.

## Why it exists

Generic content generators frequently make two costly mistakes:

1. They convert a detailed audience description into a vague, jargon-heavy niche.
2. They generate content for the creator instead of the creator's customers, clients, or community.

For example, a real estate agent normally needs content for home buyers, sellers, and homeowners—not advice written for content creators or other real estate agents. Connection Magic Blueprint makes that distinction before research begins and carries it through every topic and script.

## What it does

- Interprets the creator's position, target audience, desired outcome, and relevant exclusions.
- Uses live web search when it is available before describing pain points as researched or trending.
- Identifies 10 evidence-supported audience pain points in language the audience recognizes.
- Generates 20 focused short-form video topics mapped to those pain points.
- Accepts a selected topic or the user's own rough outline.
- Creates scripts for Instagram Reels, TikTok, or both platforms.
- Supports Keyword, Follow, General, Community, Link/Bio, Save/Bookmark, and Custom CTAs.
- Produces hooks, timestamps, spoken audio, visual direction, text overlays, captions, and SEO terms.
- Applies platform-specific timing, pacing, CTA behavior, and visual safe zones.

## Guided workflow

### Step 1 — Audience research

The user enters a niche or describes the people they want to reach. The plugin distinguishes the creator from the intended viewer, confirms its interpretation, and researches the audience's current questions, frustrations, objections, risks, and desired outcomes.

The result includes:

- A concise audience interpretation
- 10 researched pain points
- 20 potential video topics
- A compact list of source links

If live search is unavailable, the plugin must say so clearly and request permission before offering an inference-only topic set. It never disguises generic suggestions as current research.

### Step 2 — Topic or rough outline

The user replies with a topic number, pastes one of the suggested topics, or provides an original idea or outline.

### Step 3 — Platform

The user selects:

- Instagram Reels
- TikTok
- Both

When Both is selected, the plugin creates two meaningfully different scripts rather than relabeling the same script.

### Step 4 — CTA outcome

The user chooses one primary action:

| CTA | Intended outcome |
| :--- | :--- |
| Keyword | Comment a relevant word for a clearly defined benefit |
| Follow | Follow for a specific recurring result or subject |
| General | Use the most natural next action for the topic and platform |
| Community | Answer a question, share an experience, or request a video reply |
| Link/Bio | Visit a clearly described resource |
| Save/Bookmark | Save the information for a foreseeable future need |
| Custom | Use the user's requested action and wording |

### Step 5 — Production script

The final output includes:

1. Short-Form Video Concept & Target Runtime
2. Production Script table
3. Three Hook Variations for Testing
4. Caption & CTA Setup

## Platform targets

| Requirement | Instagram Reels | TikTok |
| :--- | :--- | :--- |
| Runtime | 45–58 seconds | 61–65 seconds |
| Spoken length | 110–135 words | 145–160 words |
| Style | Polished, clean, clear audio | Raw, conversational, lightly unfiltered |
| Default CTA | Keyword | Community |
| Text placement | Central 1080 × 1440 px safe zone | Upper-middle; right 150 px and bottom 30% clear |

CTA selection overrides the platform default. The plugin uses one primary CTA and does not stack competing actions.

## Retention structure

Every script follows a high-retention narrative bridge:

| Time | Purpose |
| :--- | :--- |
| 0:00–0:03 | Pattern-interrupt visual, absolute hook, and a specific open loop |
| 0:03–0:12 | Core problem, tension, stakes, or misconception |
| 0:12–0:15 | Genuine narrative pivot or reframe |
| 0:15–0:45 | Three sequential, actionable value points |
| 0:45–0:53 | Climax, proof, core realization, and loop closure |
| 0:53–end | One platform-appropriate CTA |

Visual changes, scale cuts, b-roll, gestures, or text beats are planned every three to four seconds without forcing frantic pacing.

## Skills-only architecture

This package intentionally contains no MCP server and no custom iframe interface. It relies on the model and native tools available in the user's current ChatGPT or Codex session.

That means:

- No developer-owned OpenAI API key
- No usage-based AI charges to the publisher
- No developer-controlled backend
- No publisher database or prompt logs
- No runtime path for the publisher to collect user inputs or generated scripts

OpenAI account, workspace, history, memory, web-search, and data-control settings still apply.

## Example requests

```text
Research first-time home buyers and give me 20 video topics.
```

```text
My audience is stay-at-home dads looking for legitimate ways to make money online.
```

```text
Turn topic 7 into separate Instagram and TikTok scripts. Use a Follow CTA.
```

```text
Write an Instagram Reel from this rough outline and use the keyword CLARITY.
```

## Repository structure

```text
.agents/plugins/marketplace.json
plugins/connection-magic-blueprint/
├── .codex-plugin/plugin.json
└── skills/connection-magic-blueprint/
    ├── SKILL.md
    ├── agents/openai.yaml
    └── references/
        ├── audience-research.md
        └── script-spec.md
submission/
└── test-cases.md
```

## Key files

- `plugin.json` defines the plugin's identity, listing metadata, capabilities, and starter prompts.
- `SKILL.md` controls activation, intake, audience interpretation, step order, voice, and quality checks.
- `audience-research.md` defines source standards, research-status labels, pain-point ranking, and topic-generation safeguards.
- `script-spec.md` defines platform runtimes, safe zones, CTA behavior, production tables, hooks, and captions.
- `test-cases.md` contains positive, negative, and boundary cases for pre-submission testing.

## Privacy statement

> Connection Magic Blueprint does not transmit or store user prompts, audience information, research queries, or generated scripts on developer-controlled infrastructure. Processing occurs within the user's ChatGPT or Codex session and remains subject to the user's OpenAI account or workspace data settings.

## Development status

Version `0.1.0` is the initial skills-only implementation. The skill and plugin manifests pass their respective structural validators. Behavioral testing should be completed in a clean conversation before public submission.

## Author

Created by **Evan Bang**.
