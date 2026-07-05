# CEFT Agent Safety Demo

This static demo page visualizes CEFT for the AgentDoG-Lite challenge.

Open `index.html` directly in a browser, or publish this branch with GitHub Pages:

```bash
xdg-open /root/AgentDoG_Lite/demo/index.html
```

Expected Pages URL:

```text
https://erin110.github.io/CEFT/
```

The page includes:

- Metric comparison under the AgentDoG 1.5 coarse prompt / unsafe-positive evaluation standard.
- SearchSwarm-style project page layout with a centered CEFT method title.
- CEFT framework diagram loaded from `assets/ceft-framework.jpg`.
- 3D diagnosis distribution loaded from `assets/diagnosis-distribution.jpg`.
- Trajectory cards with tool list, user messages, agent tool calls, environment returns, and final response.
- Summary-first demo interaction: the main page groups 8 cases into R-Judge and 2026 summer test sections, and clicking a card opens the detailed trajectory and model analysis.
- Cases from the 2026 summer test set and R-Judge, including a benign store-update case for over-refusal analysis.
- Side-by-side baseline vs CEFT verdicts.
- Short-CoT style CEFT analysis: Evidence, Risk source, Failure mode, Harm, Judgment.
- Counterfactual boundaries showing why CEFT learns behavior evidence instead of keyword refusal.

Referenced local artifacts:

- Training checkpoint: `outputs/ceft_sft/ceft_shortcot_full_3072_e1/final`
- Training data: `data/ceft_shortcot_full.jsonl`
- Prompt template: `prompts/ceft_shortcot_v1.txt`
- Evaluation logs: `outputs/*/ceft_shortcot_full_3072_e1_eval/`
