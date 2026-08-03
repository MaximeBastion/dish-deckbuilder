# Rules

This document describes the current playtest rules. Anything marked `Open` is
intentionally unresolved.

## Game Premise

Rival chefs open restaurants on the same street and compete over multiple days
to convince a judge that their restaurant is the best. Players improve their
repertoire by learning dishes, techniques, and long-term support cards, then
present meals to move the judge's favor toward themselves.

The restaurant frame explains why learned cards enter the deck for future turns,
but the gameplay focus should stay on dishes and what the chef/player does.

## Players

- Designed first for 2 players.
- Multiplayer playtests can use the same turn structure: each opponent gets a
  chance to interact, and every player's board stays visible until that player
  starts their next turn.
- Multiplayer uses a separate Favor total instead of the 1v1 tug-of-war judge
  track.

## Main Terms

- **Time**: the resource spent to learn cards from the market. Unspent Time is
  lost at the end of the turn unless a card says otherwise.
- **Learn**: buy a card and add it to your deck.
- **Dish**: a card that may be presented as part of a meal.
- **Attach**: place a Dish under another Dish. An attached Dish adds its Taste
  and tags to the Dish it is attached to, but does not count as a separate
  presented Dish or course.
- **Taste**: the scoring value of a dish.
- **Favor**: progress toward winning over the judge.
- **Peel**: remove a card from your deck permanently.
- **Scorch N**: Peel the top N cards of your deck. This is a risky version of
  Peel used by spicy, high-Taste cards.
- **Reaction**: a card played during an opponent's interaction step.
- **Status**: a harmful or blank card added to a deck by effects.
- **Board**: the cards a player played or presented on their most recent turn.
  The board stays visible until the beginning of that player's next turn.
- **Fridge / Frigo**: a one-card reserve slot, inspired by Flesh and Blood's
  arsenal. A card in the Fridge is saved for a later turn instead of being
  discarded with the rest of the hand.

## Win Condition

In 1v1, the judge starts at the center of a favor track. When a player gains
Favor, move the judge that many spaces toward that player. If the judge reaches
a player, that player wins.

With 3 or more players, each player tracks their own Favor total instead. When a
player reaches 20 Favor, that player wins.

Open: exact 1v1 track length and multiplayer Favor threshold. Start by testing
a short 1v1 track and a 20-Favor multiplayer threshold so games end before
players want them to end.

Open: whether the multiplayer threshold should also replace the 1v1 judge
track. The distinction is flavorful in 1v1, but one unified scoring system may
be easier to teach and balance.

For card text:

- In 1v1, the judge favors the player whose side of the track the judge is on.
  At the center, the judge favors nobody.
- With 3 or more players, the judge favors the single player with the most
  Favor. If there is a tie for the most Favor, the judge favors nobody.
- `If the Judge favors you` only applies when you are that favored player.
- `If the Judge does not favor you` only applies when another player is favored.
  It does not apply when the judge favors nobody.

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
causes an opponent to gain a Status, that Status can go on top of that
opponent's deck if it is the first card learned that turn.

Open: whether every first learned card should topdeck, or only some cards.

## Turn Structure

On your turn:

1. Start of turn: discard your board from your previous turn.
2. Draw 5 cards.
3. Cook: play cards and learn cards in any order.
4. Present your final meal.
5. Opponents have one interaction step and may play Reactions.
6. Score your presented meal and gain Favor.
7. After-service: learn cards by spending remaining Time. This is when you can
   spend any Time gained during judging.
8. Fridge: if your Fridge is empty, you may put 1 card from your hand into your
   Fridge.
9. Discard any remaining unplayed hand cards. Cards on your board stay there
   until the beginning of your next turn.

Open: exact hand size. Start by testing 5.

When you draw cards during another player's turn, keep those cards in your hand.
At the start of your next turn, still draw the full hand size. This keeps
Reaction draw effects meaningful.

Effects that say `at the start of your turn` resolve during step 1, after board
cleanup and before drawing, unless the card says otherwise.

During After-service, you may learn cards from the market or always-available
cards. You may not play cards, present dishes, or resolve non-learning effects
unless a card explicitly says otherwise.

## Board, Cleanup, And Drawing

Played cards and presented dishes stay on that player's board after scoring and
after the After-service step. They do not immediately go to the discard pile.

At the beginning of a player's next turn, that player discards all cards on
their board, then draws 5 cards. This makes each player's most recent meal
available for comparison during other players' turns.

Only the active player cleans up their own board at the beginning of their turn.
Other players' boards remain visible until those players' next turns.

When a player must draw or reveal from an empty deck, shuffle that player's
discard pile to form a new deck, then continue drawing or revealing. Cards
currently on a board, in a Fridge, or learned this turn are not in the discard
pile unless an effect explicitly put them there.

When an effect tells a player to look at the top N cards of their deck and that
deck has fewer than N cards, that player may shuffle their discard pile into
their deck before looking. If they do not, they look at as many cards as are
available.

## Fridge / Frigo

Each player has one Fridge slot.

- A Fridge can hold at most 1 card.
- During the Fridge step at the end of your turn, if your Fridge is empty, you
  may put 1 card from your hand into your Fridge.
- Cards in the Fridge are face down.
- Cards in the Fridge are not in your hand, deck, discard pile, or board.
- On your turn, you may play a card from your Fridge as if it were in your hand.
- If a card leaves the Fridge, the Fridge becomes empty.

## Presenting Dishes

After the Cook step, a player presents dishes from their hand, Fridge, or cards
played this turn as a final meal. Course labels matter, but they are not hard
slots for now: a meal may include duplicate course types.

Card effects resolve when played by default. Effects that depend on the final
presented meal should say `During judging`.

During the Cook step, effects that modify a Dish may target a Dish in hand, in
your Fridge, or on your board if it was played this turn. Those modifiers apply
if that Dish is presented this turn.

Current course types:

- Appetizer
- Main
- Dessert
- Extra
- Flexible

Only presented dishes contribute Taste unless a card says otherwise. Dishes that
are not presented may still have play effects if the card allows it.

When you present a Flexible dish, choose whether it counts as Appetizer, Main,
Dessert, or Extra for that judging. Flexible dishes are intentionally inefficient
on raw Taste, but they help complete awkward meals.

Because boards persist until the beginning of their owners' next turns, effects
may compare against presented dishes on other players' boards. A dish that was
part of a player's judged meal is still that player's presented dish until that
player cleans up their board.

Meal bonuses:

- Present at least 2 distinct core courses: gain +2 Favor.
- Present Appetizer, Main, and Dessert: gain +5 Favor.
- Extra dishes do not count toward completing the core meal unless a card says
  otherwise.

Open: exact course bonus values and whether there should be a maximum number of
presented dishes.

## Interaction

Each opponent gets one interaction step before scoring. Reactions are the main
interaction card type.

Current constraint:

- A player may play at most 1 Reaction during each interaction step.

Interaction should create tension without routinely erasing the satisfaction of
presenting a meal.

## Status Cards

The first Status card to test is:

| Card | Type | Effect |
|---|---|---|
| Distraction | Status | No effect. |

Cards may give an opponent a `Distraction`. `Distraction` can be Peeled.

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
