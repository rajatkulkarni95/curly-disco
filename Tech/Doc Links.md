```
Workspaces: {
    [uuid]: {
      Wikilinks: {
        [file_id]: {
           Links: [],
           Backlinks: []
        }
     }
}
```

- [x] Remove FileName from the wikilinks structure (since renames and stuff don’t work)

- [x] Run an `update` on every save after a timeout (for deletions)

- [x] Truncate the name of the file for 300px.

- [x] When deleting file, remove their linked/backlinked stats

- [x] Check for links (if from outside the app) when loading a new page

- [x] Allow linking `Daily Desk` (cuid could be `formattedDate` )

- [x] Shortcut for Meta

- [x] Wikilink in `/` command

- [x] Figure out scrolls for the meta tag

- [x] Figure out colors between themes for the doc links

- [x] Creating new links from broken links should update the structure

- [x] Delete from breadcrumb doesn’t work :facepalm:

- [x] Disable wikilinks for templates

- [ ] Cursor doesn’t show up after the link

- [ ] Adding a file with a long name or a long path, expands the Meta (it should remain static)

- [ ] Deleting a duplicated file with \[\[wikilinks\]\] causes blank values in meta.

**Fast Follows:**

- [ ] Write a function when renaming/moving file to go to all `backlinked` files, and regex find/replace the `[[text]]` with `[[new name]]`

- [ ] Toast notifications when updated markdown

- [ ] Wikilinks command doesn’t show up if the previous text was a wikiink

- [ ] When the app is at is smallest width, opening both sidebars causes the meta to go out of bounds with no way to access