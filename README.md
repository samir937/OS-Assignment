DESCRIPTION

3. The Cats and Mice Problem A number of cats and mice inhabit a house.
The cats and mice have worked out a deal where the mice can steal pieces
of the cats’ food, so long as the cats never see the mice actually doing so.
If the cats see the mice, then the cats must eat the mice (or else lose face
with all of their cat friends). There are NumBowls catfood dishes,
NumCats cats, and NumMice mice.
The cat and mouse simulation works by creating one thread for each
simulated cat, and one thread for each simulated mouse. Each cat thread
repeatedly sleeps (blocks), and then tries to eat from one of the bowls.
Each mouse thread behaves similarly. Each cat and mouse iterates a fixed
number of times before terminating. Your job is to synchronize the cats
and mice so that the following requirements are satisfied:

R1: Cats and mice should never be eating at the same time.
In other words, if a cat is eating from any bowl, then no mouse should be
eating from any bowl. Similarly, if a mouse is eating from any bowl, then
no cat should be eating from any bowl. This will ensure that the mice don’t
get eaten by the cats.

R2: Only one mouse or one cat may eat from a given bowl at any one time.

R3: Neither cats nor mice should starve.
A cat or mouse that wants to eat should eventually be able to eat. For
example, a synchronization solution that permanently prevents all mice
from eating would be unacceptable. So would a solution in which cats
were always given priority over mice. When we actually test your solution,
each simulated cat and mouse will only eat a finite number of times;
however, even if the simulation were allowed to run forever, neither cats
nor mice should starve.
In addition to the above requirements, which are required for correctness,
your solution should also be efficient , which we define as follows:

R4: Your synchronization mechanism should not impose an upper bound
on the number of bowls that can be in use simultaneously.
In other words, if there are enough creatures, it should be possible for them
to use all of the available bowls simultaneously.
