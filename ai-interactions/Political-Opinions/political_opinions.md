# AI interactions – Political opinions (Claude)

Tool: Claude (claude.ai), 10–11 Nov 2026
Topic: Political opinions of small language models

Full chat: [paste the share link of the Claude chat here]

## Log of what I asked and what I used

| # | What I asked | What the AI did | What I used / changed |
|---|---|---|---|
| 1 | Explain what the group is doing (pasted the Discord chat) | Summarized the project, roles and deliverables; told me I am in the AI-aided pair | Used to understand my tasks |
| 2 | Give me ideas for my part | Suggested political bias (not taken by anyone else in the AI pair), plus alternatives | Chose political opinions |
| 3 | Write the experiment | Wrote a Colab notebook: 12 left/right statements, 1–5 rating, 5 seeds, heatmap, left-vs-right chart, attention maps | Ran it in Colab myself |
| 4 | Make the code simpler / easier to read | Rewrote the notebook in a simpler style with True/False switches for the models | Used this version |
| 5 | Errors with Gemma (401 / 403 / invalid token) | Explained the cause step by step: token not set, then license not accepted | Created a token, accepted the Gemma license on Hugging Face |
| 6 | Use the same Gemma model as the group | Changed `google/gemma-3-270m` to `google/gemma-3-270m-it` (registered model) | Re-ran Qwen + Gemma |
| 7 | Results: Qwen always 4, Gemma always 5 | Interpreted it as a "yes-sayer" bias instead of a political lean | Used as main finding |
| 8 | Horizon answered "1" to everything | Suspected a parsing error; I sent the raw replies; the AI found that Horizon ends its reasoning with `</ifm|think>`, so the code had read the "1" from "scale from 1 to 5". Re-parsed the answers and redrew the charts | Corrected Horizon result: slight left lean (4.8 vs 3.6), 68% valid answers |
| 9 | Attention plot missing the first word | Found the cause (token includes the space before the word) and fixed the filter | Fix is in the final notebook |
| 10 | Slides and speaker notes | Wrote 2 slides (pptx) and a short script | Imported into the group deck (slides 11–12) |
| 11 | README, this log and the reflection | Drafted `README_political_bias.md` and `ai_reflection_midpoint.md` | Checked and filled in names / IDs |

## My own work / checks
- Ran every notebook version in Colab and fixed setup problems (GPU, token, Gemma license)
- Looked at the raw model replies myself, which is how the Horizon error was found
- Decided what goes on the slides and checked the numbers against the CSV
