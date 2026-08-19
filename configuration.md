# Configuration Guide

Use a business configuration rather than hard-coding a single brand into the flow.

## Required

- `businessName`: display name supplied by the owner.
- `googleReviewUrl`: direct review URL supplied by the owner. Validate that it is an `https://` URL before opening it.
- `languages`: supported locale codes and translated labels for every visible option.
- `experiences`: truthful positive, neutral, and improvement-oriented options. Each option needs a stable `id` and localized label/phrase.

## Optional

- `industry`: used for copy and sensible defaults, never as evidence of a claim.
- `services`: products, treatments, visits, or job types customers may select.
- `providers`: staff, technicians, clinicians, guides, or other people involved in delivery. Omit this step when it does not fit the business.
- `returnIntents`: honest choices such as returning, trying another service, undecided, or not at the moment.
- `sharingDestinations`: Google plus optional destinations such as Instagram. Each destination must be user-initiated and clearly labeled.
- `brand`: logo, colors, imagery, and tone supplied by the owner.

## Copy model

Store both a short label and a phrase fragment for each selectable option. Phrase fragments should combine naturally in each supported language and remain easy to edit. Avoid guaranteed outcomes, medical claims, fabricated numbers, pressure, or incentives tied to positive ratings.

## Review generation

The generated text should identify the business and the customer's selected context, summarize only selected experiences, include the selected return intent, and add an improvement note only when selected. Use a local deterministic formatter for predictable behavior. Keep the draft in an editable text area.

## Handoff safeguards

The final action may copy the draft and open the supplied Google URL in a new tab or app. It must not submit the review, choose stars, or hide the Google screen. Show a clear note that the customer reviews and confirms the content before posting.
