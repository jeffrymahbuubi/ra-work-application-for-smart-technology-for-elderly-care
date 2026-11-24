# AI-Based Traffic-Light Risk Classification System for Older Adults

The first group chose **Technology 2** from its older adult care proposal. The project explores how home care supervisors in Taiwan could use recent changes in a case, reported incidents, and service records to decide which cases to review first.

## What the supervisor sees

| Indicator | Meaning |
| --- | --- |
| Green · Routine review | The available information suggests the case is relatively stable. |
| Yellow · Monitor | A reported change needs continued monitoring. |
| Red · Review promptly | The case needs priority review by a supervisor. |
| Incomplete · Needs information | Some information needed to classify the case is missing. |

Each result shows the reason in plain language. The supervisor checks the underlying information and decides what follow-up is needed. This classroom prototype uses fictional cases to demonstrate review priority. Clinical decisions require professional judgment, and emergencies follow established response procedures.

## First classroom prototype

Start with a single browser page and two fictional inputs. Use rules that produce the same result for the same inputs so the group can check every result by hand. Later, students can compare an AI-assisted approach against this version and look at where their results differ.

1. Open this folder in Codex or Claude Code. Paste the prompt below into the chat.

   > Read `AGENTS.md` and the sample cases in `README.md`. Create a single `index.html` file that opens directly in a browser. Add two fields, “Recent change reported” and “Prompt supervisor review requested,” each with a blank, Yes, and No option. Add a “Check priority” button. Apply the first matching rule in this order. If prompt review is requested, show Red. If either field is blank, show Incomplete. If a recent change was reported, show Yellow. Otherwise, show Green. Show the result as text as well as color, with one sentence explaining the result. Use fictional data and tell me how to open and try the page.

2. Open the generated `index.html` in a browser. Enter each sample case, click **Check priority**, and compare the result and explanation with the table.
3. Ask the agent for one improvement based on what you observe. For example, if the Incomplete message is too vague, ask it to name the missing field. Then repeat the case with that field blank.

| Recent change reported | Prompt supervisor review requested | Expected result and reason |
| --- | --- | --- |
| No | No | Green · Neither a recent change nor a prompt review was reported. |
| Yes | No | Yellow · A recent change was reported. |
| No | Yes | Red · Prompt supervisor review was requested. |
| Blank | No | Incomplete · The recent change field is missing. |
| Blank | Yes | Red · The request for prompt review takes priority. |

As a group, decide which information a supervisor needs to understand each result and what an AI-assisted version would have to explain before you could compare it with the rules.
