# Sunset: "Should we let you go?"

Reusable warning mail for inactive subscribers. Sent once per sunset cycle to the contacts flagged by `BIBB-Operational/operations/01_inactive/mailjet_inactive.ipynb`. Full process: `README.md` in that folder.

No LinkedIn version, no social posts. This mail only goes to the flagged segment.

---

## Mailjet configuration

| Field | Value |
|---|---|
| Campaign name (internal, drives utm_campaign) | `bibb_sunset` |
| Subject | Should we let you go? |
| Preview text | One click keeps you on the list. No click, and we remove your address in a week. |
| Sender name | bibb \| Oscar Martínez |
| Sender address | contact_bibb@bibb.pro |
| Recipients | List "BIBB Complete Newsletter subscribers", segment `sunset` equals `flagged` |
| Click tracking | **On** (the click is what keeps a contact) |

The subject must contain `let you go`. The notebook uses it to prove the warning was sent (`WARNING_SUBJECT`). Never use that phrase in a regular newsletter subject.

---

## Checklist per cycle

1. Refresh the three "In case you missed it" links in `sunset.mjml` with the latest content.
1. Notebook run with `APPLY = True` the same day, flags written.
2. Segment count in Mailjet matches "flagged" in the notebook output.
3. Send this mail to the segment.
4. Run the notebook again 7 or more days later: dry run, then `APPLY = True` and `DELETE = True`.

---

## Send log

| Date | Recipients | Clicked (kept) | Deleted |
|---|---|---|---|
| 2026-11-08 08:30 | 5,741 | | |
