# Butler Brief

A morning brief for your household, written by Claude Code. Run one command and get a short page
for the day: the weather, each person's day, what to prepare for and your to-do list. It works from
a small file about your family that stays on your computer.

Butler Brief is a free Claude Code plugin from [Build Your Butler](https://buildyourbutler.com/?utm_source=butler_brief&utm_medium=github),
a free course that teaches families to build a household assistant that emails this kind of brief
every morning by itself.

## Install

In your terminal:

```
claude plugin marketplace add MadFiddlerLabs/butler-brief
claude plugin install butler-brief@build-your-butler
```

Then, in Claude Code:

```
/butler-brief:morning-brief
```

## What it does

1. **The first time**, Claude asks four short questions: who lives with you, your town (for the
   weather), what the brief should cover, and anything regular, such as "PE kit on Tuesdays". It
   writes your answers to `morning-brief/household.md` in the folder where Claude Code is open.
2. **Each morning**, it gathers today's calendar (from a calendar connector if you have one, or
   from what you tell it), the weather (with your permission) and your to-dos.
3. **It writes the brief**, under 250 words, and saves it as `morning-brief/briefs/<date>.md`.
4. **You reply in plain words** to change things: "add milk to the to-dos", "milk is done",
   "leave out the weather". Run it again the same day and it shows today's brief, refreshing it
   only if you say so.

## Example prompts

- `/butler-brief:morning-brief`
- "What's on for the family today?"
- "Add 'book the dentist' to our to-dos and redo today's brief."

An invented example of a brief, for the Johnsons in Lisbon:

> **A busy Tuesday: PE kit, and Alex is in Porto until 6.**
> **Weather:** 19° and sunny, 21° by 3pm. No coats needed.
> **Sam:** working from home, call at 10. **Alex:** Porto, back by 6. **Mia:** nursery, PE today.
> **Prepare for:** Mia's party present for Saturday.
> **To-dos:** buy milk, book the dentist.

## What it reads and sends

- **Files:** only the `morning-brief/` folder, where Claude Code is open.
- **Your calendar:** only through a calendar connector you've added yourself, and only after you
  say yes. It never changes your calendar.
- **The weather:** one web search for your town's forecast, through Claude Code's own search,
  only after you say yes.
- **Nothing else.** The plugin has no server, runs no scripts and sends nothing to us. It never
  sends email or messages. See [PRIVACY.md](PRIVACY.md).

The skill asks you never to share ID numbers, account numbers, passwords or health details, and
leaves them out if you do.

## Troubleshooting

- **No weather:** say "you may look up the weather" and run it again.
- **No calendar:** add a calendar connector in Claude, or tell Claude what's on today.
- **Start over:** delete the `morning-brief/` folder.

Questions or problems: [open an issue](https://github.com/MadFiddlerLabs/butler-brief/issues).

## License

MIT. See [LICENSE](LICENSE).
