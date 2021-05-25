## Upgrade your project

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Upgrade your project with more drums to upgrade to and more backdrops as you play more amazing venues. </div>
<div>
![](images/image.png){:width="300px"}
</div>
</div>

There are lots more drum costumes to choose from to add more upgrades to your project.

--- task ---
To add another drum to upgrade to, look back at the earlier steps of the project. You will need to:

+ Add a new drum sprite with two costumes. Copy the scripts from another drum sprite and change the costume and sound. Change the message that makes the drum appear to the message broadcast by the previous drum. Change the number of beats that the new drum gives when you click on it.
+ Add a new Get button sprite for the new drum. Change the costume including the cost of the new drum. Change the number of beats you must have to get this drum in the `if`{:class="block3events"} condition and the negative number of beats you `change by`{:class="block3variables"} when you get this drum. Change the message that gets broadcast to the name of the new drum.
+ Add a new backdrop and add a script to the Stage to switch to that backdrop when the messgage for this drum is receieved.

--- /task ---

--- task ---
You might find that your drums need to be in a new position on a different backdrop. 

Add script starting with `when backdrop changes to`{:class="block3events"} to each drum sprite with a `go to`{:class="block3motion"} block to make them change position.

You will also need to set their starting position `when flag clicked`{:class="block3events"}.

--- /task ---

--- collapse ---

---
title: Completed project
---

You can view the [completed project here](https://scratch.mit.edu/projects/485673032/){:target="_blank"}.

--- /collapse ---

--- save ---