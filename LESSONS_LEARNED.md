# Lessons Learned

A few things that stuck with me after finishing Phishing Unfolding.

## Speed vs. accuracy is a real tension

Alerts kept coming in while I was still working through older ones, and it was tempting to just clear the queue fast. But rushing a verdict is exactly how you either miss a true positive or waste time escalating something benign. I had to consciously slow down on anything that looked ambiguous instead of pattern-matching to "looks like the last one."

## Not every alert deserves the same attention

Early on I was treating every alert like it needed a full deep-dive. That doesn't scale when there are dozens stacking up. Learning to triage by severity and age first — and quickly recognizing "this is clearly noise" vs "this needs a closer look" — made a huge difference in actually keeping up with the queue.

## Alerts are rarely isolated

A bunch of the alerts I worked were downstream symptoms of the same root phishing email. Once I noticed the pattern, I stopped treating each one as a brand new investigation and started asking "is this connected to something I already confirmed?" That saved a lot of redundant work and made the final report more coherent than a pile of disconnected verdicts.

## Threat intel is a tool, not a verdict machine

TryDetectThis was useful for confirming suspicion on indicators, but it didn't hand me answers. I still had to reason through headers, sender behavior, and context myself. Leaning too hard on "the TIP said X" without understanding why would've been a shortcut that doesn't hold up in a real SOC.

## Documentation matters as much as the catch

Getting the right verdict wasn't the whole job — writing it up clearly, so someone else (or future me) could follow the reasoning without re-doing the investigation, was just as important. That's a habit I want to carry into every future writeup, not just this one.

## What I'd do differently next time

- Set up a lightweight note-taking system *before* alerts start flooding in, instead of improvising structure mid-shift
- Flag "possibly related" alerts immediately instead of waiting to notice the pattern later
- Time-box the initial look at each alert so a tricky one doesn't eat the whole queue
