# Aiko voice lines: Lumisphere staging build

45 clips, English. Record each with the **exact filename** in the first column
and drop them in `assets/voice/en/`. Arabic later, same filenames, in
`assets/voice/ar/`, following the pattern already set in the `aiko-staging`
repo.

No emoji, no markup, nothing in brackets is spoken. The "when it plays" column
is there so the take can be performed right, not just read.

---

## Before you generate anything

**The voice is decided and recorded.** All 45 clips below were generated on
13 August 2026 with:

| | |
| --- | --- |
| Voice | **Aiko - Trial 1** |
| Voice ID | `aSnZCgQZDQBkk7weT1tf` |
| Model | `eleven_multilingual_v2` |
| Settings | stability 0.40, similarity 0.75, style 0.30, speaker boost on |
| Seed | CRC32 of the filename, so any single clip regenerates identically |

**Do not delete this voice from the ElevenLabs account.** It is a Voice Design
generated voice. If it is deleted it cannot be recreated, not even from the
same prompt, and all 45 clips would have to be remade in a different voice.

The `aiko-staging` repo's manifest listed 32 clips but none were ever recorded,
so there was no existing pack to match. This voice now sets Aiko for both
builds.

**Settings.** Eleven Multilingual v2, since Arabic is coming and switching
models later would change the timbre. Stability around 40, similarity 75, style
around 30, speaker boost on. Low stability makes Aiko expressive; going much
below 35 makes them erratic between takes. Export mp3 44.1kHz 128kbps, and I
will compress on the way in.

**Performance.** Warm, quick, a bit cheeky. On the child's side, never
instructing from above. Punctuation does more work than any slider: "Nice!"
and "Nice." are different performances of the same word. Aiko is amused by the
scammers, not frightened of them.

**Generate each line as its own clip.** One long file cannot be triggered at
the right moment.

---

## A. Welcome and hub (6)

| file | what Aiko says | when it plays |
| --- | --- | --- |
| `welcome-hello.mp3` | Hi. I'm Aiko. | Welcome screen, first words. Reuse `intro-greeting.mp3` if it exists |
| `welcome-invite.mp3` | There are three jobs in here, and not one of them is boring. Come on. | Welcome screen, straight after the greeting |
| `hub-pick.mp3` | Pick one. They are all completely different. | Hub, first arrival |
| `hub-locked.mp3` | Not that one yet. It is still cooking. | Child taps a locked placeholder card |
| `hub-back.mp3` | Back for another? Good. | Returning to the hub after finishing a game |
| `hub-alldone.mp3` | You did all three. Genuinely, that was good. | All three games complete |

## B. Night Shift (12)

Spotting scams. Messages fall, the child zaps the bad ones.

| file | what Aiko says | when it plays |
| --- | --- | --- |
| `ns-tut-1.mp3` | Messages drop towards your inbox. Zap the sketchy ones before they land. | Tutorial panel 1 |
| `ns-tut-2.mp3` | Your real friends drop too. Leave those alone. Let them land. | Tutorial panel 2 |
| `ns-tut-3.mp3` | Here is the trick. Scary words are not the clue. Watch what the message asks you to do. | Tutorial panel 3, the actual lesson |
| `ns-start.mp3` | Night shift. You are on. | Round begins |
| `ns-first-good.mp3` | That is it. That one wanted something off you. | First correct zap of a round |
| `ns-first-bad.mp3` | Ah. That was a real friend. Read what it asks for, not how loud it is. | First mistake of a round |
| `ns-streak.mp3` | Okay. You are quick. | Several correct in a row |
| `ns-lastlife.mp3` | Careful now. One more slip and we are done. | Down to the last life |
| `ns-wave.mp3` | Wave down. They come faster from here. | A wave is cleared |
| `ns-win.mp3` | You held the whole night. Nothing got through. | Game won |
| `ns-lose.mp3` | One got past us. Not the end of the world. Go again. | Game lost |
| `ns-takeaway.mp3` | Urgent, scary, or too good to be true. That is the pressure talking. Ask a grown-up before you tap. | The lesson, on the end screen |

## C. Breadcrumbs (11)

How small public details add up. The child plays the stranger.

| file | what Aiko says | when it plays |
| --- | --- | --- |
| `fp-tut-1.mp3` | You are the stranger this time. You are reading someone's posts. Tap anything that tells you something about them. | Tutorial panel 1 |
| `fp-tut-2.mp3` | On their own these are nothing. Together they add up to a real person. | Tutorial panel 2 |
| `fp-tut-3.mp3` | Then you go back and fix it. Deleting everything is not the goal. You score on how much you keep. | Tutorial panel 3 |
| `fp-first-clue.mp3` | One down. Keep going, and look at the pictures too, not just the words. | First clue found |
| `fp-decoy.mp3` | Good try. That one tells me nothing though. | Child taps a decoy |
| `fp-photo-hint.mp3` | Check the photo. People forget what is behind them. | Stuck with only caption clues found |
| `fp-half.mp3` | Halfway. I can almost picture them. | Four of eight found |
| `fp-allfound.mp3` | Eight. That is a name, a school, a street, and a face. From posts. | All eight found |
| `fp-fix-start.mp3` | Now fix it. Keep as much as you can though. They are allowed a life. | The repair phase begins |
| `fp-overdelete.mp3` | You deleted nearly everything. Safe, yes. Also a bit sad. | Child deletes almost every post |
| `fp-takeaway.mp3` | No single post gave them away. All of them together did. That is the whole trick. | The lesson, on the end screen |

## D. Vault (10)

What makes a password strong. A machine is cracking it in real time.

| file | what Aiko says | when it plays |
| --- | --- | --- |
| `pw-tut-1.mp3` | A machine is trying to crack your vault. The stronger your password, the slower it gets. | Tutorial panel 1 |
| `pw-tut-2.mp3` | Tap a word to add it. Random words slow it right down. Things about you barely help. | Tutorial panel 2 |
| `pw-personal.mp3` | Your dog's name? The machine guessed that one first. | Child adds a personal word |
| `pw-random.mp3` | Now that, it did not see coming. | Child adds a random word |
| `pw-long.mp3` | Longer is better. Boringly, that is most of the secret. | Password passes a good length |
| `pw-close.mp3` | It is nearly through. Give me something strange. | Cracker close to breaking in |
| `pw-held.mp3` | Held. Look how slowly it moved. | A vault survives |
| `pw-level.mp3` | Vault holds. The next one is tougher. | Level cleared |
| `pw-win.mp3` | Every vault held. That machine is going home. | Game won. Or reuse `mission-complete.mp3` |
| `pw-takeaway.mp3` | Long and random beats short and clever. And never the same one twice. | The lesson, on the end screen |

## E. Nudges (6)

These fire when a child stalls or taps empty space. They repeat more than
anything else in the build, so they need the lightest touch. Aiko is keeping
someone company here, not hurrying them.

| file | what Aiko says | when it plays |
| --- | --- | --- |
| `nudge-1.mp3` | Still there? | Idle, first nudge |
| `nudge-2.mp3` | Want a hand, or are you thinking? | Idle, second nudge |
| `nudge-3.mp3` | Take your time. I am not going anywhere. | Idle, third nudge |
| `nudge-4.mp3` | Try tapping one and see what happens. | Idle, still nothing after three |
| `nudge-wrong-1.mp3` | Not there. Warmer towards the middle. | Tapping dead space |
| `nudge-wrong-2.mp3` | Nothing there. Somewhere else. | Tapping dead space again |

---

## Notes for whoever wires these up

**Audio unlocks on the welcome tap.** Browsers block sound until the child
interacts with the page, so the "let's go" button on the welcome screen is the
unlock moment. Nothing can speak before it.

**Captions stay on screen regardless.** The voice is an enhancement and never
the only channel. A deaf child, a broken speaker, or a classroom with the sound
off must lose nothing.

**Classroom reality.** Thirty tablets all saying "Still there?" is not a
lesson, it is a riot. For AIA Lusail, either default to muted with headphones
as the opt-in, or remember the mute choice per device. The mute button already
exists, it just needs to persist.

**Weight.** 45 clips is roughly 1.8 MB served from Pages, which is fine. It
would not be fine inlined as base64 in a single-file build, so if this ever
goes back to a Claude artifact the voice track has to be dropped or streamed.
