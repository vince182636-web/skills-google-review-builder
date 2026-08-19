---
name: google-review-builder
description: Create or adapt an honest, reusable Google Review collection flow for a business or industry, including configurable questions, editable review drafts, and safe handoff to Google.
---

# Google Review Builder

Use this skill when building, adapting, or documenting a customer-facing flow that helps real customers leave Google reviews. It applies across industries such as salons, clinics, restaurants, home services, retail, and professional services.

## Outcome

Produce a working review flow that:

- asks only for facts the customer can truthfully confirm;
- creates an editable draft locally or in the user's chosen app;
- never selects a star rating, posts automatically, invents claims, or suppresses negative feedback;
- opens the business's own Google review URL only after the customer chooses to continue;
- supports the requested language(s), device constraints, and existing project framework.

## Workflow

1. Inspect the target project and identify its framework, entry point, styling conventions, and existing review or sharing behavior. Do not overwrite unrelated work.
2. Gather or derive a business configuration: business name, industry, Google review URL, languages, services/products, staff or provider list (if relevant), truthful experience options, return-intent options, and sharing destinations. Use [assets/review-config.example.json](assets/review-config.example.json) as the shape.
3. Read [references/configuration.md](references/configuration.md) before designing the question model or copy. It defines configurable fields, content safety boundaries, and adaptation rules.
4. Build the smallest flow that fits the host project. A typical flow has: direct-write path, guided questions, editable draft, copy/open Google action, and an explicit confirmation boundary.
5. Keep review generation deterministic and transparent where possible. If AI assistance is requested, treat it as optional drafting only and preserve the same truthfulness and editing safeguards.
6. Verify the flow with the project's available typecheck, lint, build, and tests. Test empty states, incomplete answers, language switching, mobile layout, clipboard failure, and an invalid or missing Google URL.

## Adaptation rules

- Replace all example brand, staff, service, pricing, ranking, speed, and testimonial content with user-provided values. Mark anything still illustrative as `placeholder`.
- Do not assume an industry-specific question is universal. Prefer neutral concepts such as service received, staff/provider (optional), what went well, what could improve, and likelihood of returning.
- Preserve negative and mixed experiences. A customer must be able to select an improvement or neutral option and edit the final text.
- Use the platform's official review link supplied by the user. Do not scrape listings or fabricate a place ID.
- Keep personal data out of the generated draft unless the customer explicitly supplies it and the host product has a clear reason to use it.

## Deliverables

Depending on the request, deliver code, configuration, copy, or a concise implementation note. When creating a reusable implementation, keep business-specific values in a separate configuration object or file so another industry can be supported without rewriting the flow.
