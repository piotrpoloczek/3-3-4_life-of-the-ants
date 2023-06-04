# 3-3-4_life-of-the-ants

In an ant colony, there are four different castes: workers, soldiers, drones, and there is one queen. The colony area is square (has a width), and the ants live and move within the borders of the colony.

Each ant acts in every timestep, according to a caste-specific rule.

The queen sits in the middle and does not move.
Workers normally make one step in one of the four directions, chosen randomly before each move.
Soldiers "patrol" close to their starting position; this means that in a four-cycle, they step one and turn to the left (towards North, East, South, or West) and then they start the cycle again.
Drones always try to make one step towards the Queen. When they get next to the queen, they have a chance that she is in the mood for mating. In this happy case, they say "HALLELUJAH", and stay there for 10 timesteps. After that they are kicked off in one of the four directions (chosen randomly), to the edge of the colony. If the queen isn't in the mood, drones say ":(", and are kicked away instantly.
The queen’s mating mood is determined using a cooldown timer (set to 50 to 100 timesteps) after a successful mating. When the timer runs out, she gets in the mood again.


What are you going to learn?
Design an application using a class diagram.
Think in the OOP way.
Work a little with algorithms.

# Tasks

### Class diagram
Plan and draw the class diagram for this simulation on draw.io. Create and upload a plan. After finishing the implementation, update the plan to show the end result, and upload it as well.

1. The class diagram plan is added to the repository with the first commit as diagram-plan.png. It displays all classes and methods mentioned in the story. 
2. The final class diagram is uploaded as diagram-final.png. It mirrors the implemented simulation exactly.


### Ant Colony
A colony is created with a width value setting its range, a width by width square. A queen is created at construction time and is positioned at the center of the colony. Colony also has a generateAnts method with three integer arguments that set the number of drones, workers, and soldiers to be created, respectively. It also has an update method which invokes each ants' act method, and a display method which displays the colony "map" on the console.

1. Upon construction, the value of width is set, and a queen is created at the center. 
2. There is an update method that calls act on each ants. 
3. There is a display method that prints all ants in the colony as a width by width map, placing the initials of the ants (Q, W, S, D) at their actual positions. If more then one ants share the same position, only one letter is displayed.