# Garak + LM Studio Setup Notes

## Config file (`lmstudio.yaml`)

```yaml
plugins:
  generators:
    openai:
      OpenAICompatible:
        uri: "http://<WINDOWS_IP>:1234/v1/"
```

## Environment

```bash
export OPENAICOMPATIBLE_API_KEY="lm-studio"
```

## Example command

```bash
python -m garak \
  --config lmstudio.yaml \
  --target_type openai.OpenAICompatible \
  --target_name qwen3.5-4b \
  --probes dan.Dan_11_0 \
  --generations 2
```

## Notes

- Enable "Serve on Local Network" in LM Studio.
- Use Host-only or Bridged networking between attack VM and Windows host.
