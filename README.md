# Grouped Artist Onboarding — Email Drip Campaign

HTML email templates for the Grouped artist onboarding series. Built for import into **Brevo**.

---

## File Index

| File | Email | Subject Line | Send Trigger |
|------|-------|-------------|--------------|
| `EmailOneWelcome.html` | Email 1 | Welcome To The Grouped Family! 👋 | Immediately after artist verifies email |
| `Email2Swaps.html` | Email 2 | Your first swap takes less than 5 minutes | +1 day after Email 1 |
| `Email3DataOwnership.html` | Email 3 | Know your fans. Own your data. | +2 days after Email 2 |
| `Email4FounderStory.html` | Email 4 | Why we built Grouped | +3 days after Email 3 |
| `Email5SocialProof.html` | Email 5 | The OnlySteves blueprint 👀 | +3 days after Email 4 |
| `Email6re-engagement.html` | Email 6 | Still finding your footing? | +5 days after Email 5 |
| `Email7FinalPush.html` | Email 7 | Your fans are waiting | +7 days after Email 6 |

> **Note:** The verify email is handled separately outside of this drip series. The trigger for Email 1 (series entry) is email verification — needs to be confirmed with Ben/dev on how that event is surfaced in Brevo.

---

## Design

- **Logo:** Navy (`#111620`) Grouped wordmark — embedded inline as base64 SVG (no external hosting needed)
- **Background:** `#f0efef` (light grey)
- **Brand Gold:** `#C48A3A`
- **Navy:** `#111620`
- **Fonts:** Syne (headings) + DM Sans (body) via Google Fonts
- **Reply-to:** support@grouped.com

---

## Brevo Variables

Replace these placeholders when building the series in Brevo:

| Variable | Description |
|----------|-------------|
| `{{artistName}}` | Artist's Name |
| `{{alias}}` | Name of their Group/community |
| `{{swap_creation_url}}` | Link to create a swap |
| `{{group_setup_url}}` | Link to Group setup *(confirm with Ben/dev)* |
| `{{unsubscribe_url}}` | Unsubscribe link |

---

## Series Entry/Exit

- **Entry trigger:** Artist successfully verifies their email — need to confirm with Ben whether manually verifying an artist via the admin panel also fires this trigger (some artists have issues with the verification link or never receive the email)
- **Exit trigger:** `swap_created` — artist creates their first swap (remove from series immediately)
