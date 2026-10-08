# linkhub-data

The links shown on the Link Hub pages. One file per site:

| File | Page | Dashboard |
|---|---|---|
| `hazwoper-osha.json` | https://linkhub.hazwoper-osha.com/ | https://linkhub.hazwoper-osha.com/admin/ |
| `ictraining.json` | https://linkhub.ictraining.us/ | https://linkhub.ictraining.us/admin/ |

Each file is a list of categories (`sections`), each with its links (`title`, optional `subtitle`,
`url`, optional `icon`). The page loads its file from GitHub when someone visits, so a change here
shows on the page within about 5 minutes (GitHub caches the file that long). No deploy needed.

## Editing

Use either dashboard. Sign in with a fine-grained GitHub token that has **Contents: Read and
write** on this repository; the same token works for both sites.

You can also edit the files directly on GitHub. Keep them valid JSON, and give every link a full
`https://` address; anything else is dropped from the page. `icon` is a path to an image on that
site (for example `assets/icons/mold.png`).

A page with one category shows a plain list; headings appear once it has two or more.

`social` lists the round social media buttons under the page intro, in order: `network` is one of
`facebook`, `instagram`, `youtube`, `x`, `linkedin`, `pinterest`, `website`, plus a `url`. An
empty list hides the row.

## Notes

- This repo must stay **public**: visitors' browsers read `links.json` straight from GitHub.
- The page also has a built-in copy of the links for search engines and in case GitHub is
  unreachable. That copy is refreshed whenever the site itself is redeployed.
- Every save is a commit, so the history doubles as an undo log.
