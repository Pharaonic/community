# Maintaining

## Branches

`main` is the only long-lived branch. Discussion forms and community health files are read from it, so a change takes effect as soon as it merges.

## Discussion Categories

| Category | Slug | Format | Who starts threads | Form |
| --- | --- | --- | --- | --- |
| Announcements | `announcements` | Announcement | Maintainers | None |
| General | `general` | Open discussion | Everyone | None |
| Ideas | `ideas` | Open discussion | Everyone | `ideas.yml` |
| Polls | `polls` | Poll | Everyone | Not supported by GitHub |
| Q&A | `q-a` | Question and answer | Everyone | `q-a.yml` |
| Show and tell | `show-and-tell` | Open discussion | Everyone | `show-and-tell.yml` |

Categories are managed in the GitHub interface. A form applies only when its file name in `.github/DISCUSSION_TEMPLATE/` equals the category slug, so changing a slug means renaming the form and updating the links in `README.md`.

## Triage

- Mark the reply that solves a Q&A thread as the answer if its author does not. Ask for what is missing with `status: needs info`.
- Add a `layer:` label when a thread concerns one part of the ecosystem.
- When a thread turns out to be a confirmed bug or a specific feature, ask the author to open an issue in the package's repository, or open it yourself, link it from the thread, add `status: moved to package`, and close the thread.
- Hide or delete vulnerability details immediately, then ask the reporter to use the package's private reporting.

## Announcements

Post major releases, new packages, and deprecations. Routine patch releases stay in each package's release notes.

## Labels

`.github/labels.yml` is the source of truth. The `Labels` workflow creates and updates listed labels on every change to that file, and leaves any unlisted label alone.

## Settings Kept Outside the Repository

These live in GitHub settings and do not change through a pull request:

- **Organization discussions:** this repository is the source repository. Do not delete, rename, or make it private without choosing a new source first.
- **Repository features:** Discussions is on. Issues, Wiki, and Projects are off, because issues belong in each package's repository.
- **Private vulnerability reporting:** on.
