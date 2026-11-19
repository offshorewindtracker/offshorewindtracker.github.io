# Offshore Wind Tracker

A dated log of federal actions, litigation and lease buybacks affecting U.S. wind development, with the DoD Siting Clearinghouse thread marked so it can be viewed alone.

**Read it:** https://offshorewindtracker.github.io/

Every entry is written from a public source, and each links to the source it rests on.

## How review works

1. A scheduled search looks for new developments each weekday and proposes them as a pull request that adds entries to `data/items.json`.
2. Reviewers open the pull request under [Pull requests](../../pulls), check each proposed entry against its source link, and edit or remove entries as needed.
3. When a reviewer merges the pull request, the entries appear on the page within a minute or two.

Nothing reaches the page without a merge.

## Getting notified

Click **Watch** at the top of this repository and choose **All activity**. GitHub will email you whenever a new batch is proposed or merged.

## Suggesting an item or a correction

Open an [issue](../../issues/new) with the date, what happened and a link to a public source. Reviewers with write access can also edit `data/items.json` directly in the browser.

## The data file

`data/items.json` is a list with one entry per line. Each entry has these fields:

| Field | Meaning |
|---|---|
| `id` | `YYYYMMDD-short-description`, unique |
| `date` | Date the event happened, `YYYY-MM-DD` |
| `summary` | One or two sentences: who did what, with the case name and court for litigation |
| `project` | Project or lease, or `All wind` |
| `type` | `Litigation`, `Lease buyback`, `Regulatory action`, `Legislation / policy`, `Congressional oversight`, `Research / analysis`, `Project milestone` or `State / local` |
| `clearinghouse` | `true` when DoD or Clearinghouse review, or a national-security or radar rationale, is directly at issue |
| `mission` | The mission-relevance angle when `clearinghouse` is true, otherwise empty |
| `status` | `Pending`, `Ongoing` or `Resolved` |
| `next` | The next expected milestone, if the source states one |
| `actor` | Agency or court |
| `developer` | Developer, if any |
| `region` | State or states, or `National` |
| `scope` | `Offshore`, `Onshore` or `Both` |
| `tier` | `Primary` (filing, agency release, Federal Register), `Legal analysis` or `Press` |
| `source`, `url` | Name of the source and its link |

Keep the file valid JSON: entries are separated by commas, and the last entry has no trailing comma. If the page shows "could not be loaded" after an edit, the file has a syntax error.
