[&laquo; Table of Contents](..)

# Combat

Combat is resolved in *combat rounds*, during which each character can do *actions*.

## Combat Rounds

During a combat round, each character acts simultaneously. Different *actions* are grouped into round *phases*, which occur in order.

### Round Actions

During a combat round, a character can take one of the following actions.

- Attack another character (melee or ranged)
- Move to an adjacent [area](time-and-space#local-areas)
- Perform miscellaneous action (e.g. a skill check)

In addition, at the start of the round, a character may draw a weapon, or switch to another weapon as a free action.

### Round Phases

The combat round phases are as follows.

| Phase | Notes |
|-|-|
| Planning | Each player decides what their character tries to do in this round, and informs the Game Master. The Game Master decides actions for each of the NPCs. |
| Ranged combat | Ranged combat, whether using marksman or throwing weapons, is resolved using the [ranged attack resolution](#ranged-attack-resolution) rules. |
| Melee combat | Melee combat is resolved using the [melee skirmish resolution](#melee-skirmish-resolution) rules. |
| Magic and divinity | Magical spells and divine prayers are resolved. |
| Miscellaneous actions | Other actions, such as climbing a wall, are resolved. A character being attacked while performing such action has [disadvantage](characters#advantage-and-disadvantage) in both that action and evading the attack. |
| End phase | End-of-round effects, such as bleeding, are applied. |

All actions in a phase are resolved simultaneously, i.e. if two characters fire arrows at each other, and the first arrow kills its target, the second attack is still resolved normally.

Movement occurs simultaneously with other phases, and depends on the actions of characters, at the discretion of the Game Master.

### Skirmish Assignment

Characters who share the same [area](time-and-space#local-areas), or move into it, can engage in melee combat.

Generally, one character can opt to fight a single opponent. However, multiple characters are allowed to target a single character, when there are no unengaged targets nearby. In such a case, a single *skirmish* will have multiple participants on one side (other effects may allow there to be multiple characters on both sides).

The process of determining which character is in which skirmish is called assignment, and depends on the relative locations of the various characters and the Game Master's discretion.

The particular situation allowing, player characters should generally be allowed to pick their assignments first, with extra NPCs taking their picks after.

### Ranged Targeting

Designating targets for ranged attacks is not an exact science, but the following guidelines apply.

Generally, [Marksman weapons](equipment#ranged-weapons) can target opponents in your own [area](time-and-space#local-areas) and adjacent areas that have line of sight, as long as you are not [engaged](#engagement-and-disengaging) in a melee skirmish.

[Thrown weapons](equipment#ranged-weapons) can target opponents in your own [area](time-and-space#local-areas), even if you are [engaged](#engagement-and-disengaging).

However, at the Game Master's discretion, other targets can be designated. For example, a Marksman weapon could be used to target an opponent several areas away, if those areas represent locations which are not physically far separated, and provide line of sight. A thrown weapon could also target an area adjacent to your area, for example when there is an elevation difference between the areas.

## Combat Resolution Rules

### Ranged Attack Resolution

A ranged attack is resolved as follows.

1. The attacker rolls `d20` and adds the skill modifier of the [*Ranged*](characters#list-of-skills) skill they are using.
1. The defender rolls `d20` and adds the [Evasion](characters#list-of-skills) skill modifier and [shield](#shields) modifier, if using a shield.
1. If the attack roll is *higher* than the defense roll, the attack hits. Otherwise, the attack misses, and the resolution ends.
1. Determine the attack hit location using [hit location resolution](#hit-location).
1. Calculate [attack damage](#attack-damage) based on roll difference.
1. Calculate and apply pain using [pain resolution](#pain-resolution) and attack damage.
1. Determine and apply critical wounds using [wounds resolution](#critical-wounds-resolution) and attack damage.

#### Ranged Attacks Into Skirmishes

When making a ranged attack against a character who is engaged in melee skirmish with another character, there is a risk that the projectile hits the other character.

If the attack misses its target, perform ranged attack resolution against the other character using the natural roll value. If there are multiple, the Game Master chooses one. If the attack still misses, the resolution ends.

### Melee Skirmish Resolution

A melee skirmish with one or more characters on either side is resolved as follows.

1. Each character rolls `d20` and adds the skill modifier of the [*Melee*](characters#list-of-skills) skill they are using.
1. The side with the highest roll value wins the skirmish. The character who rolled this value will deal damage. The character with the lowest natural roll on the losing side will sustain damage. If each side's results are equal, the side with the highest natural roll wins. If it's still a tie, no damage is dealt, and the resolution ends.
1. Determine the attack hit location using [hit location resolution](#hit-location).
1. Calculate [attack damage](#attack-damage) based on roll difference of the sides' rolls.
1. Calculate and apply pain using [pain resolution](#pain-resolution) and attack damage.
1. Determine and apply critical wounds using [wounds resolution](#critical-wounds-resolution) and attack damage.

### Critical Hit

In a skirmish, if a character rolls a natural `20`, it is a *critical hit*.

A critical hit wins a skirmish against any non-critical hit and always has a [damage multiplier](#attack-damage) of at least `2`.

If characters on both sides of a skirmish roll critical hits, resolve the skirmish as if neither had.

### Hit Location

Roll `d4` and refer to the table below.

| Roll | Hit Location |
|-|-|
| 1 | Roll `d4` again: 1&ndash;2 Head, 3&ndash;4 Torso |
| 2 | Torso |
| 3 | Arms |
| 4 | Legs |

### Attack Damage

Let `R1` be the (modified) attack roll, `R2` be the (modified) defense roll, `B` be the attacker's base weapon damage, `AV` be the defender's armor value, and `SV` be the defender's shield value, if any. Let `R1` > `R2`.

Then, the attack damage is calculated as `M × B - AV - SV` where damage multiplier `M` is read from the table below, based on the roll difference `R1 - R2`.

| Difference | Multiplier |
|-:|-:|
| 1 &ndash; 5 | 1 |
| 6 &ndash; 10 | 2 |
| 11+ | 3 |

> **Example**
>
> The attack roll is 15. The defense roll is 4. The attacker's base weapon damage is 7, while the defender's armor value is 5. Hence the roll difference is 15 - 4 = 11, the damage multiplier is 3 and attack damage is 3 × 7 - 5 = 16.

### Pain Resolution

Let `D` be the damage dealt and `F` be the target character's [Fortitude](#characters#secondary-stats) secondary stat value.

The pain sustained by the target character is `⌈D / F⌉`.

> **Example**
>
> The damage dealt is 6 and the target character's Fortitude is 5. Hence the pain sustained is ⌈6 / 5⌉ = 2. If that character's Fortitude was instead 6, they would only suffer one point of pain.

### Critical Wounds Resolution

Let `D` be the damage dealt, `L` be the hit location and `C` be the target character's [Critical](characters#secondary-stats) secondary stat value.

If `D` is *equal or greater than* `C`, but less than `3C`, the target character suffers a *critical wound* based on the hit location `L` from the table below.

If `D` is *equal or greater than* `3C`, the target character instead suffers a *supercritical wound* based on the hit location `L` from the table below.

| Hit Location | Critical Wound | Supercritical Wound |
|-|-|-|
| Head | Skull Fracture, Bleeding | Severed Head |
| Torso | Bleeding | Crushed Torso |
| Arms | Fractured Arm | Severed Arm, Bleeding |
| Legs | Fractured Leg | Severed Leg, Bleeding |

If a character has a critical wound in a given hit location, they cannot sustain another critical wound to that location, but can still suffer a supercritical wound to that hit location.

If a character has a supercritical wound in a given hit location, they cannot sustain another supercritical wound to that hit location.

See also [critical wound effects](#critical-wound-effects).

## Critical Wound Effects

| Critical Wound | Effect |
|-|-|
| Skull Fracture | [Incapacitation](#incapacitation), Cognition and Willpower based skill checks, including spells and prayers, have [disadvantage](characters/#advantage-and-disadvantage). |
| Fractured Arm | *Melee*, *Ranged*, *Physical* and *Manual* skill checks and spells and prayers have [disadvantage](characters/#advantage-and-disadvantage). |
| Fractured Leg | *Melee*, *Ranged*, *Physical* and Evasion skill checks have [disadvantage](characters/#advantage-and-disadvantage). Traveling times are *one and half* times as long. |
| Bleeding | Character suffers 1 Fatigue at each end phase until at zero Stamina. See also [incapacitation](#incapacitation). |
| Incineration | Character suffers 2 Pain at each end phase until at zero Stamina, or until the character takes a full round to put out the fire. See also [incapacitation](#incapacitation). |
| Hindering | Character cannot move for one round. |
| Frostburn | A character cannot regain Stamina through resting while suffering from frostburn. |
| Corrosion | Armor becomes in disrepair immediately. |
| Poisoning | Character has `-2` [Critical](characters#secondary-stats) and [Fortitude](characters#secondary-stats) secondary stat values. |

Critical wounds can be treated using the [Trauma treatment](characters#list-of-skills) skill. See [trauma treatment resolution](#trauma-treatment-resolution).

| Supercritical Wound | Effect |
|-|-|
| Severed Head | Instant death. |
| Crushed Torso | Instant death. |
| Severed Arm | [Incapacitation](#incapacitation), permanent Fractured Arm effects. |
| Severed Leg | [Incapacitation](#incapacitation), permanent Fractured Leg effects. |
| Incineration | Instant death, body burned to cinder. |
| Forstburn | Instant death, body shattered. |
| Corrosion | Armor is destroyed, weapons and shields become in disrepair. |
| Poisoning | [Incapacitation](#incapacitation), become dying. Medical skill checks cannot be used on character while dying. |

Supercritical wounds are beyond the skills of adventurers to treat, but [monasteries](environment#monasteries) may offer restoration and even resurrection services.

## Shields

As the combat resolution rules specify, shields have two effects:

- Modify ranged attack hit chance
- Act as additional armor against all damage

## Engagement and Disengaging

A character who is in a melee skirmish with another character is *engaged* in combat with that character.

This condition persists, until either that character or all opposing characters in the skirmish are dead or incapacitated, or until that character or all opposing characters *disengage*.

Characters that are engaged cannot move away from their current [area](time-and-space#local-areas).

Disengagement is performed by participating in a melee skirmish, except instead of using a *Melee* or *Ranged* (Throwing) skill, the Evasion skill is used. If you win the skirmish, instead of doing damage, you will have successfully disengaged.

## Incapacitation

A character whose [Stamina](characters#secondary-stats) is equal or less than zero (i.e. their [Fatigue](characters#secondary-stats) is equal or greater than their [Endurance](characters#secondary-stats)), or who suffers a critical wound that causes Incapacitation, is *incapacitated*.

Such a character is unconscious, but alive. An incapacitated character is *stable*, unless they are bleeding.

A character regains consciousness when their Stamina is raised to one or more. A stable character regains one point of Stamina per [watch](time-and-space#watches).

An incapacitated character who is also bleeding is *dying*. No amount of Fatigue by itself will cause a character to die. Note that a character can be dying even with positive Stamina.

## Dying and Death

A dying character must roll a *death check* each [watch](time-and-space#watches) for three watches, or until stabilized. If a character fails all three death checks, they die. If a character is stabilized, their death check failure counter is reset.

A death check is a roll with Target Difficulty of `15` and is modified by current Stamina.

A dying character can be stabilized using the [Stabilization](characters#list-of-skills) skill by another character. See [rest](#time-and-space#rest).

[Monasteries](environment#monasteries) may offer restoration and even resurrection services.

A character's body, unless magically or otherwise treated, generally stays for two days before becoming unresurrectable.

> **Example**
>
> A character takes a knock in the head and becomes incapacitated and bleeding, with 4 current Stamina. As such, they are dying, and must make a death check each watch. The character rolls 10 + 4 = 14, failing their first check.

## Stabilization and Trauma Treatment

### Stabilization Resolution

Bleeding can be staunched using the [Stabilization](characters#list-of-skills) skill during a [rest](time-and-space#rest).

The target difficulty for treating a bleeding wound is `15`.

Once a Stabilization skill check succeeds, the bleeding wound is completely healed at the end of the rest.

### Trauma Treatment Resolution

Critical wounds (not supercritical wounds) can be healed using the [Trauma treatment](characters#list-of-skills) skill during a [camp](time-and-space#camp).

The target difficulty for treating a single critical wound is `15`.

Once a Trauma treatment skill check succeeds, the critical wound is completely healed at the end of the camp.

## Damage Types

| Type | Critical Effects |
|-|-|
| Blade | *Physical.* [Locational](#critical-wounds-resolution). |
| Impact | *Physical.* [Locational](#critical-wounds-resolution). |
| Pierce | *Physical.* [Locational](#critical-wounds-resolution). |
| Fire | *Elemental.* [Incineration](#critical-wound-effects). |
| Frost | *Elemental.* [Hindering](#critical-wound-effects), [Frostburn](#critical-wound-effects). |
| Acid | *Elemental.* [Corrosion](#critical-wound-effects). |
| Poison | *Elemental.* [Poisoning](#critical-wound-effects). |

## Damage Resistance

A character who is *resistant* to a type of damage has the attack damage multiplier of attacks made using that damage type reduced by one, to a minimum of zero.

Attacks that do not use damage multiplier, such as some magical attacks, have their damage reduced by half.

Characters who are *immune* to a damage type take no damage at all from attacks of that damage type.

## Constructs

*Constructs* are any non-living characters or structures. Constructs do not have Endurance or Fortitude, but instead have a *Structure* stat and have an intrinsic *Armor Value* and may have a durability value.

Constructs cannot become [incapacitated](#incapacitation) or [bleeding](#critical-wound-effects) and are immune to [poison](#damage-types).

When a construct with armor value `AV` suffers `D` points of damage, its structure is reduced by `D - AV` (minimum zero) points. When a construct is reduced to zero structure, it is destroyed.

A Destroyed construct may still be repaired, unless its durability has been reduced to zero.

Immobile constructs (walls, doors, chests, etc.) suffer the maximum damage of any attack. Attacking immobile constructs creates a [disturbance](charaters#disturbance).

> **Example**
>
> A wooden door blocks the path. The door is a construct with 100 structure and 5 AV. A character wielding a Greataxe (base damage 10) will cause 25 points (3 × 10 - 5) of damage per attack, and will destroy the door, removing the obstacle, in 4 rounds. A character attacking the door with a dagger would require 15 turns.

[&laquo; Table of Contents](..)

[&raquo; Sorcery and Divinity](sorcery-and-divinity)
