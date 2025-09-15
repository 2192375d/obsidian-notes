This is a bunch of notes I take for how bullet pattern works and looks like while making a (unresonable) assumption that bullets move at a constant speed with no angle rotation.
In the end this note I will provide an in depth analysis of the following bullet pattern from <u>Touhou  Bunkachou Word Flower Album ~ Shoot the Bullet</u> (Touhou 9.5):

[INSERT THE SOURCE HERE]

(A more in depth source: This is from Yukari's spellcard: __[Border Sign] Borders of Waves and Particles__)

Note that this document is mostly (almost entirely) based on mathematical concepts, so ready your brain up for this!

### Very basic notation & math stuffs
(explain what $\Delta$ means, explain how angles work(quadrant stuffs))

### bullet patterns with fixed angle
Consider a system where the speed of bullets are constant (for the sake of simplicity), and the source of bullet do not change (e.g. always shoot from a fixed starting point).
Then the only two values we can play around about individual bullets are:
	 $t_i$, the time when bullet $i$ is shot
	$\theta_i$, the angle at which bullet $i$ is shot
We can represent all bullets shot by as a set of tuples: $\{(t_1, \theta_1),(t_2, \theta_2),(t_3, \theta_3),...\}$
This set alone is enough to describe the entire bullet pattern, or spellcard, hence, let's call it the BP set: $BP = \{(t_1, \theta_1),(t_2, \theta_2),(t_3, \theta_3),...\}$

The most basic pattern we can have is a single bullet shooting at $\theta$, every $\Delta t$ second.

_example_
Here we shoot every bullet with fixed parameters:
	$\Delta t=0.1$
	$\Delta\theta=0.0$
(This essentially means we shoot a bullet every 0.1s, without changing angle)

Here is the result:
[INSERT THE RESULT HERE]

As a result, we have $BP = \{(0.00,0),(0.1,0),(0.2,0),...\}$

Decreasing $\Delta t$ to different values will create some other interesting results as well:
	$\Delta t$ = 0.5
[INSERT THE RESULT HERE]
	$\Delta t$ = 2.0
[INSERT THE RESULT HERE]

The previous examples should be pretty self explanatory, we shoot a bullet every 0.01s with a fixed direction. 

### bullet patterns with a changing angle
However, shooting at one direction is boring, let's see what's gonna happen if we rotate a bullet by a certain angle in between every shot:
	$\Delta t=0.1$
	$\Delta\theta=60\degree$
[INSERT THE RESULT HERE]


Notice that if we shoot quick enough, it seems like we are shooting multiple lines of bullets instead of just one.

In fact, the example above is similar to the first example at at six directions all at ones.

