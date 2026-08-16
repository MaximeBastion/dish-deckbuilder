# Dish Deckbuilder

Dish Deckbuilder is a short 2-player deckbuilding card game about rival chefs
learning recipes, presenting meals, and winning the judge's favor.

The current design target is a fast prototype, not a complete rulebook. The
source of truth should stay small and versioned so card/rule changes are easy
to review.

## Documents

- [Rules](docs/rules.md): current playtest rules and unresolved questions.
- [Playtest feedback](docs/playtest-feedback.md): checked-off feedback,
  unresolved ideas, and future card/rule directions.
- [Design concepts](docs/design-concepts.md): emotional target, design pillars,
  faction identities, and constraints.
- [Balance baseline](docs/balance-baseline.md): provisional value curve,
  effect pricing, and current card outliers.
- [Art direction](docs/art-direction.md): v1 placeholder artwork style and
  prompt template.

## Data

The source of truth for UI imports is intentionally small:

- [cards.csv](data/cards.csv): latest UI-ready card definitions. This includes
  Status cards, because they can be spawned during the game.
- [deck.csv](data/deck.csv): latest UI-ready deck composition. This excludes
  Status cards that are only spawned by effects.

Older card and deck exports are not kept as separate files. Use Git history to
inspect earlier versions.

Game metadata lives separately from UI-ready import data:

- [dish_tags.csv](data/metadata/dish_tags.csv): the six strict dish tags.
- [faction_tag_access.csv](data/metadata/faction_tag_access.csv): which
  factions share each tag.
- [factions.csv](data/metadata/factions.csv): faction flavor and mechanical
  identities.
