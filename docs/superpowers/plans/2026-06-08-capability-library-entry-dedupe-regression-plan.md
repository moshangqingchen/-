# Capability Library Entry Dedupe Regression Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Tighten the current AI super director capability library by reducing entry duplication and adding regression checks for the two newly introduced capabilities.

**Architecture:** This is a documentation maintenance pass. `README.md` remains the practical launch surface, `docs/superpowers/specs/2026-06-07-ai-super-director-master-index-command-map.md` remains the routing map, and each new capability card owns its own trigger, output, self-check, and regression examples.

**Tech Stack:** Markdown documentation, PowerShell verification commands, ripgrep search.

---

### Task 1: README Entry Discipline

**Files:**
- Modify: `README.md`

- [ ] **Step 1: Compress repeated maintenance guidance**

Replace repeated long-form entry language with a short maintenance rule that says README entries must change behavior, not merely list assets.

- [ ] **Step 2: Keep the two new capability entries but make them operational**

Ensure the novel/story import entry points to source analysis, adaptation form choice, and Seedance-safe output. Ensure the prompt humanization entry points to director judgment, visible action, and final prompt lint.

- [ ] **Step 3: Run focused search**

Run: `rg -n "小说/剧情导入|提示词人味|能力库体检|README 只" README.md`

Expected: each new capability has one quick-start/default route, one core asset link, and one operational entry section.

### Task 2: Master Index Routing Consistency

**Files:**
- Modify: `docs/superpowers/specs/2026-06-07-ai-super-director-master-index-command-map.md`

- [ ] **Step 1: Verify the new capability rows are present**

Run: `rg -n "小说/剧情导入|提示词人味" docs/superpowers/specs/2026-06-07-ai-super-director-master-index-command-map.md`

Expected: both capabilities appear in startup order, depth table, and user command routing table.

- [ ] **Step 2: Add routing guardrails if missing**

Novel/story import must not bypass copyright/originality boundaries. Prompt humanization must not replace Seedance final lint; it should run before final lint.

### Task 3: Capability Card Regression Cases

**Files:**
- Modify: `docs/superpowers/specs/2026-06-08-ai-super-director-novel-story-import-adaptation-engine.md`
- Modify: `docs/superpowers/specs/2026-06-08-ai-super-director-prompt-humanization-live-director-optimizer.md`

- [ ] **Step 1: Add regression examples to the novel/story import card**

Add two concise regression cases: one user-original story import, one copyright-unclear imported story. Each case must state expected output fields and failure signs.

- [ ] **Step 2: Add regression examples to the prompt humanization card**

Add two concise regression cases: one abstract emotional prompt, one overloaded multi-variable Seedance prompt. Each case must state expected output fields and failure signs.

- [ ] **Step 3: Run placeholder scan**

Run: `rg -n "TODO|TBD|待补|占位" docs/superpowers/specs/2026-06-08-ai-super-director-novel-story-import-adaptation-engine.md docs/superpowers/specs/2026-06-08-ai-super-director-prompt-humanization-live-director-optimizer.md`

Expected: no matches.

### Task 4: Verification

**Files:**
- Inspect: `README.md`
- Inspect: `docs/superpowers/specs/2026-06-07-ai-super-director-master-index-command-map.md`
- Inspect: the two new capability cards

- [ ] **Step 1: Check local links exist**

Run a PowerShell link check over `README.md` for `D:/创业/超级导演/...` markdown targets.

Expected: no missing linked files.

- [ ] **Step 2: Check git diff scope**

Run: `git diff --stat`

Expected: only this plan, `README.md`, the master index, and the two new capability cards changed.

- [ ] **Step 3: Summarize remaining risk**

Report whether the library is more maintainable, whether any large README duplication remains, and whether goal completion is proven or still active.
