# base-unit-trait-diplomatic-missions

The `DiplomaticMissions` unit trait: a unit type with it can carry out diplomatic missions.

A unit type with this trait can enter another player's city to establish an embassy, investigate it, steal a technology, sabotage it or incite a revolt, and can bribe units.

For example: Civ1: Diplomat. Civ2: Diplomat and Spy.

A game declares which of its unit classes have the trait with `UnitTraits` rules from `@civ-clone/core-unit`, and its
rules ask `unit.hasTrait(DiplomaticMissions)`:

```ts
import DiplomaticMissions from '@civ-clone/base-unit-trait-diplomatic-missions/DiplomaticMissions';
import { unitTraits } from '@civ-clone/core-unit/Rules/UnitTraits';

ruleRegistry.register(...unitTraits('my-game:unit/trait', MyUnit, DiplomaticMissions));
```

Part of the unit traits design (civ-clone/web-renderer#1008).
