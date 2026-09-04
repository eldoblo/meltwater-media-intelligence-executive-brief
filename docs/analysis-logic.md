# Analysis logic

The workflow follows a deterministic-first sequence:

1. Normalize records from `mentions`, `data`, `results`, or a direct array.
2. Preserve source IDs and record-level evidence.
3. Calculate counts, period change, sentiment mix, source concentration, themes, reach, high-impact records, authors, geographies, competitor/share-of-voice signals, and a spike flag where a previous count exists.
4. Emit `unavailable` for absent fields; never substitute a guessed value.
5. Build an LLM handoff prompt that requires evidence IDs and the sections: executive summary, what happened, what changed, why it matters, top narratives, reputational risks, communications opportunities, recommended actions, and watch next.
6. Produce a deterministic fallback brief in Demo Mode.
7. Package both outputs for human review.

The workflow does not claim that a theme caused a change. Any interpretation must remain traceable to supplied records.
