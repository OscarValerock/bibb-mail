# bibb-mail

Newsletter emails for bibb. Sent via Mailjet (~13K subscribers) and published as LinkedIn native newsletter. Goes out Sunday mornings.

Workflow and MJML block templates: `/bibb-newsletter` skill in ValerockOS (`.claude/skills/bibb-newsletter/SKILL.md`).

---

## Folder structure

Each edition lives in its own folder at the repo root:

```
00019/
├── 00019.mjml                # Email template (compiled via MJML)
├── campaign.md               # Mailjet config, LinkedIn posts, UTM links
└── linkedin-newsletter.docx  # LinkedIn native newsletter version (copy from Word, paste into LinkedIn)
```

---

## UTM tracking

Canonical taxonomy: `documentation/Analytics.md` in the BIBB-Pro repo.

**Email:** UTMs are handled by Mailjet's auto-tagging. Do not hardcode UTM params in MJML hrefs, all links stay clean. Check that UTM tagging is on in the campaign settings before scheduling. Mailjet appends:

```
utm_source=bibb_pro_newsletter
utm_medium=email
utm_campaign=[[CAMPAIGN_TITLE]]
```

The Mailjet campaign name is the canonical `utm_campaign` value. Follow the `[owner]_[topic]` taxonomy:

| Type | Example campaign name |
|---|---|
| bibb content | `bibb_blog_content`, `bibb_cf_icons_launch` |
| Partner exclusive | `metrica_salesforce_connector` |

Drop sequence numbers (e.g. `N0017`), they are not descriptive and break the taxonomy.

**LinkedIn:** links are tagged by hand, with the same `utm_campaign` as the Mailjet campaign.

| Where | utm_source | utm_medium |
|---|---|---|
| LinkedIn post (first comment) | `linkedin` | `social` |
| LinkedIn native newsletter (docx) | `linkedin_newsletter` | `newsletter` |

External links (Microsoft Learn, LinkedIn profiles, YouTube) and the Mailjet signup page stay clean.

---

## What drives performance

- **Open rate:** Subject line provocation on core BI topics. #13 ("Most dashboards will die") is the benchmark at 48.56%.
- **Click rate:** Actionability. #10 hit 4.35% because it had specific resources to click. #17 (new tool, 2.41%) confirms it. Off-brand or low-action content hovers at 0.4 to 1.4%.
- **Rule:** One concrete thing to do or get = higher clicks. Vague digests do not convert.
- Use click rate, not open rate, to compare editions. Apple Mail privacy inflates opens.

---

## Edition index

| # | Topic | Sponsor | Status |
|---|-------|---------|--------|
| 7 | Startup Success: Crafting Impactful Dashboards | none | Sent |
| 8 | Top N Products With Time Comparisons in Power BI | none | Sent |
| 9 | The Update Power BI Users Have Been Waiting For | none | Sent |
| 10 | Quick Wins for BI Adoption & Accessibility | none | Sent. Click rate outlier (4.35%, highest in series). |
| 11 | 2 Videos, 2 Blogs, 1 Stand Against AI Scraping | none | Sent. Digest format confirmed underperformer. |
| 12 | 2 Videos, 4 Blogs, theme generator updates | none | Sent. Digest format confirmed underperformer. |
| 13 | Most dashboards will die, but yours don't have to | none | Sent. Best open rate (48.56%). Benchmark edition. |
| 14 | AI Agent Skills: Token Efficiency (Aditya Kumar Darak) | none | Sent. Off-brand topic. Worst open and click rate. |
| 15 | How to Design Better KPIs Before They Mislead You | Carolina Lago (affiliate, OSCAR25) | Sent. First sponsor block. bibb Pro accounts announced. |
| 16 | Salesforce Power BI Integration (Anton Storozhuk) | Metrica Software | Sent. First external partner sponsor. |
| 17 | New tool: CF Icons Generator, Sajjad Ahmadi joins bibb | bibb (CF Icons Generator) | Sent Aug 2, 2026. 36.98% open, 2.41% click. |
| 18 | Power Query book out + Git for BI teams | Metrica Software | Sent Aug 9, 2026. 14.4% open, 0.65% click (second send in 7 days). |
| 19 | Claude Dashboards on Fabric + Theme Generator redesign + first data story | bibb (Power Query book) | Scheduled Nov 1, 2026. First edition after a 12-week gap. |
