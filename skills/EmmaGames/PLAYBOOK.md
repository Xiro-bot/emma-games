# Playbook — what works for a 5-year-old (Emma)

_Running list of lessons. Add a line whenever we learn something. Newest on top._

- **A recipe panel teaches; the spoken step does the work.** She can't read, so the on-screen ingredient/step list is for *recognising* (pictures + ✓ + a gold highlight on the current line) while the actual instruction is spoken. Both together = she can follow a real recipe.
- **Show only what the current step needs.** In the bakery only the current step's ingredient cards appear on the shelf, pulsing. Wrong-thing-at-the-wrong-time can't happen, so the order itself is what she learns — no scolding needed.
- **Count multiples out loud.** "One! Two! Three!" as she drags the third egg in turns a chore into counting practice.
- **Scale the whole scene to the screen.** A multi-station scene should scale *up* on a big screen, not just down on a small one — bigger targets are strictly better for a 5yo. (`fitStage()` in cake-bakery.)
- **Watch what the hint bubble covers.** A bubble anchored above a target can land on top of the very cards she needs to drag — clamp it below them.

- **She can't read but knows letters** (almost 6, as of Aug 2026) — words in games need a picture cue + the word spoken aloud; letters themselves are fair game.
- **Keyboard games: put a mirror keyboard on screen.** For no-look typing, highlight the target key on an on-screen keyboard so she finds keys on the screen instead of staring at her hands. Layout must match the physical keyboard (QWERTZ/QWERTY toggle).

- **Hidden rewards beat marked ones — if popping is fun by itself.** We first marked the candy balloons; Emma's dad asked for the candy to be hidden (1 in 5, no tell) so every pop is a little suspense. Works because the action itself (pop!) is already the fun part, so a "miss" costs nothing. Mark the target instead when the action is a chore.
- **When the reward is a surprise, make the reveal loud.** Golden shockwave ring + "CANDY!" + sparkles + flight into the jar — the moment has to be unmistakable since nothing announced it in advance.
- **Make hit-testing forgiving, and bias it toward the rewarding target.** Full bounding box + a margin, and when two targets overlap, the one that pays out wins the click — a 5yo reads a stolen click as "the game is broken".
- **Sandbox / no-lose modes work too.** Not every game needs a win/lose loop — a dress-up sandbox (drag clothes onto models) lets her create freely, with an on-demand "Start Show!" reward button. Give creative play a big optional celebration rather than a fail state.
- **Draw clothes/props in CSS, not emoji.** Emoji read as "stickers" (her complaint on cups). Hand-draw with gradients + shapes.
- **Default to the easiest setting.** Emma called the first build "too hard." Ship the gentlest version first; let difficulty scale up with optional buttons.
- **Slow and steady beats fast.** On Easy, cups should move slowly and NOT speed up over time. Speeding-up is brutal for little kids.
- **Give a long preview.** Show the treasure/goal for ~3 seconds before the challenge starts.
- **Make the goal unmissable.** Big emoji, glow halos, gentle bobbing/spinning animation. (We lost the coin/diamonds once because they were hidden — visibility is critical.)
- **Reward big.** Fairy + confetti + spoken "Congratulations!" lands well. Tap-anywhere to dismiss.
- **Mouse-driven.** She uses a mouse; the cursor-as-magic-wand is a hit. Avoid keyboard controls.
- **Themes she loves:** treasure, gold, diamonds, hearts, rainbows, fairies, wands, sparkles.
- **Encouraging on loss.** Never harsh. "So close! Try again! 💪" and reveal the answer.
