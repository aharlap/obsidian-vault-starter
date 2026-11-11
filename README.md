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

## Use

- Create a note from a template with the **Templates: Insert template** command.
- Open a note in `Categories/` to see everything in that category.
- To track a meeting action item, type it as a checkbox, then run TaskNotes' convert command on that line. It becomes a task note with a link in its place.
- Add a project to a task's `projects` property and the task appears in that project note's Tasks section.

## License

MIT. The original template is copyright Steph Ango; see `LICENSE`.
