# NAO 10U Fall Ball 2026 — Team Site Reference

## Purpose
Replace the season's Google Doc / GroupMe link-dump with a single static
HTML page that serves as a standing resource hub for coaches and parents.
Built to survive across seasons — evergreen content (practice resources)
stays in place, seasonal content (schedule, scores, announcements) gets
wiped and refreshed at each season transition (fall → spring → fall).

## Hosting & Build Approach
- Single HTML file (`index.html`), mobile-first (parents/coaches will pull
  this up on phones at the field)
- Hosted on GitHub Pages (free), same pattern as saveaustinisd.org
- Repo: `nahunta/coach-nelson-huddle`, deployed from `main`
- Custom domain: **coachnelsonhuddle.com** (set via `CNAME` file; DNS
  configured the same way as saveaustinisd.org)
- Site title: **Coach Nelson's Huddle** (header subtitle: "NAO 10U Fall
  Ball - 2026")
- Link previews: Open Graph + Twitter Card meta tags using `og-image.png`;
  favicon is embedded inline; `apple-touch-icon.png` for iOS home screen
- Video content via standard YouTube iframe embeds only — never
  downloaded/re-hosted (confirmed within YouTube ToS)
- Built by Claude Code from this reference doc
- Workflow: changes are reviewed (summary + `git status`) before any
  commit; commit and push only after Nelson confirms

## Season Transition Logic
At the end of each season, wipe and replace:
- Schedule → next season's schedule (or "schedule coming soon")
- Scores → cleared for new season
- Announcements → season-specific info (e.g. spring registration/deadlines
  during off-season gaps)
- Season-specific text → header subtitle, Team facts (Season, Colors),
  footer, OG description, and disclaimer all name "Fall Ball 2026"

Keep as-is across transitions:
- Practice Resources / Coaches Corner (evergreen drill library)
- Site structure/navigation
- Team creed (update only if it changes season to season)

---

## Site Sections
Nav order: Team · Schedule · Scores · Announcements · Coaches Corner

### 1. Team Name & Creed
- Team name: **Toros** (decided by team vote; section heading reads
  "Welcome Toros!")
- Team facts cards: Club (North Austin Optimist), Division (10U), Season
  (Fall Ball 2026), This Season's Colors
- Uniform colors (this season only): charcoal grey and burnt orange,
  with black trim — grey body, burnt orange sleeves/collar, black piping,
  "NAO" circle patch on sleeve (`10U Uniform.PNG`)
- Logo: North Austin Optimist crest — navy blue, red, white, and black
  city skyline with crossed bats and baseball, "North Austin" on a
  banner above script "Optimist" wordmark, black background
  (`NAO Logo.jpeg`)
- **Visual direction (site-wide, multi-season):** Anchor the site's color
  scheme to the NAO logo and its standard **red, white, and blue** theme
  (matching NAO's All-Star branding) rather than this season's specific
  uniform colors. Uniform colors change team-to-team and season-to-season
  (this fall is grey/burnt orange); the NAO identity doesn't. Keeps the
  site's look stable and reusable across seasons/teams without a redesign
  each time. Team-specific accents (like this season's jersey number/name
  style) can live in smaller details if desired, but the core palette
  should stay red/white/blue.
- Team creed (updated this season; also repeated in the footer):
  > **Sportsmanship First. Always Hustle. Get the Last Out.**
- Footer disclaimer: site is an independent coaching resource by Coach
  Nelson, not an official page of North Austin Optimist or Optimist
  International.

### 2. Season Info — Schedule
Original skeleton schedule (subject to change):

| Date | Event |
|---|---|
| Sept 12 | Opening Day / First Game — Doubleheader vs EAST |
| Sept 19 | Delwood Doubleheader |
| Oct 3 | Delwood Doubleheader |
| Oct 24–25 | NAO Fall Tournament |
| Nov 21 | End of Season & Closing Ceremony |
| Dec 5–6 | Brown Santa Tournament |

Live table format:

| Date | Day | Time | Opponent | Home/Away | Location |
|---|---|---|---|---|---|

- Opponent prefixed with "vs" for home games, "@" for away games
- Tournaments: opponent column holds the tournament name, Home/Away is
  "—", time is "TBA" until known
- Subtitle note: game times/locations subject to change; check GroupMe
- **Upcoming games only** — on each weekly update, remove games that have
  been played (their results move to Scores)

### 3. Season Info — Scores
**V1 (this season):** Simple results table, no PII (no player or coach
names — team-level only unless placed behind a login in the future).

| Date | Time | Opponent | Home/Away | Result |
|---|---|---|---|---|

- New results are added as a row at the bottom (chronological order)
- Time column: game start time, or "Game 1" / "Game 2" for doubleheaders
  and tournament games
- Opponent: team name only (no "vs" / "@" prefix)
- Result: green **W** or red **L** badge (`badge win` / `badge loss`)
  followed by the score

**Result rule:** Scores are listed in box-score order — away team's runs
first, home team's runs second — regardless of whether we won or lost. The
W/L badge shows our result.
- Home game: opponent's score first (e.g., L 9-3 = we scored 3, they scored 9)
- Away game: our score first (e.g., W 8-4 = we scored 8, they scored 4)
- Forfeits: badge plus "(Forfeit)", no score

**V2.0 (future):** Professional per-inning box score, fed from the OnDeck
app Nelson was developing last fall. Out of scope for this build — noting
as a planned upgrade path, not being built now.

### 4. Coaches Corner (Evergreen — Practice Resources)
Organized by category, YouTube iframe embeds (lazy-loaded), one-line
labels. Closing note: "If you have a video and would like to share,
please send to Coach Nelson."

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

**Hitting Drills**
- How to Soft Toss — https://www.youtube.com/watch?v=rV3EQ5tHcNE
- Hitting off a Tee — https://www.youtube.com/watch?v=njFyLD5LOZo
- Effective Hitting Techniques — https://www.youtube.com/watch?v=NEfaNRgWJdU
- 3 Keys to Hitting with Power — https://www.youtube.com/watch?v=xInPUnOR7tY
- Best Hitting Drills Invented — https://www.youtube.com/watch?v=8IP_fvHirO4

**Pitchers and Catchers**
- Catching 101 — https://www.youtube.com/watch?v=szgo9zzCldE
- Catcher Receiving Drills — https://www.youtube.com/watch?v=W1iV0NpavYo
- Coaching Pitchers — https://www.youtube.com/watch?v=bAMzqO32l6s
- Flat Ground Pitching Drills — https://www.youtube.com/watch?v=jbsP6U4y2B4
- Balance Pitching Drills — https://www.youtube.com/watch?v=q8FaTf5sk7M
- Pitching & Catching Drills — https://www.youtube.com/watch?v=bNZGlGb-ZKo

*(Additional categories — Outfield/Infield beyond warm-ups, Base
Running — to be added as Nelson supplies links from Notes)*

### 5. Announcements & Updates (Maintained Weekly)
Unlike Schedule/Scores (wiped at season transitions), Announcements is a
**living section** — manually maintained by Nelson with a weekly pass
(target: Sunday updates), adding new items and removing ones that are no
longer relevant (e.g. jersey order deadline comes down once it's passed).
Keep this simple — plain manual edit, no dates/expiration logic needed.
Time-sensitive items (e.g. fields closed) go at the top of the list.

Current announcements (as of Oct 25):
- **Parking Reminder — Player & Neighbor Safety** — use the designated
  parking lot entrance at Morrow & Watson; don't park along Morrow St near
  the Gault St intersection or enter through the Gault gate
- **NAO Play-It-Forward Gear Exchange** — ongoing, free community program
  for players ages 4–14; donate or take gear, email
  northaustinoptimist@gmail.com
- **Practice Schedule** — Wednesday 6:30–8:30 required full-team practice
  (cleats and baseball pants); Friday 6:00–7:30 optional hitting and
  bullpen, pitchers and catchers required
- **PONY bat rule** — Only USA and BBCOR Drop 3 bats allowed

---

## Weekly Update Checklist
1. Add new results to the bottom of Scores (follow the Result rule)
2. Remove played games from Schedule
3. Add/remove Announcements as needed
4. Review the diff and `git status`, then commit and push once confirmed

## Open Items
- [x] Team logo image — received (`NAO Logo.jpeg`)
- [x] Uniform reference image — received (`10U Uniform.PNG`)
- [x] Visual direction — anchor on NAO red/white/blue logo theme, not
      seasonal uniform colors
- [x] Announcements maintenance model — manual, weekly (Sunday), simple
      add/remove, no expiration logic
- [x] Coaches Corner drill links — current list considered sufficient for
      the season; Hitting Drills category added
- [x] Official team name — Toros
- [x] Custom domain — coachnelsonhuddle.com
