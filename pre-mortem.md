# Pre-mortem

A short framework for de-risking a project before you start. Faster than building and finding out the hard way.

## The idea

A pre-mortem is the opposite of a post-mortem. Instead of asking "the project failed; why?" after the fact, you ask it before you begin.

Imagine yourself six months from now. The project has failed. It's obvious in hindsight that it was going to fail. What killed it?

The reframe matters. "What could go wrong?" is open-ended and easy to dismiss. "We are sitting at the failure debrief; what's the cause we're describing?" forces you to be specific. You can't answer "the project failed" with "nothing went wrong."

The technique is from Gary Klein, the decision researcher. He found that teams who ran pre-mortems caught 30% more failure modes than teams who used standard risk-assessment templates. The framing does the work.

## When to run one

Before any of:
- A multi-week project where the cost of mid-flight pivots is high
- A hire, a co-founder agreement, a big partnership
- A product launch
- A migration or refactor that's hard to undo
- A bet you'd be embarrassed to have made carelessly

Pre-mortems are cheap. The cost is twenty minutes. The cost of skipping one and finding out is whatever the project was worth.

## How to run one with Claude

Three steps.

**1. Set the scene.** Tell Claude exactly what the project is and what success would look like. Specifics matter; a vague description gets a vague pre-mortem.

**2. Run the pre-mortem prompt.** Paste in the template below. Claude generates 10–15 failure modes ranked by how likely they are to kill the project.

**3. Decide what to do about the top 3.** For each: ignore it, mitigate it, or kill the project if it can't be mitigated. Most projects can absorb most risks. The point isn't to eliminate them all; it's to know which ones you're knowingly accepting.

## The prompt

```
Run a pre-mortem on the project below. The format:

1. Imagine it is six months from now. The project has failed. Don't ask
   what *could* go wrong — assume it *did* go wrong, and write the failure
   debrief from that vantage point.

2. Generate 10–15 distinct failure modes. Each one:
   - A 1-sentence description of what specifically went wrong
   - The category (technical, market, team, financial, regulatory, etc.)
   - A confidence rating: how likely was this in hindsight? (high / medium / low)
   - The 1–2 earliest signals we could have seen, if we had been watching
     for them

3. Then rank them. Put the most likely failure modes first, and explain
   in 1 sentence why you ranked the top three the way you did.

4. End with a short "what's missing" note: failure modes you considered
   weak, or categories you didn't have enough information to assess.

Be specific. "The team had communication problems" is not specific.
"The two founders never aligned on whether to optimize for revenue or
growth, and burned three months on an ICP debate that should have taken
two weeks" is specific.

The project:

[YOUR PROJECT DESCRIPTION]

What I'm worried about going in (optional, may bias the analysis but
gives you context):

[YOUR EXISTING WORRIES]
```

## Working example

Setup: you're about to start building a mobile app that uses an LLM to coach users through workouts in real time. Two-person team. Six months of runway.

What the pre-mortem might surface:

- **Latency killed it.** Real-time coaching needs sub-second response, and the chosen API averaged 2–3s. Mitigation cost more than rebuilding on a different stack. **Signals to watch:** API benchmark in week 1, end-to-end timing on real device by week 3.

- **The wrong audience.** The team built for advanced lifters and shipped to beginners. Beginners wanted form correction; lifters wanted programming. The app did neither well. **Signals to watch:** user interviews in week 2, churn analysis after first 50 users.

- **Cost per session.** Tokens added up. At the price point the market would bear ($10/mo), gross margin was negative. **Signals to watch:** cost-per-active-user calculation as part of pricing decision, not after launch.

- **Founder disagreement on scope.** One wanted to launch fast and learn; the other wanted to launch polished. Six-month timeline accommodated neither philosophy. **Signals to watch:** explicit decision on launch criteria before any code is written.

- **App Store review rejection.** The "AI personal trainer" framing triggered medical-claim concerns. Reviews dragged for weeks. **Signals to watch:** read App Store guidelines for health/fitness in week 1; talk to other AI-app teams about their review experience.

For each, you can now decide: ignore (too unlikely), mitigate (write down what you'll watch for and the trigger that means "stop"), or kill the project (the risk is too large to take on at this stage).

## Common failure modes of the pre-mortem itself

Pre-mortems aren't magic. They go wrong when:

**You hedge.** "The project failed, possibly because of X, or maybe Y, but it's hard to say." This is the pre-mortem failing on itself. Force commitment: pick the top three, defend the ranking.

**You only list things you're already worried about.** The point is to surface things you weren't thinking about. If the output matches your existing worry list, you ran a confirmation exercise, not a pre-mortem.

**You don't act on it.** Running the pre-mortem feels productive even when nothing changes. Define one action per top-three risk, with a date. If you can't define an action, you've decided to accept the risk.

**You overweight novelty.** The pre-mortem surfaces dramatic risks ("the API gets shut down") and underweights boring ones ("we shipped late and ran out of money"). Boring risks kill more projects. Don't let the exotic ones crowd them out.

## A short pairing

Pre-mortem pairs well with a "go/no-go criteria" document. After running the pre-mortem, write down what would have to be true at each checkpoint (week 4, week 12, week 20) for the project to continue. If those things aren't true at the checkpoint, you kill the project.

The pre-mortem tells you what to watch for. The go/no-go tells you when to act on what you saw.
