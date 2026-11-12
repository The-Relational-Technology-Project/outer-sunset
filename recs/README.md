# Recommendations

Neighbors' recommendations, one file per source, in the shape of `outer-dadas.yml`: a `meta` block saying where the recs came from, when, and how to reach people who aren't listed, then one entry per rec with how many neighbors vouched for it and when.

Rules for this folder:

- **Recs, not reviews.** Only things neighbors spoke well of. The agent passes along the caveat in `meta.caveat`.
- **No recommender names.** Entries say how many vouched, never who.
- **No personal numbers without a yes.** Individuals reached only by a personal phone or email are listed by first name and trade, with `contact: ask in <group>`. A steward adds a number only after that person agrees to be listed.
- **Freshness matters.** `when` is when the rec was made. Add a +1 by raising `vouches` and extending `when`; flag one that's gone downhill by opening a PR that removes it, with a line on why.

## Two ways a file can be made

- **With the group** (`outer-dadas.yml`): the group compiled it, and people in a trade can be listed by first name without a number.
- **From a chat nobody can join** (`sunset-neighbors.yml`): stricter. Only places and services with a shop, a website, or a public page. No individuals at all, no quotes, no numbers, no addresses, and every line written fresh so it can't be traced to a message. The chat is never kept in this repo. Knowy doesn't send anyone to the chat; it offers to ask a neighbor.

The agent cites each rec as the file's `meta.title` with the vouch count and date.
