# Draft — Post #5 from backlog (Open Source pillar)

**Platform:** LinkedIn
**Status:** awaiting approval (sent to WhatsApp)
**Source:** `C:\tmp\opensource\Contribution-projects\discussion_body.txt` (real Flink Agents GitHub discussion post), cross-checked against `profile/about-me.md` section 3.

---

Apache Flink has a 0.4 release freeze on Sept 15. I used the days before it to argue for a feature that doesn't exist yet.

The problem: when you change an AI agent (new prompt, different model, tweaked logic), there's no way to know how it'll behave against state it already built up — you ship and watch.

My proposal on the Flink Agents discussion: replay a job from a savepoint, but feed it a recorded stream instead of live traffic, and intercept side effects (calls to a ChatModel or a tool) instead of firing them for real.

Three pieces:
→ A sink that records the input stream (event time, key, payload) — doesn't touch runtime state.
→ A replay job started from a savepoint, reading recorded data instead of live traffic, keeping per-key ordering so watermarks and state behave the same.
→ A ReplayContext that defaults to "record what would have happened" unless an Action explicitly opts in as safe to actually run.

No changes needed to checkpoint/recovery semantics — a replay job is just a normal Flink job pointed at a different source.

Still open: should side-effect safety live on the Action as a decorator, or in a separate registry? And is comparing old-vs-new output in scope for a first cut, or is "run once, look at it" enough to start?

Posted it knowing the freeze means it won't ship anytime soon — I wanted the shape settled for whenever it does get picked up.

If you've built replay/shadow-testing into a stateful streaming system, I'd like to hear how you handled the side-effect problem.

---
*~230 words. No fabricated details — every technical claim traces to the actual discussion post.*
