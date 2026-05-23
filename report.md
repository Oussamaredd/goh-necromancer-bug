# Map version

GoH_RPG_Reforged_v1.45c_prot

## Bug title

Guilds of Hyppos Necromancer spells become unusable after selecting a ground
item, then box-selecting hero with skeletons/minions

## Class

Necromancer

## Reproduction steps

1. Have Necromancer with at least one active skeleton/minion.
2. Have an item on the ground nearby.
3. Click/select the item on the ground.
4. Immediately box-select the Necromancer hero together with other owned units,
   such as skeletons/minions/pet.
5. The hero becomes the main selected unit in the group selection tab.
6. Try using any Necromancer spell.

## Expected result

The Necromancer hero should be able to cast spells normally after being
box-selected with owned units.

## Actual result

The hero is selected and visible as the main unit, but all hero spells become
unusable. Both spell hotkeys and manually clicking the spell icons do not work.
Movement, selection, and other normal unit control still work.

## Important details

The bug only seems to happen after selecting a ground item first, then
box-selecting a group containing the hero and at least one other unit.
It does not seem to happen from normal single hero selection.
It requires more than one selected unit, for example hero + skeleton.
Skeleton/minion existence seems related, because the issue can disappear after
skeletons expire/despawn.

## Ways to fix/reset it in-game

Wait until skeletons/minions expire.
Single-select the hero again.
Box-select only the hero.
Use Tab to cycle selected units until it returns to the hero.
Select another non-item target, then reselect the hero.

## Possible cause

This seems to be a command card / selection priority issue. After selecting a
ground item, then box-selecting Necromancer with skeletons or pet, the game
shows the hero as the main selected unit, but the hero spell command card does
not properly accept orders. The issue may be related to Necromancer summons
being included in the same selection group after item selection.
