# NAO 10U Fall Ball 2026 — Team Site Reference

## Purpose
Replace the season's Google Doc / GroupMe link-dump with a single static
HTML page that serves as a standing resource hub for coaches and parents.
Built to survive across seasons — evergreen content (practice resources)
stays in place, seasonal content (schedule, scores, announcements) gets
wiped and refreshed at each season transition (fall → spring → fall).

## Hosting & Build Approach
- Single HTML file, mobile-first (parents/coaches will pull this up on
  phones at the field)
- Hosted on GitHub Pages (free), same pattern as saveaustinisd.org
- Custom domain to be attached later — reuse the DNS setup used for
  saveaustinisd.org (revisit those steps when ready to publish)
- Video content via standard YouTube iframe embeds only — never
  downloaded/re-hosted (confirmed within YouTube ToS)
- Built by Claude Code from this reference doc

## Season Transition Logic
At the end of each season, wipe and replace:
- Schedule → next season's schedule (or "schedule coming soon")
- Scores → cleared for new season
- Announcements → season-specific info (e.g. spring registration/deadlines
  during off-season gaps)

Keep as-is across transitions:
- Practice Resources / Coaches Corner (evergreen drill library)
- Site structure/navigation
- Team creed (update only if it changes season to season)

---

## Site Sections

### 1. Team Name & Creed
- Team name: **Pending vote (likely today)** — finalists are Badgers,
  Fleas/Pulgas, Bulls/Toros, Copperheads. Placeholder until confirmed.
- Uniform colors (this season only): charcoal grey and burnt orange,
  with black trim — grey body, burnt orange sleeves/collar, black piping,
  "NAO" circle patch on sleeve (`10U_Uniform.PNG`, uploaded)
- Logo: North Austin Optimist crest — navy blue, red, white, and black
  city skyline with crossed bats and baseball, "North Austin" on a
  banner above script "Optimist" wordmark, black background
  (`NAO_Logo.jpeg`, uploaded)
- **Visual direction (site-wide, multi-season):** Anchor the site's color
  scheme to the NAO logo and its standard **red, white, and blue** theme
  (matching NAO's All-Star branding) rather than this season's specific
  uniform colors. Uniform colors change team-to-team and season-to-season
  (this fall is grey/burnt orange); the NAO identity doesn't. Keeps the
  site's look stable and reusable across seasons/teams without a redesign
  each time. Team-specific accents (like this season's jersey number/name
  style) can live in smaller details if desired, but the core palette
  should stay red/white/blue.
- Team creed (same as last season):
  > **Be Humble. Always Hustle. Get the Last Out.**

### 2. Season Info — Schedule
Skeleton schedule (subject to change):

| Date | Event |
|---|---|
| Sept 12 | Opening Day / First Game — Doubleheader vs EAST |
| Sept 19 | Delwood Doubleheader |
| Oct 3 | Delwood Doubleheader |
| Oct 24–25 | NAO Fall Tournament |
| Nov 21 | End of Season & Closing Ceremony |
| Dec 5–6 | Brown Santa Tournament |

### 3. Season Info — Scores
**V1 (this season):** Simple results table, no PII (no player or coach
names — team-level only unless placed behind a login in the future).

| Date | Time | Opponent | Home/Away | W-L (Final Score) |
|---|---|---|---|---|
| *(populate as season progresses)* | | | | |

**V2.0 (future):** Professional per-inning box score, fed from the OnDeck
app Nelson was developing last fall. Out of scope for this build — noting
as a planned upgrade path, not being built now.

### 4. Coaches Corner (Evergreen — Practice Resources)
Organized by category, YouTube iframe embeds, one-line labels.

**Warm-ups & Centers**
- Ladder Speed and Agility Drill — https://www.youtube.com/watch?v=DlFogKVCUUk
- OF Fly Ball Warm-up — https://www.youtube.com/watch?v=Lnfgd_ld_CM
- IF Hands Warm-up — https://www.youtube.com/watch?v=BYNm-AU-eBc
- Quick Hand Drills — https://www.youtube.com/watch?v=30hG6bDYSb8
- OF Star Drill and Gap Communication — https://www.youtube.com/watch?v=9ffuJhVXn_I
- IF Stay Low Drill — https://www.youtube.com/shorts/70BS4mX6gJo
- Run Down Overview — https://www.youtube.com/watch?v=fclzLQAOCKs
- Run Down Drills — https://www.youtube.com/watch?v=cV8Ivq0XcJA
- Pick-off Strategies — https://www.youtube.com/watch?v=P_HFsM6zA5E

**Pitchers and Catchers**
- Catching 101 — https://www.youtube.com/watch?v=szgo9zzCldE
- Catcher Receiving Drills — https://www.youtube.com/watch?v=W1iV0NpavYo
- Coaching Pitchers — https://www.youtube.com/watch?v=bAMzqO32l6s
- Flat Ground Pitching Drills — https://www.youtube.com/watch?v=jbsP6U4y2B4
- Balance Pitching Drills — https://www.youtube.com/watch?v=q8FaTf5sk7M
- Pitching & Catching Drills — https://www.youtube.com/watch?v=bNZGlGb-ZKo

*(Additional categories — Hitting Stations, Outfield/Infield beyond
warm-ups, Base Running — to be added as Nelson supplies links from Notes)*

### 5. Announcements & Updates (Maintained Weekly)
Unlike Schedule/Scores (wiped at season transitions), Announcements is a
**living section** — manually maintained by Nelson with a weekly pass
(target: Sunday updates), adding new items and removing ones that are no
longer relevant (e.g. jersey order deadline comes down once it's passed).
Keep this simple — plain manual edit, no dates/expiration logic needed.

Current announcements:
- **Team Rep needed** — communicates with NAO board on special events,
  organizes snack schedule, handles concession duties
- **Team DJ needed** — sources each player's walk-up song, brings a
  speaker to games, plays clean music between defensive half-innings
- **Practices begin Wednesday, August 26** — Wednesdays & Fridays,
  6:30–8:30 PM. Cleats and baseball pants required (running/sliding drills)
- **PONY bat rule** — Only USA and BBCOR Drop 3 bats allowed
- **Jersey order deadline: Monday, August 24** — message Coach Nelson
  directly with jersey size, requested number, and cap size
- **Uniform requirements** — charcoal grey baseball pants, black belt,
  black socks (parent-purchased)

---

## Open Items Before Build
- [x] Team logo image — received (`NAO_Logo.jpeg`)
- [x] Uniform reference image — received (`10U_Uniform.PNG`)
- [x] Visual direction — anchor on NAO red/white/blue logo theme, not
      seasonal uniform colors
- [x] Announcements maintenance model — manual, weekly (Sunday), simple
      add/remove, no expiration logic
- [x] Coaches Corner drill links — current list considered sufficient for
      the season; more may be added later if gaps show up
- [ ] Official team name — pending team vote (Badgers / Fleas-Pulgas /
      Bulls-Toros / Copperheads)
