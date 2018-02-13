# Equipment

Equipment includes weapons, shields, armor, quest items, and junk carried by characters.

## Weapons

### Melee Weapons

Melee weapons have the following properties.

- Base damage. See [attack damage](combat#attack-damage).
- Damage type. For future reference.
- Handedness. One-handed weapons can be used with shields.
- Traits. Modifiers to weapon stats etc.

When a one-handed weapon is used with a shield, the [Weapon-and-shield](characters#list-of-skills) skill is used in [skirmishes](combat#melee-skirmish-resolution).

| Example weapon | Base | Damage type | Notes |
|-|-:|-|-|
| Dagger | 4 | Blade | One-handed |
| Wooden club | 5 | Impact | One-handed | |
| Shortsword | 6 | Blade | One-handed |
| Flanged mace | 6 | Impact | One-handed |
| War axe, broadsword | 7 | Blade | One-handed |
| Short spear | 7 | Pierce | One-handed. *Reach.* |
| Warhammer | 7/8 | Impact | One-handed, two-handed. *Versatile.* *Penetration.* |
| Flail | 8 | Impact | One-handed. *Curving.* *Cumbersome(1).* |
| Longsword | 8/9 | Blade | One-handed, two-handed. *Versatile.* |
| Estoc | 9 | Pierce | Two-handed. *Penetration.* |
| Claymore, greataxe | 10 | Blade | Two-handed |
| Pike | 11 | Pierce | Two-handed *Reach.* |
| Heavy maul | 12 | Impact | Two-handed. *Penetration.* *Cumbersome(1).* |

#### Melee Weapon Traits

| Trait | Description |
|-|-|
| Versatile | Can be used either one or two-handed, for lower/higher damage stat. |
| Curving | Curve around opponent's shield, negating armor bonus. |
| Reach | TODO: Upside? Downside: malus in narrow spaces. |
| Penetration | Target heavy armor protection is capped at 6. TODO: downside? |
| Cumbersome(X) | Causes -X skill modifier to melee. |

### Ranged Weapons

Ranged weapons have the following properties.

- Base damage.  See [attack damage](combat#attack-damage).
- Damage type. For future reference.
- Usage. Either Marksman or Thrown weapon.
- Traits. Modifiers to weapon stats etc.

| Example weapon | Base | Damage type | Notes |
|-|-:|-|-|-|
| Rock | 4 | Impact | Throwing |
| Throwing knives | 5 | Blade | Throwing |
| Slingshot | 6 | Impact | Throwing |
| Hatchet | 7 | Blade | Throwing. Limited(TODO). |
| Javelin | 9 | Pierce | Throwing. Limited(TODO). |
| Short bow | 7 | Pierce | Marksman |
| Crossbow | 9 | Pierce | Marksman. Simple(5). Slow(1). |
| Longbow | 10 | Pierce | Marksman |
| Heavy crossbow | 11 | Pierce | Marksman. Simple(5). Slow(2). |

#### Ranged Weapon Traits

| Trait | Description |
|-|-|
| Limited(X) | Only X projectiles are available per target per engagement. |
| Simple(X) | While your skill modifier is less than X, you get a `+2` skill modifier up to X. |
| Slow(X) | After firing, the weapon must be reloaded for X rounds as an action. |

## Shields

Shields have a Shield Value property, which has the following functions.

- Increase Evasion against [ranged attacks](combat#ranged-attack-resolution)
- Act as extra armor against all [attack damage](combat#attack-damage)

| Shield type | Value |
|-|-:|
| Buckler | 1 |
| Heater | 2 |
| Tower | 3 |

## Equipment Slots

A character can have at the ready the following weapons.

- Primary melee weapon
- Secondary melee weapon, if both primary and secondary are one-handed
- A shield, if secondary weapon is not used
- A ranged weapon, Throwing or Marksman
- A small sidearm, either melee or ranged

## Wield Limits

A character's [Wield](characters#secondary-stats) secondary stat value indicates how many points worth that charcter can wield weapons.

For melee and ranged weapons, the base damage value is also the wield point cost of that weapon. For shields, the shield value is its cost.

Weapons and shields share the same pool of points.

It is possible to wield more points than your Wield stat up to `3` points, but for each point in excess, a `-1` skill modifier is applied.

For one-handed weapons and ranged weapons, for every `3` unused wield points, gain `+1` skill modifier, up to `+3`.

## Armor

Armor has a Armor Value property, which reduces incoming [damage](combat#attack-damage). Armor also has a Armor Weight Class property, which indicates how restrictive the armor is.

| Example armor | Value | Weight Class |
|-|-:|-|
| Hardened cloth | 1 | Light |
| Hardened leather  | 2 | Light |
| Studded leather | 3 | Light |
| Rawhide | 4 | Medium |
| Light chain | 5 | Medium |
| Scale mail | 6 | Medium |
| Heavy chain | 7 | Heavy |
| Splint mail | 8 | Heavy |
| Plate mail | 9 | Heavy |

### Armor Weight Classes

*Light armor* does not restrict the user.

*Medium armor* has the following restrictions.

- *Physical* skills cap at `TODO`
- *Stealth* skills cap at `TODO`

*Heavy armor* has the following restrictions.

- *Physical* skills cap at `TODO`
- *Stealth* skills cap at `TODO`
- Awareness caps at `TODO`

A skill cap means that the *effective value* of a skill is limited while wearing armor, although the actual skill value is unchanged.

## Durability and Disrepair

In addition to other properties, each piece of equipment (weapons, shields, armor) has a *durability* property.

This property describes the fundamental state of that piece.

At the end of every bout of combat, at the Game Master's discretion, *disrepair* checks are performed for each weapon, shield and armor that was used in that combat.

Usage can be judged as follows.

- A weapon was used in a skirmish or ranged attack
- A shield was used in a skirmish or to deflect ranged attack
- Armor was worn in a skirmish or as target of a ranged attack

A piece of equipment that is in disrepair has the following modifiers.

- Weapons' base damage is reduced by `2`, to a minimum of zero
- Armor's armor value is reduced by `2`, to a minimum of zero

Equipment in disrepair can be restored via a [Field repair](characters#list-of-skills) skill check. See [rest](time-and-space#rest) and [camp](time-and-space#camp).

### Disrepair Resolution

To check whether a piece of equipment becomes in *disrepair*, roll a `d20`. If the roll value is *greater than* the *durability* of the piece of equipment, it becomes in disrepair.

A piece of equipment that fails its disrepair check has its durability value reduced by `1` permanently.

When it reaches zero, that piece of equipment becomes unusable and broken beyond repair.

## Equipment Special Traits

In addition to normal equipment traits, there are also special traits that reflect unusual craftsmanship or magical or divine enhancement.

### Elven Equipment

Elven equipment is uncannily light but no less durable.

- Elven weapons have a wield point cost of one less than their base damage.
- Elven Medium armor counts as Light armor for restrictiveness

### Dwarven Equipment

Dwarven equipment is exceptionally durable.

- For Dwarven equipment, durability checks are performed twice. The equipment becomes in disrepair only, if it fails both checks.

### Gnomish Equipment

Gnomish equipment is ingeniously constructed.

- Gnomish weapons trigger Critical hits on both `19` and `20`
- Gnomish Heavy armor counts as Medium armor for restrictiveness

### Enchanted Equipment

Enchanted equipment is enhanced by magical or divine means.

Enchanted weapons and armor can have skill modifiers or other effects. Some monsters can have resistance to corporeal (unenchanted) attacks.