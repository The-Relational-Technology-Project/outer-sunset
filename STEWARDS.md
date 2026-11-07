# Stewards

The place is defined by its stewards. A small group of neighbors governs the agent together, through this repo. They set its voice (`place.md`), what it reads (`sources.yml`), who it can point to (`people.yml`), and what it has been corrected on (`corrections/`).

## Current stewards

| Name | Since | Reach |
| --- | --- | --- |
| Josh Nesbit | Nov 2026 | josh@relationaltechproject.org |

## How decisions get made

- Anything in this repo changes by pull request. Stewards review. No PR auto-merges.
- One steward can merge an event, a correction, or a proposal that looks right and harms no one. When in doubt, ask another steward in the PR.
- Changes to `place.md`, `STEWARDS.md`, `sources.yml`, or anything under `constituents/` wait for two stewards, or seven days with no objection, whichever comes first.
- Removing a source, a person, or a constituent is a steward decision and gets a line in the PR saying why.

## Reviewing a PR from the agent

Every PR the agent opens carries a label (`event`, `correction`, `proposal`) and a body with three parts: what the neighbor asked for in their words, what the agent changed, and why. Check:

1. Does the file match what the neighbor asked for? The agent showed them the exact text before opening the PR, but read it anyway.
2. Is anything in it about a private individual? Events name hosts only if the host gave a name for that purpose. Corrections cite how the neighbor knows, not who told them.
3. For a correction: is the "how I know" good enough? A photo of the door, a call, being there. "I heard" is not enough; ask in the PR.
4. For a proposal: is there already a thing that does this? Point there and close, or merge and let neighbors find each other.

Merge, or leave a comment. The agent never follows up on its own; a neighbor has to come back.

## Bringing in a suggested source

Neighbors can suggest a doc, a spreadsheet, a site, a calendar, or a group's list, in the chat or with the form on the sources page. Each one arrives as a pull request adding a file to `suggestions/` (labeled `source`) and as an email. Uploaded files come only by email; they never go into this repo.

Merge the suggestion file as the record, then bring the source in the right way:

| It's a | Bring it in as |
| --- | --- |
| Doc of recommendations (a group's recs) | A `recs/` file, like `recs/outer-dadas.yml`. Claude Code can convert a doc or PDF; keep personal numbers out unless the person said yes |
| Doc of background or history | An `archive/` note with its source |
| Spreadsheet that stays current | A `csv` source in `sources.yml`: publish the sheet to the web as CSV, then give it `title` and `text` templates |
| Spreadsheet that's a one-time list | Rows in `places.yml`, `resources.yml`, or a `recs/` file |
| Calendar | An `ics` source with the public iCal address |
| Blog, newsletter, news site with a feed | An `rss` source |
| Site neighbors built | An entry in `resources.yml` with the questions it answers; if it has a feed, a calendar, a Neighborhood API, or an llm.txt, a source too |
| Anything from a private group | Nothing yet: check with the group first, the way the Outer Dadas recs were |

Then set the suggestion's `status: added` (or `declined`) and a one-line `decision:`. Neighbors see that on the sources page, so a no comes with a kind reason.

## Becoming a steward

Open a PR that adds you to the table above, with a line on why you want to steward this and which part of the neighborhood you're closest to. Current stewards talk it over in the PR. We want this to be a few people from different corners of the Sunset, not a committee.

## Stepping back

Open a PR removing your row. No explanation needed. Thank you for the time you gave.

## Doors (doors.yml)

Groups that are glad to meet people at a life change: a new baby, a new move, a kid starting school. When a neighbor mentions one, Knowy offers a door or two, once, with how to get in. It points to the group, never to a member, and never guesses someone's life stage.

- Add a group only if it's public, or its organizers said Knowy may point people there. Write how and when in `confirmed`.
- `how_to_join` is only what the group is happy to have shared.
- A new moment (say, newly retired) needs at least one group that wants to be its door.

## The weekly email

Once a week Knowy sends a digest: what neighbors asked and couldn't get, links and dates that have gone stale, proposed cross-links, and a history note or two. Two kinds of PR come with it, both labeled so you can tell them apart:

- `links`: additions to `links.yml`, one line each saying why two records belong together. Merge the useful ones, delete the rest. Once merged, Knowy mentions the linked record when it cites either one.
- `archive`: a new note under `archive/` with `proposed_by: agent` in its front matter, drawn from the Internet Archive or Wikimedia Commons (public domain or licensed items only). Open the source link and check the note says only what the item shows before merging.

Nothing in the digest changes the notes on its own.
