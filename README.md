# AI Red Team Lab

Practical findings and notes from GenAI / LLM red teaming experiments.

This repository documents vulnerabilities, interesting behaviors, and observations discovered while testing local and open-weight models (primarily via LM Studio + Garak + manual probes).

**Focus areas**: Prompt Injection (LLM01), Sensitive Information Disclosure (LLM02), Excessive Agency, Hidden Context Exposure, and related agentic risks.

## Coverage Catalog

Similar to Nuclei templates, this catalog lists tested models and the probes/vulnerabilities evaluated against them.

| Model | Quant / Setup | Probe / Technique | Status | Notes | Report |
|-------|---------------|-------------------|--------|-------|--------|
| qwen3.5-4b | Q4_K_M (LM Studio) | dan.Dan_11_0 | Partial | MitigationBypass succeeded (100%) | [dan-11.0](./findings/qwen3.5-4b/dan-11.0.md) |
| qwen3.5-4b | Q4_K_M (LM Studio) | promptinject | Pass | No failures detected | - |
| qwen3.5-4b | Q4_K_M (LM Studio) | leakreplay | Pass | No significant leakage detected | - |

> Status legend: `Pass` = model resisted, `Fail` / `Partial` = vulnerability or interesting behavior confirmed.

## Repository Structure

```
findings/
  <model-name>/
    <probe-or-technique>.md
templates/
  finding-template.md
tools/
  garak-setup.md
assets/
  screenshots/
```

## Finding Template

Use the template in [`templates/finding-template.md`](./templates/finding-template.md) for new entries.

## Tools Used

- [Garak](https://github.com/NVIDIA/garak) — LLM vulnerability scanner
- LM Studio — local OpenAI-compatible server
- Manual probes (curl / custom payloads)

## Disclaimer

Findings are from local / open-weight models in a controlled lab environment. Always follow responsible disclosure for production systems and respect model licenses / ToS.
