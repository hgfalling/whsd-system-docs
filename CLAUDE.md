# WHSD Bridge System Documentation Project

## What This Is

Jerrod Ankenman and his bridge partner Bill Chen play a custom bidding system called WHSD (Weak Hearts, Strong Diamonds). The system notes are scattered across multiple Google Docs spanning 13+ years. This project consolidates everything into clean, authoritative documentation — one section at a time.

## Project Structure

```
whsd-system-docs/
├── CLAUDE.md              ← You are here
├── references/
│   ├── system_overview.md       ← One-page system summary (read every session)
│   ├── general_principles.md    ← Cross-cutting rules (read every session)
│   ├── section_tracker.md       ← What's done, what's next
│   └── completed_sections/      ← Clean docs produced by this project
├── source_docs/                 ← Downloaded Google Docs (raw input)
└── outputs/                     ← Working area for current session
```

## Session Workflow

Each session tackles ONE section of the system.

### 1. Orient

Always start by reading:
- `references/system_overview.md`
- `references/general_principles.md`
- `references/section_tracker.md`

Then read any completed sections directly relevant to the current work.

### 2. Load Source Material

Read the relevant files from `source_docs/`. Only load what's needed for the current section — don't read everything.

Source doc mapping:

| File | Contents |
|------|----------|
| WHSD.md | Main system doc — **controls on all conflicts** |
| BFD_1_Overview.md | BFD system overview (historical) |
| BFD_2_1C_Modified.md | 1♣ relay structure (use this over the original) |
| BFD_2_1C_Original.md | Original 1♣ (historical reference only) |
| BFD_3_1D.md | Strong diamond relay structure |
| BFD_4_2C.md | BFD's 2♣ = minors (maps to WHSD's 2♦) |
| BFD_5_2NT.md | 2NT opening |
| Other_Agreements.md | NT systems, misc agreements |
| Infernal_BFD.md | Previous consolidation attempt |
| Bill_Spencer_Misc.md | Legacy 1M raises — NOT current for 1M |

### 3. Work Through Sequences

Walk through bidding sequences methodically with Jerrod:
- Present what the source docs say
- Flag ambiguities, conflicts, or gaps
- Ask Jerrod to clarify or decide
- Note any "ask Bill" items

**Style notes:**
- Jerrod is a professional quantitative researcher and co-author of *The Mathematics of Poker*. He thinks about system design in terms of information theory, frequency, and bidding space efficiency. Engage at that level.
- Be direct about messy or contradictory notes.
- When a sequence is underspecified, propose what seems natural and ask for confirmation rather than just flagging it as a gap.
- The system reaches natural bidding fast (1-2 artificial rounds, then judgment). Don't over-specify sequences that should be judgment.
- Watch for cruft — agreements that come up so rarely they're not worth memorizing.

### 4. Produce the Section Document

Create a clean markdown document in `references/completed_sections/`:
- Self-contained — reader shouldn't need other docs to understand the section
- Tables for bidding sequences
- Reference (don't duplicate) general principles and the shortness protocol
- Flag remaining TODOs or "ask Bill" items clearly

### 5. Update Tracking

After completing a section:
- Update `references/section_tracker.md`
- Update `references/general_principles.md` if new cross-cutting rules emerged
- Update `references/system_overview.md` if any system-level facts were corrected

## System Context

**Partner:** Bill Chen

**Key design principle:** One-level openings signal *valuation* (1M = weak, 1D = strong, 1NT = narrow, 1C = medium catchall). Two-level openings signal *shape* (2♣ = majors, 2♦ = minors, 2M = one-suited).

**3rd/4th seat:** Reverts to much more standard 2/1 with weak NT system (specifics TBD).
