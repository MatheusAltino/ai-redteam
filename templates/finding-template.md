# Finding Template

Copy this file into `findings/<model-name>/<short-name>.md` and fill it in.

---

## Metadata

- **Model**: 
- **Quantization / Format**: 
- **Setup**: (e.g. LM Studio, OpenAI-compatible endpoint, context size)
- **Date**: 
- **Probe / Technique**: 
- **OWASP Mapping**: (LLM01, LLM02, ASI01, etc.)
- **Severity**: (Low / Medium / High / Info)
- **Status**: (Confirmed / Partial / Not Reproduced)

## Summary

One-paragraph description of what was observed.

## Payload / Probe

```text
Paste the exact prompt or relevant part of the probe here.
```

## Evidence

Describe the model response or attach a sanitized screenshot in `assets/screenshots/`.

- Screenshot: `../assets/screenshots/example.png`
- Raw log / JSONL excerpt (sanitized):

```json
{
  "prompt": "...",
  "response": "..."
}
```

## Impact

What an attacker could achieve with this behavior (in a realistic application context).

## Mitigation / Notes

Possible defenses or observations about why it worked / failed.

## References

- Garak probe name (if applicable)
- Related papers or write-ups
