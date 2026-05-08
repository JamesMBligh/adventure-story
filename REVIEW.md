# Review of story/ corpus

A pressure-test of the load-bearing rules, internal consistency, and game-design implications across all current story files. Not a list of fixes — a list of places worth deciding before more material accretes on top.

## What's working

- **Premise has a real engine.** "The dream IS the therapy" is the kind of single-sentence rule that drives everything — narrative stakes, ethical weight, gameplay loop, and the precedent (Ezra) all flow from it cleanly. Most game premises don't have this much load-bearing in one rule.
- **Asymmetry of risk** is the right ethical spine. It's also recursive: Wren broke it once and his entire life is the consequence; Ashley enacts it daily; the game can pull on the moment they realise what that asymmetry actually *is*. That's a structurally rich choice.
- **Two-layer deception** (patients deceived about hypnotherapy; Ashley deceived about Ezra) gives the mid-game pivot something real to do. Both layers are seeded in the opening — [the_offer.md](scenes/the_offer.md) already plants the unguarded "Ez," the closed wing, the conservatory exit phrase.
- **Cross-references are disciplined.** Files restate load-bearing facts to stay self-contained, and the cross-links are accurate. README is a real index, not a rationalisation.
- **The opening scene works.** Whitfield as tutorial is well-chosen — recognizable dream geography, "witness, not exorcism" intervention, two prior observer sessions for grounding, and the exit phrase delivered as part of the briefing.
- **Recurring motifs land.** The conservatory shows up in [clinic.md](clinic.md), [collaborator.md:48](collaborator.md:48), [the_offer.md:11](scenes/the_offer.md:11), and as the exit phrase. The fact that *the safety word is a reference to Ezra that Ashley doesn't yet know* is the kind of detail that justifies the planning.
- **Timeline is consistent.** Carters early-20s twenty years ago → early-40s now; Ryan 15; Ashley mid-20s, arrived a year ago; Edith somewhere in the longer middle. No drift across files.

## Internal consistency / load-bearing concerns

1. **"Operators are structurally safe" is asserted as physics, but the empirical basis is n=1.** The rule rests on "Wren operated, and he was fine; Ezra was the patient, and he was destroyed." That's one operator and one patient — a sample of one. [device.md:42–44](device.md:42) acknowledges this ("operator safety has been demonstrated"), but the rest of the corpus treats it as inviolable physics. Decide which it is. **Story-physics rule** (the wiring is genuinely asymmetric — operator's neural interface is non-writable, patient's is) is a much stronger foundation than **empirical generalisation Wren has elevated to dogma**, which leaves the rule available to be falsified for plot. Either is fine; right now the documents are subtly using both at different moments.

2. **The chimpanzee phase is metaphysically awkward.** [history.md:55–60](history.md:55) says Wren tested the rebuilt rig on animals "culminating in a chimpanzee" before resuming human trials. But the device's whole point is that "the dream IS the therapy" — psychological intervention via dream-logic. What did chimp testing actually test? Two possibilities, very different in implication:
   - **Physical-safety testing** (sedation, neural coupling, vitals, exit mechanism). Plausible. But then the chimp phase tells you nothing about the *patient-safety* claim that matters most — i.e. that the operator's actions inside a dream don't break the dreamer's mind. Which means the ethical leap from chimps to humans is not actually validated by the chimp work.
   - **Psychological-intervention testing**, which is incoherent — there's no "knot to resolve" in a chimp's dream-state.

   Either way, the line between "Wren earned his right to use the device on people" and "Wren told himself a story to give himself permission" gets fuzzier the harder you press. Worth deciding what the chimp phase actually demonstrated, in his own honest accounting, and what it didn't.

3. **The "no-monitor session for Ashley's treatment" is a heavier sin than the prose lets on.** [device.md:25–29](device.md:25) is the cleanest statement: "Wren chose to risk *them* — not himself." But the rest of the corpus tends to land softer — "the original sin," "the foundation of their bond" — wording that romanticises what was, in straight terms, *Wren chose to put a sedated patient at risk to save his own time/effort/secrecy*. Ashley accepting it after the fact does not make the act lighter. Worth being honest with yourself that this fact is bleaker than the surrounding tone admits, and deciding whether the story holds that bleakness or softens it. The documents currently soften it.

4. **Ashley's complicity vs. Ashley's player-avatarness, in tension.** [clinic.md:19](clinic.md:19) says "Ashley is now complicit in the deception of every new patient" — they have been doing this for a year before the game starts. But the character is being framed as the morally clean viewpoint character the player slips into. A year of complicity is not morally clean. Either:
   - Ashley feels the friction of that complicity and the documents need more language showing it (right now they read as having metabolised it cleanly, which is dramatically convenient but psychologically thin), or
   - Ashley is genuinely past it, and the player has to be brought along with that — which means the story needs a between-session beat early on that *names* the moral situation rather than assuming it.

   Currently the documents do neither, and the player will arrive in a more uneasy position than the protagonist's interiority suggests.

5. **Ezra's signature damage and operator safety, reconciled.** [collaborator.md:62–66](collaborator.md:62) — Ezra's permanent state is "the device's signature dream-state running in a waking mind." Excellent. But: Elias was inside the same dream and walked out fine. The asymmetry has to be physically grounded. Sedation? Yes — but sedation alone doesn't explain why dream-events write onto the patient's mind structurally. The story has a buried explanation it hasn't quite said: the device *writes through* the patient's neural interface and *reads through* the operator's. If that's the rule, say it once, in [device.md](device.md), and then everything else follows. If it's not the rule, the asymmetry needs another grounding — because right now it's stated as a brute fact and Ezra's specific damage is exactly the kind of thing that should also have happened to Elias.

6. **What happens when Ezra wakes is unsolved, and it's the actual ending.** [arc.md:62–67](arc.md:62) lists "the final state of the household" as an open question. But Ezra waking up with a sound mind means Ezra waking up to the knowledge that:
   - His brother broke him.
   - The clinic uses the device they co-built, on non-consenting patients, paid for partly by his own care.
   - Ashley exists, was deceived twice, and was used to recover him.
   - Twenty years of his life are gone.

   This is enormous, and "the closing material has to wrestle with it" understates the work involved. The actual climax of the game is probably not the operation that wakes Ezra; it's the conversation Ezra has with Elias afterward, and what Ashley does once Ezra's testimony breaks the operation open. Worth at least sketching the shape of that ending now, even loosely — the rest of the design will be making promises it has to cash, and right now nobody knows what currency.

## Game-design risks worth flagging

7. **16 patients in [patients.md](patients.md) is more than the format will support.** Each case is "a self-contained click-based adventure level" with its own dream-world, art, and intervention shape. Sixteen of those is multiple person-years of design. Decide on a target — probably 6–10 fully-realised cases — and explicitly demote the rest to "mentioned in case files but never visited" so they're available as in-world texture without being commitments.

8. **Hint system has a soft spot.** [design.md:48–52](design.md:48) makes Elias's hint conversations the late-game backstory drip. Fine. But a player who doesn't get stuck never triggers them, and misses the drip. Either: (a) those conversations also fire when the player chooses to leave a dream and report progress, regardless of stuckness; (b) the [arc.md:32–33](arc.md:32) "scripted hub events" are the *primary* drip and hints are a bonus. Pick one, in writing.

9. **Variable dream-time has no gameplay teeth yet.** [dreamworlds.md:42–43](dreamworlds.md:42) — "1:1; hours-inside-for-minutes-outside; some go the other way." Atmospheric, but unless outside-time is tracked and creates pressure (a patient's session has a real-time budget; multiple patients in residence have overlapping schedules), it's purely decorative. Decide whether outside-time matters mechanically. If yes, the simulation needs it. If no, scale back the rule so it doesn't promise something the game won't deliver.

10. **Rendered-narration register vs. [the_offer.md](scenes/the_offer.md).** The scene's prose is long-form literary first-person. The cabin demo's narration is short second-person ("You stand in a moonlit clearing"). The actual in-game text will be much closer to the cabin's register than to the offer's, because it has to be read off a small narration panel between clicks. Worth a stylistic note in [design.md](design.md) about what the in-game narration voice actually is — the offer can be a cutscene-style set piece, but it can't be the standard texture. Otherwise there's a quality cliff between "the prose in the doc" and "the prose on screen."

11. **Gender-neutrality rule is well-executed in first-person; third-person dialogue is the test bench.** [the_offer.md](scenes/the_offer.md) holds the rule perfectly because it's narrated by Ashley. Other characters describing or addressing Ashley in dialogue is where pronouns and connotation will leak — old patients reminiscing, Mrs. Halloran clucking, Ezra's late-game confusion. Worth a single passage somewhere of someone speaking *about* Ashley to verify the constraint can be held in third-party voice. Right now there's no such test in the corpus.

## Documentation hygiene

12. **Mrs. Halloran is underdeveloped relative to her role.** Inner-circle, knew about Ezra "for years," the household's domestic spine, complicit in the silence about Ashley — and yet has no `halloran.md`. Compare the depth of [nurse.md](nurse.md). She's the obvious next character file.

13. **Repetition is high across files.** The "operator safe / patient not" rule is restated, in slightly different words, in at least six files. It's deliberate (each file is self-contained) but it means a future revision to the rule has to land in six places consistently. Either accept the maintenance burden explicitly, or designate one file as canon and replace the restatements in others with one-line summaries plus a link. Lean toward the second once the rule-set settles.

14. **Open-questions sections drift.** Every file has its own list of open questions; some are answered elsewhere already (e.g., [device.md:69–75](device.md:69) asks "Who was the collaborator?" — answered in [collaborator.md](collaborator.md)). Worth a sweep to retire open questions that are actually closed.

## Smaller things

- **Time scale of the disgrace and the network.** [history.md:44](history.md:44) says old colleagues "have not heard from Elias in decades." [clinic.md:76](clinic.md:76) says he takes referrals from "a thin network of old colleagues." Reconcilable (someone's still talking to him), but say so once.
- **Ryan is a Chekhov's gun.** Fifteen-year-old, on the property during holidays, "knows there is a man he doesn't see." If Ezra wakes during a school holiday, Ryan is the one civilian who'll be present at the seam. Either pay him off or scale him down.
- **The third chair as gameplay.** Observer mode (Ashley present-but-not-acting in someone else's session) is mechanically distinct from operator mode and could carry a beat — e.g., Ashley observes Elias on a late case and learns something about him from the inside. The current arc puts Ashley in the operator chair from session one; the observer mechanic is in the rules but unused. Worth deciding whether it earns its space.
- **Edith parallel to Ashley.** Both healed by Wren, both stayed, both complicit in different layers of the silence. There's more potential in that parallel than the docs currently mine — could be the heart of a strong scene.
