# WHSD: Shortness Ask Protocol

*This section applies universally wherever a shortness ask occurs in the system. It supersedes any sequence-specific shortness descriptions elsewhere.*

---

## Which Protocol Applies?

| Situation | Protocol |
|-----------|----------|
| Askee has shown **9+ cards in two known suits** | Two-Suiter Shortness Ask |
| Otherwise (only one suit known, or fewer than 9 cards placed) | Standard Shortness Ask |

---

## Two-Suiter Shortness Ask

Applies when askee has shown 9+ cards in two known suits. There are only two candidate suits for shortness.

**Convention: If askee could have 2-2 in the other two suits, then 3NT (if available) shows "no shortness" and is ignored in the step pattern. 

### Step Responses

| Step | Meaning | What happens next |
|------|---------|-------------------|
| **3NT** | No shortness | — |
| **Step 1** | Exactly one shortness, in the **lower** ranking suit | Asker can relay (see below) |
| **Step 2** | Singleton in the **higher** ranking suit only | Asker can relay → exact shape ask |
| **Step 3** | Void in the **higher** ranking suit only | Asker can relay → exact shape ask |
| **Step 4** | Both suits short: singleton in both | — |
| **Step 5** | Both suits short: singleton higher, void lower | — |
| **Step 6** | Both suits short: void higher, singleton lower | — |
| **Step 7** | Both suits short: void in both | — |

**Memory aid: Steps 4–7 (both short)** use reverse binary encoding:
- Higher ranking suit is b10/(2) -> singleton = 1, void = 0
- Lower ranking suit: is b01/(1) -> singleton = 1, void = 0
- Steps are 3,2,1,0 in binary order: 11, 10, 01, 00

### After Step 1 (Lower Suit Short)

Asker relays (next step) to ask further:

| Askee's response | Meaning |
|-----------------|---------|
| Next step (Step 3 from relay) | Singleton in lower suit → asker can relay again for exact shape |
| Step 4+ from relay | Void in lower suit → responds as though exact shape asked (see below) |

### Exact Shape Ask

Triggered when asker relays after learning the specific shortness. At this point we know:
- Which suit is short and whether it's a singleton or void
- 9+ cards in the two long suits

Askee sorts the possible hand patterns by suit length in **lexicographic order** and bids steps accordingly (more extreme shapes higher steps):

**With a lone singleton** (one short suit = 1, other short suit = 2+):

| Step | Shape |
|------|-------|
| 1 | 5-4-2-1 |
| 2 | 5-5-2-1 |
| 3 | 6-4-2-1 |

**With a lone void** (one short suit = 0, other short suit = 2+):

| Step | Shape |
|------|-------|
| 1 | 5-4-4-0 |
| 2 | 5-5-3-0 |
| 3 | 6-4-3-0 |
| 4 | 6-5-2-0 |
| 5 | 7-4-2-0 |

---

## Standard Shortness Ask

Applies when no two-suiter has been described (only one suit known, or hand shape still ambiguous). There are three candidate suits for shortness.

### Step Responses

| Step | Meaning | What happens next |
|------|---------|-------------------|
| **Step 1** | No shortness | — |
| **Step 2** | Short in the lower of the two cheaper suits | Asker can relay (see below) |
| **Step 3** | Short in the higher of the two cheaper suits | Asker can relay (see below) |
| **Step 4** | Singleton in the highest ranking other suit | — |
| **Step 5** | Void in the highest ranking other suit | — |

"Other suits" = the three suits other than the one known long suit, ranked low to high.

### After Step 2 or Step 3 (Cheaper Suit Short)

Asker relays (next step) to distinguish singleton from void:

| Askee's response | Meaning |
|-----------------|---------|
| Next step | Singleton |
| Skip a step | Void |

---

## General Notes

- **Cheaper = lower.** Across all shortness-related sequences, when it comes time to show which suit the shortness is in by walking up steps, cheaper steps correspond to lower-ranking suits. Some sequences have adjustments — a step with a special meaning, or a dropped step because shortness is already guaranteed — but the cheaper = lower ordering always applies to the shortness-showing steps themselves.
- **Guaranteed-shortness modification.** When the bidding has already promised shortness (e.g., the mini-splinter over 1M), the "no shortness" step is **skipped**, saving a level. The remaining steps shift down accordingly.

## Summary of Key Principles

1. **3NT = no shortness** whenever it's available as a natural step in the two-suiter ask.
2. **Cheaper = lower** for identifying which suit is short (see General Notes above).
3. **Reverse binary** (11, 10, 01, 00) for both-short situations in the two-suiter ask, with higher suit as the leading digit and singleton = 1, void = 0.
4. **Exact shape** uses lexicographic ordering of possible shapes sorted by suit length.
5. **Relay = tell me more** at every stage — asker can always stop relaying and place the contract or do something else (RKC for example)
