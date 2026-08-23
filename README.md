# Caraer app schemas

Public [JSON Schema](https://json-schema.org/) files for Caraer app config.

These are the schemas editors load from a `# yaml-language-server: $schema=…`
line (or a JSON `$schema` field). The caraer CLI still validates against the
same files bundled in the private `caraer-cli` repo.

## Files

| File | Used by |
| --- | --- |
| [`schemas/app.caraer.schema.json`](schemas/app.caraer.schema.json) | `src/app/app.caraer.yaml` |
| [`schemas/function.caraer.schema.json`](schemas/function.caraer.schema.json) | `src/app/functions/<name>/function.caraer.json` |
| [`schemas/webhook.caraer.schema.json`](schemas/webhook.caraer.schema.json) | `src/app/webhooks/*.json` |
| [`schemas/schedule.caraer.schema.json`](schemas/schedule.caraer.schema.json) | `src/app/schedules/*.json` |
| [`schemas/inbound.caraer.schema.json`](schemas/inbound.caraer.schema.json) | `src/app/inbound/*.json` |
| [`schemas/lifecycle.caraer.schema.json`](schemas/lifecycle.caraer.schema.json) | `src/app/lifecycle/*.json` |

## Editor hint

Put this at the top of `app.caraer.yaml`:

```yaml
# yaml-language-server: $schema=https://raw.githubusercontent.com/Caraer-HQ/caraer-app-schemas/main/schemas/app.caraer.schema.json
```

`caraer apps init` writes that line for you.

## Docs

- [How to create a Caraer app](https://developer.caraer.com/blog/2026-08-23-how-to-create-a-caraer-app)
