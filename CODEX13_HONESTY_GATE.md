# CODEX13 HONESTY GATE — claim-vs-DOM

Scope reviewed:
- `/workspace/uploads/index_8e9e.html`
- `/workspace/uploads/MERGE_RECEIPT_9a03.md`
- `/workspace/uploads/EVIDENCE_RECEIPT_7678.md`
- `/workspace/uploads/JEFF_README_5810.txt`

Gate date: 2026-09-20

## Claim-by-claim verdict

| Claim | Verdict | Evidence in DOM/receipts |
|---|---|---|
| Casa Ford name | **VERIFIED** | Header + Rest hero show **Casa Ford of El Paso**; Proof row includes Casa dealer facts and domain. |
| scan finished 2026-08-13 / ~38d age language | **VERIFIED** | Live strip: “Finished Aug 13, 2026”; script source `FIN = 2026-08-13T00:48:13.562+00:00`; age displayed as “About 38 days old” at gate date. |
| Rest = “Nothing needs you” and Rest ≠ Clear | **VERIFIED** | Rest hero says **Nothing needs you.** Copy explicitly says quiet is **not** a clean bill of health and scan is too old to trust. |
| 28 open + 5 more | **VERIFIED** | Seen copy states **28 open items** and **+5 more open, not shown**; Proof rows match counts and +5 list. |
| PREVIEW DONE ≠ published | **VERIFIED** | HOLD caveat: “PREVIEW DONE is not published”; HOLD subtext: “Still practice · nothing sent.” |
| cannot check Google listing today (`gbp_place_id null`) and no live mismatch claim | **VERIFIED** | Seen card says cannot check Google today and “not claiming a live mismatch”; Proof row explicitly shows `gbp_place_id null`. |
| PR #24 draft only if still in Proof | **CONFLICT (patched)** | Incoming DOM had a header link directly to PR #24 outside Proof. Tiny patch applied: header now links to **Proof notes**; PR #24 draft details remain in Proof drawer only. |
| DB RECEIPT vs preview badges honesty | **VERIFIED** | Data claims are framed as saved/looked-up historical scan (not live); HOLD explicitly labeled practice/preview and not sending. Evidence receipt contract aligns with UI copy. |

## Overall gate

**SHIP-WITH-PATCHES**

Reason: one honesty leak (PR #24 surfaced outside Proof) was present in the incoming file and fixed with a tiny honesty-only patch.

## Tiny honesty patch applied

- File: `/workspace/uploads/index_8e9e.html`
- Change: header link `Change not shipped` (direct PR URL) → `Proof notes` (internal `#evidenceDrawer` link)
- Impact: keeps PR draft/unmerged specifics confined to Proof, consistent with gate rule.
