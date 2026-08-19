# Google Review Builder Skill

Reusable Codex skill for creating customer-controlled Google Review flows for different businesses and industries.

## Install from GitHub

Copy the `google-review-builder` folder into your Codex skills directory:

```text
<CODEX_HOME>/skills/google-review-builder
```

On a typical Windows installation this is:

```text
C:\Users\<you>\.codex\skills\google-review-builder
```

Then invoke it explicitly with `$google-review-builder`, or let Codex discover it from the request.

## Adapt it

Provide the business name, direct Google review URL, industry, languages, services, providers (if applicable), and truthful experience options. Use `assets/review-config.example.json` as a starting shape. The skill keeps the draft editable and requires the customer to confirm before Google receives anything.

All example values in this repository are placeholders and must be replaced before deployment.
