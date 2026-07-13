# Dish Deckbuilder

Dish Deckbuilder is a short 2-player deckbuilding card game about rival chefs
learning recipes, presenting meals, and winning the judge's favor.

The current design target is a fast prototype, not a complete rulebook. The
source of truth should stay small and versioned so card/rule changes are easy
to review.

## Documents

- [Rules](docs/rules.md): current playtest rules and unresolved questions.
- [Design concepts](docs/design-concepts.md): emotional target, design pillars,
  faction identities, and constraints.
- [Art direction](docs/art-direction.md): v1 placeholder artwork style and
  prompt template.

## Data

- [dish_tags.csv](data/dish_tags.csv): the six strict dish tags.
- [dishes.csv](data/dishes.csv): first-playtest dish cards.
- [faction_tag_access.csv](data/faction_tag_access.csv): which factions share
  each tag.
- [factions.csv](data/factions.csv): faction flavor and mechanical identities.
- [actions.csv](data/actions.csv): first-playtest technique and reaction cards.
- [passives.csv](data/passives.csv): first-playtest long-term support cards.
- [statuses.csv](data/statuses.csv): status cards created by effects.
- [time_cards.csv](data/time_cards.csv): baseline Time cards.
