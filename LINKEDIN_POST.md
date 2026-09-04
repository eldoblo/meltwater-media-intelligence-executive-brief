# LinkedIn draft

Media monitoring is only useful when it helps a communications team decide what to do next.

I built an open-source n8n workflow that turns Meltwater-style monitoring data into an executive communications brief. It separates deterministic evidence from interpretation: mention volume, period change, sentiment, sources, themes, reach, authors, geographies, competitor signals, and unusual spikes are calculated first. Only then does the workflow prepare an optional LLM handoff prompt.

The demo uses fictional cybersecurity coverage, so it runs without credentials and does not pretend to represent a real brand. The final output is a human-review packet—not an automatic email, post, or journalist outreach.

Three design choices matter:

- Missing fields are marked unavailable instead of guessed.
- Every AI assertion is required to point back to supplied evidence IDs.
- Meltwater API mode is opt-in and contract-specific; no token or endpoint is hardcoded.

Draft contribution: **[GitHub draft pull request](https://github.com/eldoblo/meltwater-media-intelligence-executive-brief/pull/1)**

What would make an executive media brief genuinely useful in your team: better narrative detection, clearer risk thresholds, or more actionable next steps?

Recommended visual: a cropped n8n canvas showing the DEMO/API switch, deterministic metrics node, and Human Review Packet, with sensitive values hidden.
