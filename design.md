# Game Design

## Format
- **Web-based SPA**, built in **Vue**.
- Fully **static**, hosted on **GitHub Pages**. No backend, no server, no accounts.
- Implication: state lives in the browser (likely `localStorage`), assets ship with the build, no live network dependencies.

## Genre and influences
- **Text-based adventures of the 1980s** — atmosphere over spectacle, prose carrying place and mood, descriptive pacing, careful inventory, the writer's voice as a primary game element.
- **Graphical point-and-click adventures** — *Monkey Island*, the *Discworld* games. Click-based interaction, item-combining puzzles, characters with voice and warmth, exploration as pleasure, dialogue as gameplay.
- **Directly in the lineage of *The Institute* (Med Systems Software, 1981)** — one of the earliest dream-puzzle adventures, in which a patient in a mental institution navigates their own dreams to escape. The puzzle structure of dream-logic, the institutional setting, the surreal-mundane hybrid, the early-PC aesthetic of text and primitive graphics: all formative for what this game is doing. **The crucial inversion:** in *The Institute* the protagonist is the patient escaping their own dream. Here the protagonist is the *operator* entering someone else's. The genre is the same; the camera is on the other side of the chair.

## Core gameplay structure
The game alternates between **two modes**:

### 1. The dream-state (primary gameplay)
Each patient's dream is a **self-contained click-based adventure level**. Inside the dream:
- Explore the dream-world's locations.
- Find and collect items into an **inventory**.
- Solve **puzzles** rooted in the patient's psyche — find the right object, take it to the right place, have the right conversation, witness the right thing.
- Interact with figures the dream produces — including the patient's own dream-self, where appropriate.
- Each dream's **goal depends on the patient and their condition.** No two dreams are solved the same way.

**Success and failure:**
- **Success** — the puzzle is resolved correctly within the dream. The patient improves on waking. Progress is made.
- **Leaving without success** — the operator can always exit (the standing safety rule). Leaving early means the work was not done. The patient does not improve from that session. Re-entry is permitted within the patient's stay.

The dream's **persistence across sessions** (per `dreamworlds.md`) means a patient who needs multiple sessions has the *same* dream-world to return to. Items found, places mapped, and conversations had can be carried forward.

### 2. The house (hub world)
Between dreams, the player navigates the **Wren family home** as a point-and-click hub:
- Move between **locations** — consulting rooms, library, treatment room, gallery, dining hall, grounds, and others.
- Talk to other characters — Elias, Ashley's own thoughts, Mrs. Halloran, Alison, eventually Ryan, eventually Ezra.
- Read documents, books, and case files.
- Trigger scripted story events that move the larger narrative forward.

**Locations unlock progressively** as the story unfolds. The closed area of the house — the parents' suite where Ezra lives — is **not navigable at game-start.** It becomes accessible only after the mid-game pivot, when the silence around Ezra cracks. Other locations (an old outbuilding, a study drawer, a particular shelf) may unlock at other story beats.

## The case-file system
A persistent in-game archive Ashley can read at any time:
- **Current patients** — files for the patients in residence right now. Background, presenting issue, history, intake notes, prior session notes. This is the **diagnostic surface** that informs how to approach each dream.
- **Past patients** — successful cases already treated. Useful for cross-referencing patterns, recognising motifs, and grounding the player in the practice's history. Some past cases also seed hints for current ones.
- **Choosing whom to treat** — when multiple patients are in residence, the player chooses which one to interview, which one to enter. Elias proposes, the player picks. This makes case selection a meaningful decision rather than a fixed sequence.

The files themselves are **in-world artefacts**: Elias's clinical notes, sometimes in his hand, sometimes typed up by Edith, occasionally annotated by Ashley themselves once they have started seeing patients.

## The hint system
Adventure games stall when the player gets stuck, and the cure for being stuck cannot break the world. So:
- **Leaving the dream is the hint mechanism.** When Ashley exits a dream without solving it, they wake at the rig and can talk to Elias (or, late-game, alone with their own deductions).
- **Elias gives tips and suggestions for progression** in his particular register — clinical, patient, sometimes formal, occasionally piercing. He never simply tells the player the answer; he asks the right question.
- The hint system is therefore **also a relationship-building mechanism.** Every time the player struggles, they have another scene with Elias. The frequency of return shapes how the player comes to know him.
- Late-game, after the silence around Ezra breaks, the hint conversations can carry **new information** — fragments of his backstory that he could not have told earlier.

## Progression and pacing
- **Standard loop:** read patient file → interview patient → enter dream → solve (or retry) → patient improves → next case.
- **Scripted hub events** between sessions move the larger story forward (`arc.md`).
- **Mid-game pivot:** Ashley operates on Elias. This session unlocks Ezra's existence to Ashley and unlocks the closed area of the house.
- **Late game:** Ezra sessions become the chapter boundaries, interleaved with continuing patient cases.
- **Endgame:** the full backstory is exposed; Ezra is healed; the practice and the household resolve.

## Visual and aural register (open)
The game's visual style is to be decided. Possibilities that fit the tone:
- **Illustrated point-and-click** in the *Monkey Island* / *Discworld* tradition, with a more painterly, restrained palette suited to the dreamlike-surreal subject matter.
- **High-contrast pixel art** in the spirit of 80s adventures, with text doing the heavy lifting.
- **Mixed media** — handpainted backgrounds with rendered overlays, varied per-dream so each patient's mind has its own visual signature.

Sound and music undefined. The house has a record player; the dreams range from cosmic to mundane; both ends of that range have implications for score.

## Saves and persistence
Static hosting on GitHub Pages implies:
- **Browser `localStorage`** for save state.
- A single autosave plus possibly named save slots.
- No cloud sync; saves are local to the browser.

## Open design questions
- **Approximate length and scope** — how long is a full playthrough meant to be?
- **Multiple endings**, or a single resolution?
- **Failure permanence** — can a patient be treated wrongly and left damaged, or is the worst outcome merely "no improvement, try again"?
- **Visual style** — pick one of the directions above (or another).
- **Voice acting** vs text-only dialogue. Text-only honours the 80s adventure influence and is far cheaper; voice could elevate the late-game emotional beats.
- **Difficulty / hint density** — how generous are Elias's tips? Adjustable, fixed, or paced?
- **What happens when you fail to help every patient in residence within their week?** Does the unhelped patient leave? Does this affect later beats?