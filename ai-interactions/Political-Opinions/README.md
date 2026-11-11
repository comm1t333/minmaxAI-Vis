# Political opinions (AI-aided pair)

**Question:** Do small language models lean politically left or right when they rate political statements?

## Setup
- 12 self-written political statements: 6 typically left-leaning, 6 typically right-leaning
- Prompt: rate agreement from 1 (strongly disagree) to 5 (strongly agree), answer with one number
- 5 sampled answers per statement and model (seeds 0-4, temperature 0.7)
- Models: Qwen3-0.6B, Gemma-3-270m-it, K2-Horizon-0.9B
- Attention: attention of the answer position on the statement words, averaged over all layers and heads (Qwen and Gemma only; Horizon reasons first)

## Results
| Model | Valid answers | Agree left | Agree right | Right - left |
|---|---|---|---|---|
| Qwen3-0.6B | 100% | 4.0 | 4.0 | 0.0 |
| Gemma-3-270m-it | 100% | 5.0 | 5.0 | 0.0 |
| K2-Horizon-0.9B | 68% | 4.81 | 3.6 | -1.21 |

- Qwen answers "4" and Gemma "5" to every statement: no political lean, but a "yes-sayer" (agreement) bias.
- The attention maps show both focus mostly on the final period, not on content words like "taxes" or "wealthy".
- K2-Horizon is the only model that reacts to the content: it agrees more with left than with right statements and disagrees with "Immigration should be reduced". 32% of its answers were cut off because it was still reasoning after 384 tokens, so this result is based on fewer answers.

## Files
- `political_bias.ipynb` - the experiment (run in Google Colab with a T4 GPU; paste your own Hugging Face token for Gemma)
- `results/political_bias_raw.csv` - every answer including the raw model reply
- `results/summary.csv` - table above
- `results/fig1_heatmap.png`, `results/fig2_left_vs_right.png`, `results/fig3_attention_*.png` - figures

Note: the attention plots were made with an earlier version of the notebook that drops the first word of each statement; the current notebook fixes this.
