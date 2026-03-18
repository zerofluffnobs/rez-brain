---
created: 2026-03-18
updated: 2026-03-18
tags: [project, superhuman]
---

# Superhuman Pipeline Gap: Linux Adaptation

**Scouted:** 2026-03-18

## Finding

All three existing Superhuman threads (`coder-integration`, `research-infrastructure`, `refiner-validation`) are at `sh-status: review` — waiting for the creator. No threads exist for Phase 1 of the orchestration build order.

**Phase 1 (Linux Adaptation) is the critical path blocker** for the entire pipeline. Two Python files need platform guards before the Tier 1 (thinker) container can run on Fedora 43.

## Gap

| Phase | Status | Thread |
|-------|--------|--------|
| 1. Linux Adaptation | **No thread — created 2026-03-18** | `linux-adaptation.md` |
| 2. Vault repo on homelab | Unthreaded | — |
| 3. Scanner.sh | Covered by coder-integration | Review |
| 4. systemd timer | Specced in plan-orchestration-layer.md | Unthreaded |
| 5. Result harvesting | Covered by coder-integration | Review |
| 6. Observability | Unthreaded | — |

## What I Did

Created two files in `/home/agent/brain/90-Threads/Superhuman/`:

1. **`linux-adaptation.md`** — Thread with Turn 1 analysis. Identifies the two files needing changes, proposes 5 tasks, set to `sh-status: review`.
2. **`plan-linux-adaptation.md`** — Deliverable with exact diffs, audit checklist, test protocol, and build order context.

## The Two Changes

**`lib/collectors.py`:**
```python
if sys.platform == "darwin":
    items.extend(_collect_apple_notes())
```

**`agents/refiner/routing.py`:**
```python
if APPLE_REMINDERS_ENABLED and sys.platform == "darwin":
    _create_reminder(task_title, due_date)
```

## Next Gaps After This

Once Linux Adaptation ships and is tested:
1. **Homelab setup thread** — clone repos to `/srv/ai-repos/`, configure SELinux labels
2. **systemd timer thread** — deploy Phase 4 units (already fully specced in plan-orchestration-layer.md)
3. **Observability thread** — vault status note + journald query patterns
