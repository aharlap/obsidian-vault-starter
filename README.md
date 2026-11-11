# Obsidian vault starter

A starter vault based on [kepano-obsidian](https://github.com/kepano/kepano-obsidian), Steph Ango's vault template, explained in [How I use Obsidian](https://stephango.com/vault). It keeps his approach (categories as properties, Bases for views, links to notes that don't exist yet) and changes four things:

1. **Notes go in `Notes/`.** New notes and journal entries are created there instead of at the vault root.
2. **Tasks use [TaskNotes](https://github.com/callumalpass/tasknotes).** Each task is a note. Project notes list their tasks, and `Categories/Tasks.md` lists open tasks.
3. **Fewer categories.** Movies, shows, music, games, places, recipes, products and trips are removed. People, companies, meetings, projects, books, podcasts, posts, events, clippings, evergreen notes and the journal remain.
4. **Agent instructions.** `AGENTS.md` (and `CLAUDE.md`, which loads it) tells AI coding agents how the vault is organised and not to rename notes from the shell.

The example notes are removed, so the vault starts empty.

## Set up

1. Download or clone this repository and open the folder as a vault in Obsidian. TaskNotes needs Obsidian 1.12.2 or later.
2. In Settings → Community plugins, turn on community plugins, then browse for **TaskNotes** and install and enable it. Its default settings work with this vault: tasks are tagged `task` and saved in `TaskNotes/Tasks/`.
3. If you use [Obsidian Web Clipper](https://obsidian.md/clipper), set its default template's note location to `Clippings` and add `categories` with the value `[[Clippings]]`. `Templates/Clipping Template.md` shows the full set of properties.

## Shortcuts

Set in `.obsidian/hotkeys.json`. On Windows and Linux, Cmd is Ctrl and Option is Alt.

| Shortcut     | Does                                        |
| ------------ | ------------------------------------------- |
| Cmd+N        | New note in `Notes/`                        |
| Cmd+Shift+I  | Insert a template into the current note     |
| Cmd+O        | Open any note by name                       |
| Cmd+P        | Command palette: run any command by name    |
| Cmd+Option+T | New task                                    |
| Cmd+Option+C | Turn the checkbox at the cursor into a task |
| Cmd+Option+L | Task list                                   |
| Cmd+Option+A | Task agenda (by date)                       |
| Cmd+Option+D | Today's daily note                          |
| Cmd+Option+J | New journal entry                           |

## Four rules

1. **Write everything in `Notes/`.** Cmd+N puts new notes there. Don't sort notes into folders.
2. **The template says what a note is.** Inserting the Meeting template makes a note a meeting, because the template adds `categories: [[Meetings]]`. Everything else in the vault reads that property.
3. **Link freely.** Type `[[` for any person, company, project or idea, even if it has no note yet. Clicking a link creates the note; insert a template into it to say what it is.
4. **Notes in `Categories/` list their category.** Open [[Meetings]], [[Projects]], [[Tasks]], [[People]] and so on to see their notes as tables.

## Which template to use

You need four of these most days: Meeting, People, Project and Journal. Ignore the rest until something calls for them.

| Template | Use it for | Title the note |
|---|---|---|
| **Meeting** | Any conversation worth notes: calls, interviews, coffee chats. Fill in `people` and `org`. | `2026-11-12 Kickoff with Jane` |
| **People** | Anyone you meet or work with. Their note lists every meeting they were in. | `Jane Doe` |
| **Company** | An organisation: client, funder, competitor, employer. | `Acme` |
| **Project** | Something with an outcome you're working towards, and **ideas for things you could build**. Set `status` to `idea`, `active`, `paused` or `done`. The Ideas tab in [[Projects]] lists every project whose status is `idea`. | `Course commons` |
| **Journal** | Thinking out loud: reflections, worries, decisions you're weighing. One note per entry. Cmd+Option+J creates it already titled with the date and time. | (automatic) |
| **Evergreen** | One idea of your own that you'll keep refining, titled as a claim. Link it from meetings and clippings that support it. Not the place for build ideas; use Project for those. | `Learners skip what they can't use this week` |
| **Book** | A book you're reading or want to read. It starts tagged `to-read`; add a `rating` when you finish. | `Thinking in Systems` |
| **Author** | A writer whose books you track. The note lists their books. Use People instead for someone you've actually met. | `Donella Meadows` |
| **Post** | Something you published, such as a blog post, a LinkedIn post or a talk, with its `url` and `published` date. | `Why course completion lies` |
| **Clipping** | Applied for you by Web Clipper. You rarely insert it by hand. | (automatic) |
| **Quote** | A line worth keeping, with `attribution` and `source`. | the quote's first few words |
| **Event**, **Conference**, **Conference Session** | Events you attend and the sessions you take notes on. | `DevLearn 2026` |
| **Podcast**, **Podcast Episode** | Shows you follow and episodes worth notes. | `Well Made 145` |
| **Email** | An email you need to keep as a record. | `2026-11-12 Email from Acme about scope` |
| **Monthly Note** | Optional. A note titled with a month lists every note created that month. | `2026-11` |

Rarely needed: **Contact** (People does the same job), **Meeting Type** (a note such as "Interview" that lists every meeting with `type: [[Interview]]`) and **Meetings List** (adds a meetings list to a note that already exists).

### Daily notes and journal entries

- **Daily note** (Cmd+Option+D). One per day, titled with the date, saved in `Daily/`. It lists every note you created that day, so it shows what happened. Jot quick scraps in it if you like, but anything worth finding later belongs in its own note.
- **Journal entry** (Cmd+Option+J). A separate note for each bout of thinking. It appears in that day's daily note automatically.

## Tasks

Each task is its own note in `TaskNotes/Tasks/`. Create one with Cmd+Option+T and type in plain language:

```
Send proposal due friday +[[Website redesign]] @email
```

- **Project (`+`).** The outcome the task belongs to. It's a link to a Project note, and the task appears in that note's Tasks section. Most tasks should have one.
- **Context (`@`).** Where or how you can do it: `@computer`, `@phone`, `@email`, `@errands`, `@waiting`. Use contexts to batch work ("I have 20 minutes and my phone"). Skip them until you want that.
- **Tag (`#`).** A cross-cutting area that isn't a project, such as `#admin` or `#finance`. You can mostly do without. Every task already has the `task` tag, which is how TaskNotes finds it; don't remove it.

Dates: "friday" on its own sets the **scheduled** date, the day you plan to work on it. "due friday", "by friday" or "deadline friday" sets the **due** date.

During a meeting, type action items as ordinary checkboxes (`- [ ] Send the draft`). For each one worth tracking, put the cursor on it and press Cmd+Option+C.

Review tasks with Cmd+Option+L (list), Cmd+Option+A (agenda) or [[Tasks]]. `TaskNotes/Start Here.md` is TaskNotes' own tour.

## Saving web pages

Clip with Web Clipper. Pages land in `Clippings/` and appear in [[Clippings]]. Link a clipping from the meeting, project or evergreen note it supports.

## License

MIT. The original template is copyright Steph Ango; see `LICENSE`.
