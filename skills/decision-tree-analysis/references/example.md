# Example: decision-tree-analysis

**You invoke it with:**
> "Build a decision tree for whether to launch our smart thermostat"

**It needs from you:**
- DECISION (required): "Helio should launch the Helio One smart thermostat now, run a paid market test first, or shelve the product."
- PAYOFF MEASURE (required): "Three-year net present value in dollars; product gains positive, all build and test costs negative."
- HORIZON (required): "Three years from the launch decision."
- CONTEXT (optional): "A full launch costs about $4M to tool and market. A paid market test costs about $0.6M and takes a quarter. The thermostat market is competitive; we put roughly even odds on the segment being strong. Helio has ~$9M in the bank, so a failed launch is a serious but survivable hit."

**You get back:** a saved markdown report (`decision-tree-analysis-helio-thermostat-<date>.md`) with the full tree (decision and chance nodes with probabilities, terminal NPVs), branch detail with evidence and confidence, the fold-back arithmetic at every node with the optimal path marked, a break-even probability and an EVPI figure, a risk note, and a recommendation.

**See a full worked example:** [decision-tree-analysis-helio-thermostat-2026-06-19.md](decision-tree-analysis-helio-thermostat-2026-06-19.md), the report this invocation produces.
