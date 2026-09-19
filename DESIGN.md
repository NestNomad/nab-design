# Nest Nomad & Beyond

Home, road and portable tech, tested for real.

This is the visual system for NNB video: YouTube long-form, Shorts, and the animated graphics that sit over our B-roll. We film faceless or semi-faceless with scripted voiceover, so the graphics do a lot of the talking. The frame is dark, and colour tells the viewer which part of the brand they are watching.

## The palette

This is the only palette for new work. The older bright set (#FF0664, #FADB0F, #71F49C, #000000) is retired for anything made from now on. Older assets that still use it get swapped when they are next touched, not all at once.

| Token | Value | Job |
| --- | --- | --- |
| ground | #1a1c16 | NNB black. Every frame background, never pure black. |
| panel | #23251c | Plates and cards on the ground. |
| line | #34362b | Decorative hairlines and tracks. Never text. |
| scrim | ground at 80% | Behind text laid over B-roll. |
| white | #ffffff | Primary text. |
| white-muted | white at 50% | Secondary text, 40px and up. |
| nest | #1d9e75 | Nest green: home and smart tech. |
| nomad | #ef9f27 | Nomad yellow: outdoor and adventure. |
| beyond | #d4537e | Beyond pink: portable tech. |

## Colour means pillar

Each video takes one pillar colour as its accent, and only that one. A home battery video is Nest, so its lower thirds, chapter cards, highlights and progress bars are Nest green. A camping chair review is Nomad yellow. A portable power station review is Beyond pink.

The other two pillar colours appear in one place only: the three-dot mark, where all three sit together in name order (nest, nomad, beyond). Over a run of videos, viewers learn the colour before they read the title. Mixing pillar accents inside one video breaks that, so we don't.

## Contrast, measured

WCAG 2 contrast ratios. 4.5:1 is the bar for normal text, 3:1 for large text.

| Pair | Ratio | Rule |
| --- | --- | --- |
| white on ground | 17.2:1 | Any size |
| white on panel | 15.5:1 | Any size |
| white-muted on ground | 5.2:1 | 40px and up |
| white-muted on panel | 5.0:1 | 40px and up |
| nomad on ground | 7.9:1 | Any size |
| ground on nomad | 7.9:1 | Any size. The go-to for text on a pillar fill |
| nest on ground | 5.1:1 | Any size |
| ground on nest | 5.1:1 | Any size |
| beyond on ground | 4.4:1 | 48px and up |
| ground on beyond | 4.4:1 | 48px and up |
| white on beyond | 3.9:1 | 64px and up |
| white on nest | 3.4:1 | 64px and up |
| white on nomad | 2.2:1 | Never |

On pillar fills, dark text beats white every time. White only goes on nest or beyond at title sizes.

Panel sits at 1.1:1 against ground and line at 1.4:1, so neither reads as a shape on its own. Give a plate a pillar-coloured edge or dot, and never let a hairline carry meaning.

Over footage the numbers above no longer hold, because B-roll can be bright. Never set text straight onto B-roll: put it on a panel plate or the scrim.

## Type

Work Sans for everything, from 120px chapter titles down to 36px source notes. Weight does the work that a second typeface would: 800 and 700 for titles, numbers and names, 500 and 400 for supporting lines. It is a free Google Font.

Sizes are for a 1920x1080 frame, not a web page, which is why they are big. In a phone's portrait player the whole frame shrinks to roughly a fifth of its width, so 48px on the timeline shows at about 10pt and 64px at about 13pt. That makes 64px the floor for any point a viewer has to read, and keeps 36px for text nobody needs.

| Style | Size | Weight | Use |
| --- | --- | --- | --- |
| title-xl | 120px | 800 | Chapter and title cards, five words or fewer |
| title | 88px | 700 | Section headings, verdict cards |
| callout | 64px | 700 | Key numbers, single-line points |
| lower-third | 48px | 700 | Lower-third main line |
| support | 40px | 500 | Lower-third second line, spec labels, units |
| small | 36px | 400 | Sources and affiliate notes only |

## The frame

- Keep all text 96px in from the sides (safe-x) and 54px down from the top (safe-y).
- Keep essential text out of the bottom 150px (clear-bottom). YouTube's controls, progress bar and our captions live there.
- Lower thirds sit bottom left, just above that line, left aligned. Never centred.
- Plan the final 20 seconds as end screen. YouTube lays its own elements on top, so keep that stretch free of our text.
- Spacing steps: space-sm 16px, space-md 32px, space-lg 64px.
- Corners: radius-sm 8px for plates and tags, radius-md 16px for cards, radius-full for pills. The dots are true circles.

## Motion

- One move per element. It arrives, holds and leaves.
- Ease out on the way in, ease in on the way out. Nothing bounces or wobbles.
- The pillar colour moves first (the bar, the dot), then the words follow it in.
- Hold text for at least 1.5 seconds, plus about a third of a second per word, which is roughly BBC subtitle pace. If a point matters, hold it longer.
- Colour arrives with its element. No colour cycling, no gradients.

## On-screen words

Same voice as everything else we make. Sentence case, plain words, British spelling. No em dashes, no exclamation marks, no hype. If it would sound odd said out loud to someone you just met over a coffee, rewrite it.

## The mark

The three-dot wordmark goes in assets/logo/ and isn't there yet. The dots run in name order: Nest green, Nomad yellow, Beyond pink. If the current file still uses the old bright pink, yellow and green dots, it needs recolouring before it goes on screen. Until it is uploaded, set the name in Work Sans 800 in white.

## Components

Three starter graphics live in components/, each built only from the tokens: lower-third.html, chapter-card.html and stat-callout.html. New graphics follow the same pattern: one pillar class on the frame, sizes from the type scale, timings from the motion tokens in tokens/tokens.css (enter 500ms, exit 400ms, 150ms stagger).

## Do not

- Use pure black (#000000) anywhere.
- Put white text on Nomad yellow.
- Set Beyond pink text below 48px.
- Use two pillar accents in one video.
- Put text straight onto footage without a plate or scrim.
- Use the retired bright palette on anything new.
