# Blocks

What's special about one block: how high it sits, when its homes were built, what happened at its corner, what is under its street, and where an archive has an old photograph of it. Knowy answers "what's special about my block?" from these, and the page at `/commons/blocks` looks a block up with no AI at all.

The blocks are the ones on The Sunset Wave's map: Lincoln to Sloat and a little south, 19th Avenue to the Great Highway.

## What's in here

| File | What it is |
| --- | --- |
| `grid.yml` | Every block, one line each: the Wave's own id, the name ("46th Ave, Moraga to Noriega"), a map point, its height above the sea (USGS), and when its homes were built (SF Assessor's roll). Built by a script. Don't edit by hand |
| `notes-history-north.yml` | History pinned to corners and blocks, Lincoln to Noriega |
| `notes-history-south.yml` | History pinned to corners and blocks, Ortega to Sloat and just south |
| `notes-ground.yml` | The ground: sand, groundwater, faults, the shore, buried shipwrecks. Some notes are true of a wide stretch or of every block |
| `photos-opensfhistory.yml` | Where OpenSFHistory (the Western Neighborhoods Project's archive) has pinned photographs. A pin and a link each. No captions, no pictures |

## How a note is written

```yaml
- id: a-short-slug
  title: A plain title that names the place
  kind: history        # or geology, ecology, photo
  at: 48th Ave & Judah # the corner or block in words
  lat: 37.7603
  lng: -122.5075
  years: "1895-1913"
  text: 60 to 130 words, readable on its own. Years, names, numbers.
  sources:
    - {name: "Streetwise: Carville (Western Neighborhoods Project)", url: "https://www.outsidelands.org/sw18.php"}
```

- `reach: area` with a `radius_m` for something about a wider stretch. `reach: everywhere` for something true of every block. Leave it out for a spot.
- `confidence: medium` means the place is approximate or there is one source.
- Blocks and corners. A public building (a school, a theater, a firehouse, a shop) can keep its address. A home never gets a house number, even when the source prints it, and nothing here says where a person lives.
- Every note names its sources. No source, no note.

## About the photographs

The pins come from OpenSFHistory's own public map. Its site asks that its content not be collected for AI and allows links and short references, so we keep only where a photograph is pinned and the link to its page, credited the way the archive asks ("OpenSFHistory / wnp25.1234"). Knowy says the archive has photographs at that spot and links to them. It never describes a picture.

If WNP is glad to share captions or thumbnails, add them then, with a line here saying who said yes and when.

## Fixing something

These were gathered in November 2026 from public sources and will have mistakes. A neighbor's correction (`corrections/`) or own account (`knowledge/`) wins. To fix a note, fix its text and its sources together. To fix a block's figures, add a correction; `grid.yml` is rebuilt from the public data.
