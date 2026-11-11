# Vault conventions

This folder is an Obsidian vault. Notes are Markdown files with YAML properties. Follow these rules when you read or write notes.

## Folders

- `Notes/`: everything written in this vault, including meetings, projects, people and journal entries.
- `References/`: notes about things outside the vault, such as books, people, companies and podcasts.
- `Clippings/`: web pages saved with Obsidian Web Clipper. Treat them as sources, not as the owner's views.
- `Daily/`: one note per day, named `YYYY-MM-DD.md`.
- `TaskNotes/Tasks/`: one note per task, created by the TaskNotes plugin.
- `Categories/`: one note per category. Each one embeds a base that lists its notes.
- `Templates/`: note templates. `Templates/Bases/*.base` are the saved queries (Obsidian Bases, YAML) that the category notes and templates embed.
- `Attachments/`: images and files.

## Properties

- `categories` says what a note is, as a list of links: `categories: ["[[Meetings]]"]`. The matching template in `Templates/` lists the other properties for that category. Copy the template's properties when you create a note.
- Link people, companies, projects and topics as `[[Name]]`, even when the note doesn't exist yet. A link to a missing note is fine; it marks something that may get a note later.
- Dates are `YYYY-MM-DD`.
- A task is a note tagged `task` with `status` (`open`, `in-progress` or `done`), and optional `due`, `scheduled`, `priority`, `contexts` and `projects`. `projects` holds links to project notes: `projects: ["[[Website redesign]]"]`.

## Finding things

- Backlinks: search for `[[Name` (this also matches `[[Name|alias]]` and `[[Name#heading]]`).
- Notes in a category: search for `[[Meetings]]` in the `categories` property, or read the category's base in `Templates/Bases/`.

## Don't

- Don't rename or move notes. Obsidian rewrites links when it renames a note; a shell `mv` leaves every link to that note broken. Ask the owner to rename it in Obsidian.
- Don't edit `.obsidian/`.
