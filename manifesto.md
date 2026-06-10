Originally published at https://viccuad.me/blog/open-source-flight-sim-manifesto.

# The Open Source Flight Sim Manifesto

Sims are niche. One needs time, knowledge, and devices (joysticks, pedals..) to
fully enjoy them.

Sims are a captive market: there's a small and finite amount of customers. Once
you have sold the game to the majority of your potential customers, your
revenue dwindles to a trickle. Developers are left needing to "redo" and sell a
"new" version of the game, or sell the game again and again in installments,
for example by selling new airframes or scenery that take a fraction of the
effort to create but sell for as much as the base game. Or similar approaches
to obtain revenue.

This means the base game doesn't grow in horizontal features. No more ways are
added for players to interact with each other; nor more mission types, radio
comms, radar, SDKs, scenarios, campaigns, mission directors, mision editors,
etc. The community feels that the sim could be perfect with more to do besides
being a "cockpit museum" and still has the itch, so it implements these with
external addons and apps. These provide a clunky UX for newcomers, and the
cycle reinforces.

Sims are complex: lots of modelled systems, historical accuracy, multiplayer,
performance limits, etc. It gets worse with each sim generation: games cost
more to author, which means that less actual interactive features are added.
Games have more fidelity and yet less things to do. The game loop gets smaller.

We know. We are sim players. We have been through this cycle. We are part of
this small tight-knitted sim community, some of us contributing to these
community addons, planes, missions, dynamic campaigns, and more, usually
without the help or even against the wishes of the original sim developers. We
have seen several iterations of the cycle, with old games and new, and we are
tired of it.

It's not 1995 anymore. There's another way.

Sims are a captive market: we cannot break it by creating more customers
(aeronautics is trending down since the 90s), nor by injecting infinite money
into development (like Microsoft funded the old Microsoft Flight Sim family
as a PC demonstrator). But we can opt _off_ the market. Sim game studios are
not big and usually consist of 2 or 3 teams of developers, each with ~10
people. One can find the same amount of developers by just picking one of the
many forums or chat servers the sim community has.

### Our rally

_A sim game & stack from the community for the community, always_.

Complex niche products with strongly defined community and needs are the utmost
perfect fit for successful open source projects. For example in 3D suites
(Blender), databases (PostgreSQL, MariaDB family), music notation (MuseScore),
OS Kernels (Linux), web broswers (Chromium-based, Firefox), game engines
(Godot, Bevy), etc.

We firmly believe that open source is the perfect fit for our specific niche
project: it allows us to skip the perils of a captive market, it works for a
distributed global team and not against it, it scales efficiently with the
team, and it amplifies the simbiosis that can be achieved with all the stack
pieces across different sims and academia.

The sim community is starving for progress, interactivity and scale.
Collaborating asynchronously and openly online is how many successful products
are created nowadays.

### Our way

Successful open source, developed with open doors, requires a "gift culture"
approach in contrast with an "exchange culture" approach. This means ego-less
conversations in the open, and social status earned by what you "give away"
(knowledge, and work) rather to what "you own" (control over knowledge or
projects).

Succesful (open source) projects are those that rally around a lighthouse goal,
but are allowed to grow from "my baby" to "our baby". Like well-raised kids,
these projects are allowed to meet new friends that improve them and make
someone better, eventually becoming autonomous adults, while keeping their
principles intact.

To collaborate and scale the team efficiently, one needs openness. This is a
precondition and non-negotiable. We develop in the open, and communicate
in the open. We ask our questions in public. We are proud of our mistakes
because we strive to grow from them.

We want our stack to be for the community _always_. We do this by ensuring
whatever we create is open source, and the pivotal pieces are licensed under a
copyleft license. This ensures modifications _must be shared back_ to the
community, forever, even if they are adopted by other actors (possibly
competitors) in the space. We put the community first, and we hope this grows
community around us.

When authoring a sim game, there's a lot of byproducts: a Flight Dynamic Model
library, accurate 3d models, aircraft specs, game engine, etc. By open sourcing
these pieces, we ensure they are valuable not only for the specific niche of
sim that we enjoy, but others: the parts are valuable for a combat flight sim,
but also commercial flight sims, RC sims, academia, etc. This attracts
contributors, community, mindset, and knowledge that is seeded and loops back
to us, and is an incredible force multiplier that sims developed behind closed
doors simply cannot tap into.

We evaluate and contribute to existing libraries if possible, this strengthens
the community.

### Our goal

To succeed, we don't build an identity around what we are against, but focus on
what we are for. We state our heading clearly, if not for others, for
ourselves.

We want a social combat flight sim. We enjoy the social interactions of
flying with teammates and against teammates. We find teamwork and
coordination to be exhilarating compared to flying alone. Briefings,
formations, taskings, and knowing that you have a wing man, a flight, and a
squadron or 2 that have your back meanwhile you cover theirs.

We enjoy Advanced Combat Maneuvers and dogfights, and we train and improve each
other, for fun. We want a combat flight sim that enables the community to learn
ACM proficiently, not just as "something that happens organically" in the game.
We want to close the ACM knowledge gap in the sim community and make the sim
community grow.

We also want to play our sim in singleplayer, to practice, develop iteratively,
enhance multiplayer with sound game AI, let the game grow organically into
critical mass, and welcome newcomers at their own speed to the sim community.

We don't chase fidelity for its own sake, we only increase fidelity when it
increases the player's ability to make interesting choices, be it avionic
system choices or multiplayer choices. The player must be able to explain why
something happened and have levers to alter the system: without legibility, the
simulation is just hidden math. The system must be performant to allow for
hundreds of players. The system must be decopuled to allow to run the sim parts
at different speeds for singleplayer or stress tests, and it must be
deterministic to allow for competitive games and to easily reproduce bugs with
a single seed.

We want a sim game & stack without clunkiness. No 3rd party installers, tools
or mods. We want mods that are just first-class plugins to the game. Being open
source, we can legally distribute game content as a whole.

We want accurate 3d models, and specs of existing aircraft. Specs don't change,
nor does historical information. Even if this sim stack is archived in the
future, its models, missions and logic can legally be reused by the community
on new open source games. It also provides a venue for being an actual "plane
museum" for the community that can be studied and reused, moreso than closed
source games.

We want a next-gen sim game. Sim games need a game engine tailored for them.
Usually, sim games develop their own custom game engines. We believe the Bevy
Engine is a right fit for simulations such as ours, just like the Bevy authors
do.

Bevy's Entity-Component-System paradigm is next-gen, gives insane
parallelization (perfect for our perfomance needs), and matches our
extensibility needs. It also makes asynchronous collaboration easier: small,
isolated systems mean fewer conflicts and easier parallel work.

Its next-gen features such as meshlets (aka Nanites) rival commercial open
source engines such as Unreal. Its physics libraries like Avian are well
regarded and fit for a Flight Dynamics Model.

The Bevy engine itself is written in ECS, which means that if one understands
our game code, one understands the game engine, it's all turtles downwards.
This also enables us to tap into existing features from the Bevy community.
Rust is also a subjectively fun language to program on, which draws people
in.

Bevy's shortcomings at the time of writing, like the lack of game editor
or the fast development cycle, only play to our strengths: sims don't need to
create skeletal animations or corridor maps, and the fast development ensures
that forks are costlier than working on one shared stack, respectively.

The Bevy community is also a right fit for collaborating in the open,
therefore we adopt their social customs and code of conduct, as already listed
in this manifesto.

Is it easy? No! Is it doable, and fun? Hell yes!
Several mod teams are already working this way on their respective sims.

If this is not for you, it's ok. If only some parts resonate, I hope we can
collaborate for the benefit of both. If this goal and method of working
resonates with you, join us!
