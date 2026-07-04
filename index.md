# Newsletter Emails

Archive of sent and draft newsletter editions for bibb BI Corner.

Sent to Mailjet (13K subscribers) + published as LinkedIn native newsletter. Goes out Sunday mornings.

---

## Folder structure

Each edition lives in its own folder:

```
projects/bibb-pro/newsletter/
└── 000XX/
    ├── 000XX.mjml     # Email template (compiled via MJML)
    └── 000XX - campaign.md    # Social posts: LinkedIn + Twitter/X for all 4 days
```

## Sponsor block

The sponsor block sits between the hero and Oscar's Take section. Background `#e9f5f7`.

Two formats available:

**Text only** (default, no image):
```mjml
<mj-text align="center" ...>This Nth edition brought to you by:</mj-text>
<mj-text align="center" font-weight="bold" ...>[Name] - [Date]</mj-text>
<mj-text align="justify" ...>[Body copy]</mj-text>
<mj-button href="[url]" ...>[CTA]</mj-button>
```

**With banner image** (first used in #15):
```mjml
<mj-text align="center" ...>This Nth edition brought to you by:</mj-text>
<mj-text align="center" font-weight="bold" ...>[Name] - [Date]</mj-text>
<mj-image src="[url]" href="[cta url]" width="400px" border-radius="6px" />
<mj-text align="justify" ...>[Body copy]</mj-text>
<mj-button href="[url]" ...>[CTA]</mj-button>
```

Use the image format when the sponsor provides a banner (events, workshops). Link the image to the same CTA URL as the button. Width 400px keeps it centered with breathing room in the 640px layout.

---

## What drives performance

- Open rate: subject line provocation on core BI topics. #13 ("Most dashboards will die") is the benchmark at 48.56%.
- Click rate: actionability. #10 hit 4.35% (2x any other edition) because it had specific resources to click. Off-brand or low-action content hovers at 0.74–1.4%.
- Rule: one concrete thing to do or get = higher clicks. Vague digests do not convert.

## Edition index

| # | Topic | Status | Notes |
|---|-------|--------|-------|
| 7 | Startup Success: Crafting Impactful Dashboards | Sent | Earliest edition in Mailjet data. Solid open and click rate. |
| 8 | Top N Products With Time Comparisons in Power BI | Sent | Below-series open rate. Technique content but click rate average. |
| 9 | The Update Power BI Users Have Been Waiting For | Sent | Solid open rate. Click rate below average — no strong CTA. |
| 10 | Quick Wins for BI Adoption & Accessibility | Sent | Click rate outlier (4.35%, highest in series). Actionable format with specific resources drove clicks. |
| 11 | 2 Videos, 2 Blogs, 1 Stand Against AI Scraping | Sent | Digest format. Average open, low click. Digest structure does not convert. |
| 12 | 2 Videos, 4 Blogs, theme generator updates | Sent | Same pattern as #11. Digest format confirmed underperformer for clicks. |
| 13 | Most dashboards will die, but yours don't have to | Sent | Best open rate in series (48.56%). Provocative subject line on core BI topic. Benchmark edition. |
| 14 | AI Agent Skills: Token Efficiency (Aditya Kumar Darak) | Sent | Off-brand topic. Worst on both open and click rate. Confirmed: off-brand = audience disengages. |
| 15 | How to Design Better KPIs Before They Mislead You | Scheduled (April 12) | Oscar's own post. First affiliate sponsor block (Carolina Lago, OSCAR25). bibb Pro accounts launch announced. LinkedIn native newsletter also scheduled. |
