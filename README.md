# linkhub-data

The links shown on **https://linkhub.hazwoper-osha.com/**.

`links.json` is the whole database: a list of categories (`sections`), each with its links
(`title`, optional `subtitle`, `url`). The public page loads this file from GitHub when someone
visits, so a change here shows on the page within about a minute. No deploy needed.

## Editing

Use the dashboard at **https://linkhub.hazwoper-osha.com/admin/**. Sign in with a fine-grained
GitHub token that has **Contents: Read and write** on this repository only.

You can also edit `links.json` directly on GitHub. Keep it valid JSON, and give every link a full
`https://` address; anything else is dropped from the page.

## Notes

- This repo must stay **public**: visitors' browsers read `links.json` straight from GitHub.
- The page also has a built-in copy of the links for search engines and in case GitHub is
  unreachable. That copy is refreshed whenever the site itself is redeployed.
- Every save is a commit, so the history doubles as an undo log.
