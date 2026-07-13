# Rules

This document describes the current first-playtest rules. Anything marked
`Open` is intentionally unresolved.

## Game Premise

Rival chefs open restaurants on the same street and compete over multiple days
to convince a judge that their restaurant is the best. Players improve their
repertoire by learning dishes, techniques, and long-term support cards, then
present meals to move the judge's favor toward themselves.

The restaurant frame explains why learned cards enter the deck for future turns,
but the gameplay focus should stay on dishes and what the chef/player does.

## Players

- Designed first for 2 players.
- Multiplayer may be explored later with a different scoring wrapper.

## Main Terms

- **Time**: the resource spent to learn cards from the market.
- **Learn**: buy a card and add it to your deck.
- **Dish**: a card that may be presented as part of a meal.
- **Attach**: place a Dish under another Dish. An attached Dish adds its Taste
  and tags to the Dish it is attached to, but does not count as a separate
  presented Dish or course.
- **Taste**: the scoring value of a dish.
- **Favor**: progress on the judge track.
- **Peel**: remove a card from your deck permanently.
- **Reaction**: a card played during the opponent's interaction step.
- **Status**: a harmful or blank card added to a deck by effects.

## Win Condition

The judge starts at the center of a favor track. When a player gains Favor, move
the judge that many spaces toward that player. If the judge reaches a player,
that player wins.

Open: exact track length. Start by testing a short track so games end before
players want them to end.

## Starting Deck

Each player starts with:

- 5x `Prep`
- 3x `Simple Soup`

Suggested starter cards:

| Card | Type | Effect |
|---|---|---|
| Prep | Time | Gain 1 Time. |
| Simple Soup | Dish - Extra | Taste 1. |

Open: whether `Simple Soup` should be `Appetizer` instead of `Extra`.

## Always-Available Cards

These cards are not in the random market deck and can always be learned.

| Card | Cost | Type | Effect |
|---|---:|---|---|
| Practice Session | 3 | Time | Gain 2 Time. |
| Masterclass | 6 | Time | Gain 3 Time. |
| Simple Soup | 2 | Dish | Taste 1. |

Open: whether `Simple Soup` should be learnable from the always-available
market.

## Market

Use a Star Realms-style market row.

- Shuffle the market deck.
- Reveal 5 cards.
- Players may learn any visible market card by paying its Time cost.
- When a card is learned, refill the empty market slot immediately.

The first card a player learns each turn goes on top of the appropriate deck
instead of the discard pile. Usually this means the learner's deck. If a card
causes the opponent to gain a Status, that Status can go on top of the
opponent's deck if it is the first card learned that turn.

Open: whether every first learned card should topdeck, or only some cards.

## Turn Structure

On your turn:

1. Cook: play cards and learn cards in any order.
2. Present your final meal.
3. The opponent has one interaction step and may play Reactions.
4. Score your presented meal and move the judge.
5. Discard played cards, presented dishes, and unplayed hand cards.
6. Draw a new hand.

Open: exact hand size. Start by testing 5.

## Drawing And Reshuffling

Played cards stay in a play area until cleanup. Presented dishes stay in the
presented meal until cleanup. They do not immediately go to the discard pile.

When a player must draw or reveal from an empty deck, shuffle that player's
discard pile to form a new deck, then continue drawing or revealing. Cards
played this turn, presented this turn, or learned this turn are not in the
discard pile unless an effect explicitly put them there.

## Presenting Dishes

After the Cook step, a player presents dishes from their hand as a final meal.
Course labels matter, but they are not hard slots for now: a meal may include
duplicate course types.

Card effects resolve when played by default. Effects that depend on the final
presented meal should say `During judging`.

During the Cook step, effects that modify a Dish may target a Dish in hand.
Those modifiers apply if that Dish is presented this turn.

Current course types:

- Appetizer
- Main
- Dessert
- Extra

Only presented dishes contribute Taste unless a card says otherwise. Dishes that
are not presented may still have play effects if the card allows it.

Meal bonuses:

- Present at least 2 distinct core courses: gain +2 Favor.
- Present Appetizer, Main, and Dessert: gain +5 Favor.
- Extra dishes do not count toward completing the core meal unless a card says
  otherwise.

Open: exact course bonus values and whether there should be a maximum number of
presented dishes.

## Interaction

The opponent gets one interaction step before scoring. Reactions are the main
interaction card type.

First-test constraint:

- A player may play at most 1 Reaction during each interaction step.

Interaction should create tension without routinely erasing the satisfaction of
presenting a meal.

## Status Cards

The first Status card to test is:

| Card | Type | Effect |
|---|---|---|
| Distraction | Status | No effect. |

Cards may give the opponent a `Distraction`. `Distraction` can be Peeled.

## Factions

The current factions are:

- French
- American
- Japanese
- Italian

Each faction has access to exactly 3 dish tags. Each tag is shared by exactly 2
factions. See [faction_tag_access.csv](../data/faction_tag_access.csv).

## Dish Tags

The strict tag set is:

- Meat
- Seafood
- Cheese
- Fried
- Tomato
- Rice

For now, dishes should only use these tags, and only if their faction has access
to that tag.
