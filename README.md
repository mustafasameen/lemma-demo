# LEMMA demo

LEMMA is a moderator agent for group decisions. It asks each member for the limits they have not stated, checks every possible plan with an exact solver, polls members in private, and closes only when everyone has said yes.

**Live site:** https://mustafasameen.github.io/lemma-demo/

The site replays saved runs, so it makes no model calls. Each scenario runs with several moderators side by side: no moderator, a one-time rule, Muse (a general agent prompted to moderate the same chat with no tools) and LEMMA. The Outcome tab checks every final plan against each member's private facts, not against what members said.

| Scenario | What it tests |
|---|---|
| Budget cut | Four friends, one member cuts their share from $400 to $150 |
| Shared car | Two roommates, one car, work and an appointment, no times given |
| Six friends | Six friends with $1,800 and no one has said their maximum |
| Eight friends | A stress test: eight friends, $2,600, five hard needs, one plan in 81 fits everyone |
| Real household | A household from the 2017 National Household Travel Survey, moderated by the trained policy |

The first three are the prompts our peer reviewer sent for the CGN 6905 (Agentic AI for Civil Engineers) final presentation, University of Florida, Fall 2026.

Group members are LLM agents (Llama 3.3 70B on the prompts, Mistral 7B on the household) with private facts written for the demo. On the prompts LEMMA runs its tools with a scripted policy; the trained policy (Llama 3.1 8B, reinforcement learning) runs on the household.

Keys in a scenario: Space plays or pauses, the arrow keys step, O opens the outcome.
