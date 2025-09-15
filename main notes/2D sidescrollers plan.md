## Todos
- Incorporate attack gamics, import attack animation
- Complete the healthbar
- Complete the pathfinding algorithm

## Long term plan
- Rewrite the entire thing, with well-organised code (e.g. classes)
- Complete the first bossfight
- Start working on the background art

## First bossfight design
name: Motophia 

main gamic: laser (more specifically, light beam)

The bossfight will have 3 phases, most __basic attacks__ are universily used while some __skills__ are dedicated for a phase

<u>phase 1</u>
Phase 1 starts in flat ground
- basic attack 1: two straight attack

<u>phase 2</u>


<u>phase 3</u>
(The __double slit experiment__ attack!)
Motophia flies to the top of the screen, stays put (player cannot reach her)
In this phase, she has no healthbar, player needs to surviv for a given amount of time.
Platforms arise, allowing players to jump from one to another to dodge the attack.
The bullet patterns follow double slit experiment pattern, where the waves mark the player (player could dodge by dashing). Marked player loses 2 HP's if getting hit.
Although the waves do not hit the player, the intersection of the two waves do have hitbox and requires accurate movement to dodge. 
The phase goes quicker and quicker until ending
(by math, the intersection is a line)