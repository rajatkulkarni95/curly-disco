---
word_count: 65
title: Breaking
created: 2023-06-26
---

# Breaking Bugs

### V0.2.1

- Deleting a workspace, makes the app go in limbo. *Should take the next available workspace, or in the absence of any, take the user to the create screen*

- Creating a new note causes the Note Breadcrumb to not be updated, and doesn’t shift to that note uuid it seems. *Needs to move and work like it used to.*