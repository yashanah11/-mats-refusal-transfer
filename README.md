# What Does Instruction Tuning Add?

## Probing the Transfer of Refusal Behavior from Instruct to Base Models

MATS 12.0 Winter 2026–27 research project.

### Research Question

When a refusal representation learned from an instruction-tuned model is transferred to the corresponding Base model, which aspects of refusal behavior transfer: a general refusal response tendency, context-sensitive harmfulness gating, or both?

### Models

- Llama 3.2 1B Base
- Llama 3.2 1B Instruct

### Dataset

JailbreakBench JBB-Behaviors

### Main Experiment

An Instruct-derived refusal direction was extracted from activation differences between harmful and benign prompts and injected into the corresponding Base model.

The primary evaluation measured changes in the log-probability of standardized refusal continuations on held-out harmful and benign prompts.

### Main Result

On the held-out set:

- Harmful prompts: +0.1500
- Benign prompts: +0.1723
- Harmful minus benign selectivity: -0.0223
- Bootstrap 95% CI: [-0.0443, -0.0016]

The transferred refusal direction therefore increased refusal-associated behavior, but did not reproduce harmfulness-selective refusal in this setup.

### Important Caveat

The primary metric is a refusal-continuation likelihood proxy, not a semantic refusal rate or safety score. Qualitative inspection showed cases where the metric increased without producing an actual semantic refusal.

### Repository Structure

`	ext
notebooks/   Experiment notebooks
analysis/    Analysis scripts
figures/     Research figures
results/     Experimental results




@"
# What Does Instruction Tuning Add?

## Probing the Transfer of Refusal Behavior from Instruct to Base Models

MATS 12.0 Winter 2026-27 research project.

### Research Question

When a refusal representation learned from an instruction-tuned model is transferred to the corresponding Base model, which aspects of refusal behavior transfer: a general refusal response tendency, context-sensitive harmfulness gating, or both?

### Models

- Llama 3.2 1B Base
- Llama 3.2 1B Instruct

### Dataset

JailbreakBench JBB-Behaviors

### Main Experiment

An Instruct-derived refusal direction was extracted from activation differences between harmful and benign prompts and injected into the corresponding Base model.

The primary evaluation measured changes in the log-probability of standardized refusal continuations on held-out harmful and benign prompts.

### Main Result

On the held-out set:

- Harmful prompts: +0.1500
- Benign prompts: +0.1723
- Harmful minus benign selectivity: -0.0223
- Bootstrap 95% CI: [-0.0443, -0.0016]

The transferred refusal direction increased refusal-associated behavior, but did not reproduce harmfulness-selective refusal in this setup.

### Important Caveat

The primary metric is a refusal-continuation likelihood proxy, not a semantic refusal rate or safety score. Qualitative inspection showed cases where the metric increased without producing an actual semantic refusal.

### Repository Structure

- notebooks/ — Experiment notebooks
- analysis/ — Analysis scripts
- figures/ — Research figures
- results/ — Experimental results

### Status

Experimental results and analysis are documented in the accompanying research write-up.
