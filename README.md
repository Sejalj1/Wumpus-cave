# 🕳️ Wumpus Cave

A browser-based remake of the classic **Hunt the Wumpus** (1973) — playable entirely in a single HTML file, no dependencies required.

## Demo

Open `wumpus.html` in any modern browser and start hunting.

## Gameplay

You're an explorer descending into a dark cave system made up of a 4×6 grid of rooms. Somewhere in the darkness lurks the **Wumpus** — a fearsome creature you must hunt down before it finds you. Watch out for bottomless pits along the way.

**You win** by shooting the Wumpus with an arrow. **You lose** if you stumble into the Wumpus's room or fall into a pit.

### Sensing Your Surroundings

You can't see into unvisited rooms, but you'll pick up clues from adjacent ones:

| Clue | Meaning |
|------|---------|
| 🦨 Stench | The Wumpus is in a neighboring room |
| 💨 Breeze | A pit is in a neighboring room |
| ✨ Glimmer | Gold is nearby |

### Scoring

| Action | Points |
|--------|--------|
| Moving into a room | −1 |
| Firing an arrow | −5 |
| Picking up the gold | +100 |
| Killing the Wumpus | +200 |

## Controls

| Key | Action |
|-----|--------|
| `W` / `↑` | Move North |
| `D` / `→` | Move East |
| `S` / `↓` | Move South |
| `A` / `←` | Move West |
| `Space` / `F` | Toggle fire mode |

In **fire mode**, the directional keys fire an arrow in that direction instead of moving. Arrows travel up to 3 rooms. You start with **5 arrows**.

You can also use the on-screen D-pad and fire button in the sidebar.

## Map

- Rooms you've **visited** are fully lit.
- Rooms you **know about** (adjacent to visited) are revealed but dimmed — you can see clues in them.
- Rooms you **haven't discovered** are blacked out.
- After the game ends, the full map is revealed.

## Tips

- Use the stench and breeze clues together to triangulate where the Wumpus and pits are before moving.
- Missing a shot causes the Wumpus to move to a random neighboring room — it might charge right into yours.
- Grab the gold before going for the kill; there's no rush.
- You don't have to pick up the gold to win.

## Running Locally

No build step or server needed. Just open the file:

```bash
open wumpus.html       # macOS
start wumpus.html      # Windows
xdg-open wumpus.html   # Linux
```

## Browser Support

Works in any modern browser that supports the Canvas API and CSS Grid (Chrome, Firefox, Safari, Edge).

## About

Hunt the Wumpus was originally created by **Gregory Yob** in 1973 and is one of the earliest text-based games. This version adapts the core mechanics into a graphical grid with a dark terminal aesthetic.
