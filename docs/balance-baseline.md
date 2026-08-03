# Balance Baseline

This document is a provisional pricing model for reviewing cards. It is not a
hard formula. Use it to find cards that are probably too efficient, too weak, or
too swingy before playtesting.

## Core Assumption

Printed `time_cost` is treated as the Time cost to learn a card, not as an
additional Time cost to play it after it is in the deck.

If Techniques or Reactions later cost Time to play, this model must be rebuilt.

## Value Points

Use `value points` as a rough one-turn scoring equivalent.

| Effect | Baseline value |
|---|---:|
| +1 Taste this turn | 1 |
| +1 Favor | 1 |
| +1 Time during Cook | 1 |
| +1 Time during judging or After-service | 0.75 |
| Draw 1 | 1.25 |
| Draw N then discard M | about `1.25 * (N - M) + 0.5` |
| Look at top N, put 1 into hand | 1.75 to 2.25 |
| Look at top N, put 2 into hand | 3.25 to 4 |
| Peel a chosen starter card | 1.25 early, 0.5 late |
| Peel any chosen card | 1.5 early, 0.75 late |
| Peel this card | 0.75 to 1 |
| Flexible course slot | 1.25 to 1.75 |
| Give an opponent Distraction | 1.25 in 1v1 |
| Give an opponent a harmful Status | 1.75 to 2.5 in 1v1 |
| Each opponent gets an effect | scale almost linearly with player count |
| Scorch 1 yourself | -0.75 to -1.25 |
| Market rotation | 0.5 to 1.5, depending on how stuck the market is |

Notes:

- Taste and Favor are priced equally because both move the current scoring turn
  toward winning. Taste is more interactable; Favor is more final.
- Card draw is below raw card count because drawn cards still need useful
  contents, but it is above 1 because it finds Time, dishes, and Reactions.
- Time generated during judging is discounted because the post-judging phase is
  buy-only.
- Status value should be retuned after multiplayer tests. `Each opponent`
  effects are intentionally silly, but they can become much stronger in 3+
  players.
- Scorch is intentionally hard to price. It can remove bad cards, but it often
  destroys future purchases. For now, assume it is a real downside.

## Expected Value By Learn Cost

| Learn cost | Expected value | Typical dish shape |
|---:|---:|---|
| Starter | 1 | `Prep` gives 1 Time; `Simple Soup` gives 1 Taste. |
| 2 | 3 | 1 to 2 Taste plus a strong slot, tag, or synergy hook. |
| 3 | 4 to 4.5 | 2 Taste plus reliable upside, or a focused action. |
| 4 | 5.5 | 3 Taste plus relevant upside, or a strong utility action. |
| 5 | 7 | 4 to 5 Taste plus upside, or a high-impact build card. |
| 6 | 8.5 | Major build-around, economy jump, or memorable swing. |
| 7 | 10+ | One-copy faction cards, quests, or game-warping passives. |

For dishes, the printed Taste should usually be below the expected value because
course completion, tags, and recurring deck value matter. A fair dish often hits
the table below rate and reaches rate when its condition or archetype works.

## Current Outlier Report

These are first-pass estimates from the current card pool, not requested
changes.

### Probably High

| Card | Why it looks high |
|---|---|
| `Hot Dog` | Cost 2, 2 Taste floor, can become 4 Taste plus 1 Time. That is far above the cost-2 target when the duplicate-Main condition is easy. |
| `Taste Test` | Cost 2 for draw 3, discard 1, with possible Peel. This is premium selection at the cheapest market tier. |
| `Doomscroll The Menu` | Cost 2 for top-5 keep-2 is near a cost-3 effect. The self-Distraction matters, but status-synergy decks may turn the drawback into upside. |
| `Mamma Mia!` | Cost 3 for Dish tutoring, discard setup, draw 1, presentation permission, and possible Time. It has a lot of text that all points in the same direction. |
| `Secondo` | Cost 3 is fair on a 3-Taste Main, but becomes explosive with 5+ Taste Mains or spicy cards. Watch the ceiling. |
| `Freedom Isn't Free Refills` | Cost 3 for 2 Time, each opponent gets Food Coma, and a possible Favor. This is especially high in multiplayer. |
| `Health Inspector Raid` | Cost 4 each-opponent harmful Status plus full market rotation. Multiplayer scaling may be brutal. |
| `Foreigner Mistrust` | Cost 5 passive that gives every opponent a harsh Status every turn. This can dominate multiplayer games if it sticks. |
| `Wage Inequalities` | Cost 5 repeatable each-opponent Strike trigger. French already has several 5+ Taste routes. |

### Probably Low

| Card | Why it looks low |
|---|---|
| `Simple Soup` as always-available learn | Cost 2 for 1 Taste is below rate. This is acceptable only if it is intentionally a fallback/starter-quality purchase. |
| `Onigiri` | Cost 2, 1 Taste, and no card goes to hand from the top-deck look. It mostly becomes fair only when Status cleanup matters. |
| `Tasting Menu` | Cost 4, 2 Taste Flexible, and conditional 1 Time. It looks weak beside two cheaper flexible/slot-fixing purchases. |
| `Masterclass` | Cost 6 for 3 Time is a poor upgrade over `Practice Session` at cost 3 for 2 Time. It likely needs a stronger economy jump or a lower cost. |
| `Cheese Wheel` | Cost 5 for +1 Taste to Cheese dishes needs several future Cheese presentations to pay off. It is narrow compared with other passives. |
| `Algorithmic Menu` | Cost 4 for a top-2 filter each turn is useful, but it may be too slow unless Status discard happens often. |

### Swingy Or Needs Data

| Card | Watch item |
|---|---|
| `Wasabi Challenge` | Raw cost-2, 4-Taste pressure is huge. Whether it is fair depends on how painful Scorch 2 feels. |
| `Ghost Pepper Wings` | Cost-3, 6-Taste pressure can end games quickly. This may be correct for the spicy archetype, but it should feel scary. |
| `Less Is More` | Cost 3 for +5 Favor is either excellent or dead depending on how often exact core meals happen. |
| `Perfect` | Usually fair, but doubles any future outlier dish. It amplifies spicy cards and `Foie Gras Toast`. |
| `Supersize Me!` | Similar issue to `Perfect`: fair as a splashy one-copy card, dangerous with very high-Taste dishes. |
| `Review Bomb Campaign` | Alternate win cards are hard to price. It may be unplayable if 7 tokens is too slow, or oppressive if status decks trigger it incidentally. |

## Practical Review Rule

When reviewing a new card:

1. Estimate its floor value with no synergy.
2. Estimate its normal value in the deck that wants it.
3. Estimate its best-case ceiling.
4. Compare normal value to the learn-cost table.
5. If the floor is above rate, the card is probably too safe.
6. If the ceiling is far above rate, the setup should be narrow, funny, or risky.
7. If the normal case is below rate, the card should either be cheaper or carry
   a clearer archetype payoff.
