# KPI Coach

A Claude skill that helps founders set one good KPI — or honestly review the KPIs they already track.

**A KPI is a unit you steer by, not a goal you hit.** The most common founder mistake is to measure what the company *did* — activity, acquisition, revenue — instead of the value the customer *got*, and to assert that a metric matters instead of proving it. This skill drags the metric from "looks like progress" to "a value event we've shown predicts retention."

## What it does

A single entry point for choosing or grading a KPI. Trigger it when a founder asks what to measure, wants to pick or validate a north-star / value / activation metric, or wants their existing KPIs critiqued.

It works in two modes:

| Mode | Owns |
|---|---|
| SET | Find and validate a candidate value event (the "magic moment"), then run the checker |
| REVIEW | Take the KPIs a founder already tracks and grade each against the checker, honestly |

Under the hood it runs a nine-gate checker (value-exchange, predicts retention, leading, grows within existing customers, ungameable, count-not-percentage, and more), proves the retention link with a cohort analysis, and keeps a KPI distinct from a goal/OKR.

Out of scope: recurring trend/scorecard review of an already-agreed KPI (`metrics-review`), portfolio company check-ins (`company-check-in`), data-room / diligence market work (`data-room-coach`), and writing instrumentation or tracking plans in code (the `product-tracking` skills).

## Install

Pick the option that matches your comfort level. All three end up at the same place — KPI Coach loaded into Claude.

| If you... | Use |
|---|---|
| just want to download a zip and click upload | [Option A — One-click zip](#option-a--one-click-zip-no-terminal-no-git) |
| are comfortable in the terminal and use Claude Code | [Option B — Claude Code plugin](#option-b--claude-code-plugin) |
| want to clone the repo and copy folders manually | [Option C — Manual git install](#option-c--manual-git-install) |

---

### Option A — One-click zip (no terminal, no git)

The easiest way. You'll download one zip file and upload it to Claude. No command line, no GitHub account, no git.

**Step 1 — Download the skill**

Go to the [latest release](https://github.com/andresbarreto-techstars/kpi-coach/releases/latest) and download `kpi-coach.zip`.

Direct link (always points to the most recent build): https://github.com/andresbarreto-techstars/kpi-coach/releases/latest/download/kpi-coach.zip

**Step 2 — Upload it to Claude**

Where you upload depends on which Claude product you're using:

<details>
<summary><b>Claude.ai (web)</b></summary>

1. Go to [claude.ai](https://claude.ai) and sign in.
2. Click your profile (bottom-left or top-right depending on the layout) → **Settings**.
3. Open **Capabilities** → **Skills** (the menu may also call it **Custom skills**).
4. Click **Add skill** (or **Upload skill** / **Create skill** / the **+** button).
5. Drag `kpi-coach.zip` onto the upload area, or click to browse and select it.
6. Wait for the green checkmark / "uploaded" confirmation.

The skill is now available in any new conversation. To trigger it, just ask Claude something like *"is this a good KPI?"*

</details>

<details>
<summary><b>Claude desktop app / Cowork</b></summary>

1. Open the Claude desktop app.
2. Open **Settings** (cog icon).
3. Go to **Plugins & Skills** (or **Capabilities**).
4. Click **Add custom skill** / **Upload skill** / the **+** button.
5. Drag `kpi-coach.zip` onto the upload area, or click to browse and select it.
6. Confirm when it appears in your installed skills list.

The skill is now available in any new conversation. To trigger it, just ask Claude something like *"is this a good KPI?"*

</details>

**Step 3 — Update later**

When the skill gets updated, just come back to the [latest release page](https://github.com/andresbarreto-techstars/kpi-coach/releases/latest), download the new `kpi-coach.zip`, and re-upload it the same way. Claude replaces the old version.

> **Don't see a Skills / Plugins section in your settings?** Custom skill upload may not be available in every Claude plan or product yet. If that's you, try Option B or Option C, or check Anthropic's [help docs](https://support.claude.com) for the current way to add custom skills.

---

### Option A.5 — Manual zip from this repo (fallback if Releases is empty)

If the Releases page hasn't been built yet, or you prefer to grab files directly from the repo, follow this path. Slightly more steps than Option A but no command line.

1. On the repo's [main page](https://github.com/andresbarreto-techstars/kpi-coach), click the green **Code** button.
2. Click **Download ZIP** at the bottom of the dropdown. This downloads the whole repo as `kpi-coach-main.zip`.
3. Open the downloaded zip (double-click on Mac/Windows). You'll get a folder called `kpi-coach-main`.
4. Inside that folder, find `skills/kpi-coach/`. **This** is the skill — not the parent folder.
5. Compress just that `kpi-coach` folder:
   - **Mac:** right-click `kpi-coach` → **Compress "kpi-coach"**. You'll get `kpi-coach.zip`.
   - **Windows:** right-click `kpi-coach` → **Send to** → **Compressed (zipped) folder**. You'll get `kpi-coach.zip`.
6. Upload that `kpi-coach.zip` to Claude using the steps in Option A → Step 2.

---

### Option B — Claude Code plugin

If you use [Claude Code](https://docs.claude.com/en/docs/claude-code), this is the cleanest path. The plugin auto-updates from this repo.

```
/plugin marketplace add andresbarreto-techstars/kpi-coach
/plugin install kpi-coach@kpi-coach
```

To pick up the latest version later:

```
/plugin marketplace update kpi-coach
```

---

### Option C — Manual git install

For terminal users who prefer dropping the skill folder directly into their Claude skills directory.

```bash
git clone https://github.com/andresbarreto-techstars/kpi-coach.git
cp -r kpi-coach/skills/kpi-coach ~/.claude/skills/
```

To update later:

```bash
cd kpi-coach
git pull
cp -r skills/kpi-coach ~/.claude/skills/
```

## How to use it

Once installed, just ask Claude something like:

- "Is this a good KPI?"
- "What's the right KPI for us to track?"
- "Help me pick a north star metric"
- "Review my KPIs — are we measuring the right thing?"
- "How do I know my metric predicts retention?"
- "We keep confusing KPIs and goals"

The skill figures out whether you're **setting** a KPI from scratch or **reviewing** ones you already track, separates KPIs from goals/OKRs when they're blurred, runs the nine-gate checker, and tells you exactly what to instrument to prove the retention link.

## Repo layout

```
kpi-coach/
├── .claude-plugin/
│   ├── plugin.json                  ← plugin manifest
│   └── marketplace.json             ← marketplace manifest
├── .github/workflows/
│   └── release.yml                  ← auto-publishes the zip to Releases
├── skills/
│   └── kpi-coach/
│       ├── SKILL.md                 ← workflow / entry point
│       ├── references/
│       │   ├── checker.md           ← the nine gates + verdict logic
│       │   ├── retention-proof.md   ← the retention-correlation analysis
│       │   ├── kpi-vs-okr.md        ← KPI vs goal/OKR, count-not-% rule
│       │   ├── failure-archetypes.md← fast catches for REVIEW mode
│       │   └── literature.md        ← grounding + sources
│       └── assets/
│           └── what-makes-a-good-kpi.pptx  ← founder-facing summary slide
├── README.md
└── LICENSE
```

## License

MIT — see [LICENSE](LICENSE).
