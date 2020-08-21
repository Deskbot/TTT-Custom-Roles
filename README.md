# TTT-Custom-Roles
Adds a bunch of new roles to the Garry's Mod TTT game mode.

**Steam workshop page:** https://steamcommunity.com/sharedfiles/filedetails/?id=1215502383

## Differences to the [original by NoxxFlame](https://github.com/NoxxFlame/TTT-Custom-Roles).

- Fixes a bug that sometimes causes a searched player to not have their alignment shown in the scoreboard table.
- Gives Assassins and Vampires access to custom traitor shop items.
- The number of starting credits for all traitor roles and zombies are independently configurable with these commands: `ttt_credits_starting`, `ttt_assassin_credits_starting`, `ttt_hypnotist_credits_starting`, `ttt_vampire_credits_starting`, `ttt_zombie_credits_starting`.
- Fixes bugs that cause the chance of many roles to be wrong. They should now operate how you would expect.
- All players are notified in the chat when config settings are changed that relate to roles and game rules. Notably this includes role likelihoods and conditions for roles to be enabled.
- A summary of the role settings is printed into the chat at the start of each round.
- Gameplay configuration is saved between map reloads and play sessions.
- Prevents a player's role in the previous round from affecting the likelihood of what role they get in the next round.
- Improves the randomness by assigning players their role in a random order.
- Config defaults have been altered. Notably `ttt_detective_search_only` defaults to `0`.
- Fixes a bug that causes detectives to not spawn with claws when turned into a Zombie.
- Adds option `ttt_independent_warning` (Default: 1). At the start of the round, if there is a Jester, Swapper, or Killer, all players are warned that there is an "independent player".
- Fixes a bug that caused the sprint re-generation rate of players with special traitor roles to be less than for a vanilla traitor.
- Fixes a bug that causes zombies to not lose their claws when forced into a different role.
- Removes `ttt_sherlock_mode` and treats the game as though it is always true. i.e. players can inspect corpses to find the player's role. This is completely separate from `ttt_detective_search_only`, which still exists.
- Removes `ttt_limit_spectator_voice` and treats it as always true. i.e. spectators can't use in-game voice.
- Removes a special case for a certain random Steam user in role selection.

### Special Thanks:

- [NoxxFlame](https://github.com/NoxxFlame) for developing the [original TTT-Custom-Roles mod](https://github.com/NoxxFlame/TTT-Custom-Roles).
- [Jenssons](https://steamcommunity.com/profiles/76561198044525091) for the 'Town of Terror' mod which was the inspiration for this mod.
- [Bodysnatch Thunderpants](https://steamcommunity.com/id/gamerh) for the 'Better Equipment Menu' mod.
- [Milky](https://steamcommunity.com/profiles/76561198094798859) for the code used to create the pile of bones after the Vampire eats a body taken from the 'TTT Traitor Weapon Evolve' mod.
- [Wizard Cat](https://steamcommunity.com/id/Vadiminator) for the code used for the Hypnotist's brain washing device taken from the 'Defibrillator for TTT' mod.
- [Fresh Garry](https://steamcommunity.com/id/Fresh_Garry) for the 'TTT Sprint' mod which was used as the base for this mods sprinting mechanics.
- Kommandos, Lix3, FunCheetah, B1andy413, Cooliew, The_Samarox, Arack12 and Aspirin for helping me test.

### Compatibility Issues

Some weapon mods cause the team shops to bug out and only display one item (The one that is causing the issue). Here are some mods with known compatibility issues:

- [TTT Gravity Changer](https://steamcommunity.com/sharedfiles/filedetails/?id=1618719637)
- [Time Manipulator](https://steamcommunity.com/sharedfiles/filedetails/?id=1318271171)
- [TTT Blue Firework](https://steamcommunity.com/sharedfiles/filedetails/?id=1421303070)
- [TTT Scarface Jihad Bomb](https://steamcommunity.com/sharedfiles/filedetails/?id=917717470)

# Gameplay Instructions

## Innocent Team:
Goal: Kill all members of the traitor team

**Innocent**
- A standard player. Has no special abilities

**Detective**
- All other players are notified of the Detectives at the start of the round
- Can search bodies of dead players
     - Reveals the role, what killed them, who they last saw and other useful information to all players
     - If other players try to search a body it will instead alert Detectives of the body’s location (Optional)
- Has access to a shop
     - Spawns with one credit
     - Gains a credit whenever a member of the traitor team is killed

**Glitch**
- Has a chance to spawn instead of an Innocent
- Appears as a Traitor (or Zombie) to members of the traitor team
- Prevents members of the traitor team from using team text and voice chat

**Mercenary**
- Has a chance to spawn instead of an Innocent
- Has access to a shop
     - Spawns with one credit
     - Can buy any naturally occurring weapon or items available to both Detectives and Traitors

**Phantom**
- Has a chance to spawn instead of an Innocent
- Haunts attackers on death
     - Haunted players leave a smoke trail behind them
     - Killing the haunted player will revive the Phantom on 50 health
     - Detectives are notified when the Phantom is killed or revived

## Traitor Team:
Goal: Kill all members of the innocent team

**Traitor**
- Notified of team members and Jesters at the start of the round
- Has access to a shop
     - Spawns with one credit
     - Gains a credit whenever enough innocent team members are killed

**Assassin**
- Has a chance to spawn instead of a Traitor
- Notified of team members and Jesters at the start of the round
- Given a random target at the start of the round
     - Deals double damage to the target and half damage to all other players
     - When the target dies a new target is selected
     - Detectives will always be the final targets
     - Killing the wrong player will fail the contract and the Assassin will deal half damage to all players
- Has access to a basic shop
     - Spawns with no credits
     - Gains a credit whenever enough innocent team members are killed

**Hypnotist**
- Has a chance to spawn instead of a Traitor
- Notified of team members and Jesters at the start of the round
- Spawns with a brain washing device
     - When used on a dead body it will revive them at full health
     - Changes the role of the revived player to Traitor
     - Cannot be used on Jesters and Swappers
- Has access to a basic shop
     - Spawns with no credits
     - Gains a credit whenever enough innocent team members are killed

**Vampire**
- Has a chance to spawn instead of a Traitor
- Notified of team members and Jesters at the start of the round
- Spawns with fangs
     - When used on a dead body it will destroy the body and heal 50 health up to a maximum of 125 health
     - Right click will grant short term speed and invisibility on a cooldown
- Has access to a basic shop
     - Spawns with no credits
     - Gains a credit whenever enough innocent team members are killed

**Zombie**
- Has a chance to spawn instead of all Traitors
- Notified of team members and Jesters at the start of the round
- Spawns with claws
     - Deals 50 damage to members of the innocent team
     - If used to kill a player they will re-spawn as a zombie
- Deals half damage will all standard weapons
- Has access to a perk shop
     - Spawns with no credits
     - Gains a credit upon infecting another player with the claws

## Independent Players:

**Jester (Goal: Get killed by another player)**
- Has a chance to spawn instead of an Innocent
- Deals no damage to other players or props
- Takes no environmental damage (e.g. fire, fall, explosion...)
- Can message members of the traitor team using team text and voice chat but will not recieve replies

**Swapper (Goal: Get killed by another player and then fulfil their old goal)**

- Has a chance to spawn instead of an Innocent
- Appears as a Jester to members of the traitor team
- Deals no damage to other players or props
- Takes no environmental damage (e.g. fire, fall, explosion...)
- Can message members of the traitor team using team text and voice chat but will not recieve replies
- When killed by another player the Swapper swaps roles with their attacker
     ◦ The attacker will die instead and the Swapper will respawn with the newly swapped role
     ◦ If a Detective searches the body of the attacker they will look like a Swapper

**Killer (Goal: Be the last player standing)**

- Has a chance to spawn instead of an Innocent
- Spawns with 150 health and maximum health
- Traitors are notified if there is a Killer
- Has access to a shop
     - Spawns with one credit
     - Can buy any naturally occurring weapon or items available to both Detectives and Traitors

# Server config options

Add the following to your server config:

```cpp
// ----------------------------------------
// Custom Role Settings
// Values shown are defaults
// ----------------------------------------

ttt_glitch_enabled    1 // Whether the Glitch should spawn or not
ttt_mercenary_enabled 1 // Whether the Mercenary should spawn or not
ttt_phantom_enabled   0 // Whether the Phantom should spawn or not
ttt_assassin_enabled  1 // Whether the Assassin should spawn or not
ttt_hypnotist_enabled 0 // Whether the Hypnotist should spawn or not
ttt_vampire_enabled   1 // Whether the Vampire should spawn or not
ttt_zombie_enabled    1 // Whether Zombies should spawn or not
ttt_jester_enabled    1 // Whether the Jester should spawn or not
ttt_swapper_enabled   1 // Whether the Swapper should spawn or not
ttt_killer_enabled    0 // Whether the Swapper should spawn or not

// Role Spawn Chances
ttt_glitch_chance    0.25 // Chance of the Glitch spawning in a round
ttt_mercenary_chance 0.1  // Chance of the Mercenary spawning in a round
ttt_phantom_chance   0    // Chance of the Phantom spawning in a round
ttt_assassin_chance  0.1  // Chance of the Assassin spawning in a round
ttt_hypnotist_chance 1    // Chance of the Hypnotist spawning in a round
ttt_vampire_chance   0.1  // Chance of the Vampire spawning in a round
ttt_zombie_chance    0.05 // Chance of Zombies replacing traitors in a round
ttt_jester_chance    0.05 // Chance of the Jester spawning in a round
ttt_swapper_chance   0.05 // Chance of the Swapper spawning in a round
ttt_killer_chance    1    // Chance of the Killer spawning in a round

// Role Spawn Requirements
ttt_glitch_required_innos       6 // Number of innocents for the Glitch to spawn
ttt_mercenary_required_innos    6 // Number of innocents for the Mercenary to spawn
ttt_phantom_required_innos      2 // Number of innocents for the Phantom to spawn
ttt_assassin_required_traitors  2 // Number of traitors for the Assassin to spawn
ttt_hypnotist_required_traitors 2 // Number of traitors for the Hypnotist to spawn
ttt_vampire_required_traitors   2 // Number of traitors for the Vampire to spawn
ttt_jester_required_innos       4 // Number of innocents for the Jester to spawn
ttt_swapper_required_innos      4 // Number of innocents for the Swapper to spawn
ttt_killer_required_innos       6 // Number of innocents for the Killer to spawn

// Karma
ttt_karma_jesterkill_penalty 50   // Karma penalty for killing the Jester or Swapper
ttt_karma_jester_ratio        0.5 // Ratio of damage to Jesters, to be taken from karma

// Other
ttt_zombie_pct              0.2  // Percentage of total players that will be a Zombie
ttt_detective_search_only   0    // Whether only detectives can search bodies or not
ttt_assassin_credits_starting  2 // Number of credits the assassin starts with
ttt_hypnotist_credits_starting 2 // Number of credits the hypnotist starts with
ttt_vampire_credits_starting   2 // Number of credits the vampire starts with
ttt_zombie_credits_starting    2 // Number of credits the zombie starts with
ttt_mer_credits_starting    1    // Number of credits the Mercenary starts with
ttt_kil_credits_starting    2    // Number of credits the Killer starts with
ttt_independent_warning     0    // At the start of the round, if there is a Jester, Swapper, or Killer, all players are warned that there is an "independent player".
```