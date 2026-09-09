# Discussion guide

This paper is a measurement record, not a claim that language-model agents have learned a profitable trading policy. The two fleets share one design lineage, and neither shows a directional edge. The useful result is a set of observed failure modes and control questions that can be tested elsewhere.

## Questions for follow-up work

### What belongs to the model, and what belongs to the operating layer?

The paired replay did not separate three frontier models on decision quality at the measured horizon, while repeated-choice stability differed sharply. A useful replication would hold tools, prompts, policy checks, state, and sampling fixed across model families, then report both economic outcomes and choice stability.

### Should volatility response be enforced rather than requested?

The agents received volatility information but chose the same median leverage across every volatility sextile. A follow-up should compare prose-only risk instructions with deterministic sizing constraints under the same point-in-time market states.

### Why do agents fail to retain favorable excursion?

Many positions reached substantial open profit and later closed negative. The fixed bracket result is a paired counterfactual on recorded positions, not evidence of a deployable alpha strategy. Replications should preserve fees, causal timing, and the same entry population while testing exit policies.

### How much behavior is caused by rendered context?

The gainers-leaderboard boundary changed selection despite not appearing in user strategy text. Similar tests could vary ordering, truncation, salience, and tool defaults while preserving the underlying information set.

### Which findings survive outside this lineage?

Both systems came from the same lab. Independent work should test different markets, tool surfaces, model families, holding periods, and human configuration interfaces before treating any mechanism as general.

## Evidence boundaries

- DX Terminal Pro was a 21-day real-capital deployment on Base. The DXAP record covers 69 days of Hyperliquid perpetual decisions, primarily paper execution at live prices plus a smaller real-capital book.
- The public files are aggregate extracts. They do not contain per-user or per-position rows.
- The paper reports no directional edge and no profitable live fleet. The bracket analysis is a mechanical replay result, not a trading recommendation.
- The regression discontinuity concerns the rendered leaderboard boundary in this system. It does not establish that every ranked list will cause the same behavior.
- The model league contains 416 captured production scenarios at one measured horizon. It is not a general model leaderboard.

## Reuse

The aggregate files in [`data/`](data/) map to specific figures in the paper. If you reproduce or challenge a result, please identify the file, paper section, timing assumption, and fee treatment you used. Corrections and replication notes are welcome at poof@dxrg.ai.
