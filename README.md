# bibb-mail

Newsletter emails for bibb. Sent to Mailjet (~13K subscribers) + published as LinkedIn native newsletter. Goes out Sunday mornings.

---
For detailed info, in bibb.pro repo documentation\Analytics.md

---

## Folder structure

Each edition lives in its own folder at the repo root:

```
00017/
├── 00017.mjml      # Email template (compiled via MJML)
└── campaign.md     # Social posts: LinkedIn for all 4 days
```

---

## UTM tracking

UTMs are handled by Mailjet's auto-tagging — **do not hardcode UTM params in MJML hrefs**. All links should be clean URLs. Mailjet appends:

```
utm_source=bibb_pro_newsletter
utm_medium=email
utm_campaign=[[CAMPAIGN_TITLE]]
```

The Mailjet campaign name is the canonical `utm_campaign` value. Follow the `[owner]_[topic]` taxonomy:

| Type | Example campaign name |
|---|---|
| bibb content | `bibb_blog_content`, `bibb_tool_launch` |
| Partner exclusive | `metrica_salesforce_connector` |

Drop sequence numbers (e.g. `N0017`) — they are not descriptive and break the taxonomy.

---

## Sponsor block

Sits between the hero and Oscar's Take section. Background `#e9f5f7`.

**Self-promotion (bibb tool or product):**
```mjml
<mj-text align="center">This Nth edition of the bibb newsletter is brought to you by:</mj-text>
<mj-button href="[clean url]" align="center" background-color="#142328" color="#ffffff">[CTA]</mj-button>
<mj-text align="center">[Short description]</mj-text>
```

**External sponsor with banner image:**
```mjml
<mj-text align="center">This Nth edition of the bibb newsletter is brought to you by:</mj-text>
<mj-image src="[banner url]" href="[clean url]" width="400px" border-radius="6px" />
<mj-text align="center">[Short description]</mj-text>
<mj-button href="[clean url]" align="center" background-color="#FF0020" color="#ffffff">[CTA]</mj-button>
```

Width 400px keeps the banner centered with breathing room in the 640px layout.

---

## What drives performance

- **Open rate:** Subject line provocation on core BI topics. #13 ("Most dashboards will die") is the benchmark at 48.56%.
- **Click rate:** Actionability. #10 hit 4.35% (2x any other edition) because it had specific resources to click. Off-brand or low-action content hovers at 0.74–1.4%.
- **Rule:** One concrete thing to do or get = higher clicks. Vague digests do not convert.

---

## Edition index

| # | Topic | Sponsor | Status |
|---|-------|---------|--------|
| 7 | Startup Success: Crafting Impactful Dashboards | — | Sent |
| 8 | Top N Products With Time Comparisons in Power BI | — | Sent |
| 9 | The Update Power BI Users Have Been Waiting For | — | Sent |
| 10 | Quick Wins for BI Adoption & Accessibility | — | Sent. Click rate outlier (4.35%, highest in series). |
| 11 | 2 Videos, 2 Blogs, 1 Stand Against AI Scraping | — | Sent. Digest format confirmed underperformer. |
| 12 | 2 Videos, 4 Blogs, theme generator updates | — | Sent. Digest format confirmed underperformer. |
| 13 | Most dashboards will die, but yours don't have to | — | Sent. Best open rate (48.56%). Benchmark edition. |
| 14 | AI Agent Skills: Token Efficiency (Aditya Kumar Darak) | — | Sent. Off-brand topic. Worst open and click rate. |
| 15 | How to Design Better KPIs Before They Mislead You | Carolina Lago (affiliate, OSCAR25) | Sent. First sponsor block. bibb Pro accounts announced. |
| 16 | Salesforce Power BI Integration (Anton Storozhuk) | Metrica Software | Sent. First external partner sponsor. |
| 17 | New Tool: CF Icons Generator — Sajjad Ahmadi joins bibb | bibb (CF Icons Generator) | Sending |
