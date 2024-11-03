# Programming the Farming Drone (Report)

## Introduction

In "The Farmer was Replaced," players immerse themselves in a pixel-art world that blends farming mechanics with combat and exploration. As the farmer, you must gather crops, craft items, and fend off hostile creatures that threaten your land. 

The gameplay involves managing resources effectively, making strategic decisions about what to plant and when to harvest, while also preparing for battles against invading forces. You'll encounter various environments, each with unique challenges and secrets to discover. 

As you progress, you'll unlock new abilities and upgrades that enhance your combat skills and farming efficiency. The overarching goal is not only to protect your farm but also to uncover the mystery behind the invasion, leading to a deeper narrative experience. Balancing farming and fighting is key to reclaiming your home and restoring peace to your once tranquil life.

## Objective.

The objective is to navigate through various levels, overcoming challenges and enemies while gathering resources, upgrading abilities, and uncovering the story behind the invasion. Players must use strategy and skill to survive and ultimately reclaim their farm from the encroaching chaos.

# Table of Contents.

# Table of Contents
-[Code Snippets and Explanation](#code-snippets-and-explanation)

-[Challenges and Learnings](#challenges-and-learnings)

-[References](#references)



## Step 1 : Farming on 1 Tile

**Code**

```python
whileTrue:
    if can_harvest():
        harvest()
```

**Explanation**

The code runs an infinite number of times and harvest the grass with the if condition.


**Demo**

Video Demo :

https://github.com/user-attachments/assets/372f3625-32e7-4340-b8d0-346e2fa0df69



**Notes**

- Using the code above I was able to get enough hay to unlock the tile.

- These features were unlocked too : variables and functions.





## Step 2 : Planting a Bush

**Code**

```python

whileTrue:
    if can_harvest():
        harvest()
    else:
        plant(Entities.Bush)
        do_a_flip()
```

**Explanation**

The code makes the drone go one square at a time harvests the grass with the if condition and plants a bush after harvesting the grass.

**Demo**

Video Demo :

https://github.com/user-attachments/assets/b4340c24-da38-4a15-a38b-9827e2187a85



**Notes**

- Using the code above I was able to get enough wood to unlock the speed and operators.




## Step 3 : Farming on 3x3 Tile

**Code**

```python
while True:
	for x in range(get_world_size()):
		move(East)
		trade(Items.Carrot_Seed)
		for y in range(get_world_size()):
			if num_items(Item.Carrot):
				if can_harvest():
					harvest()
                    till()
				    plant(Entities.Carrots)
				move(South)
            else:
                retuen
```

**Explanation**
This code continuously moves across a 3x3 grid, trading for carrot seeds, planting and harvesting carrots if possible, and stopping if no carrots are available.

**Demo**

Video Demo :

https://github.com/user-attachments/assets/6777c37c-7c9b-43fe-87aa-b7014c1be5d3


**Notes**

- Using the code above I was able to harvest wood and hay simultaneously.







## Step 4 : Planting Grass

**Code**

```python
while True:
	for i in range(get_world_size()):
def planting():

            elif num_items(Items.Hay) < HayCap:
                if get_ground_type()== Grounds.Soil:
                    till()
                plant(Entities.Grass)
		
```

**Explanation**

This code makes the drone to plant and harvest grass across the grid, applying minimal water each time, until the required amount of hay is collected.

**Demo**

Video Demo :

https://github.com/user-attachments/assets/6777c37c-7c9b-43fe-87aa-b7014c1be5d3


**Notes**

- Using the code above I was able to get huge amount hay to unlock expensive functions and upgrade speed and I could even expand the field.




## Step 5 : Planting Trees

**Code**

```python
while True:
	for i in range(get_world_size()):

def planting():
   elif num_items(Items.Wood) < WoodCap:
                if (x % 2 == 0 and y % 2 == 1) or (x % 2 == 1 and y % 2 == 0):
                    plant(Entities.Tree)
                else:
                    if get_ground_type()== Grounds.Soil:
                        till()
                plant(Entities.Bush)
```

**Explanation**

This code plants trees and bushes in a checkerboard pattern across the grid, watering each cell, and harvesting as needed until the required amount of wood is collected.

**Demo**

Video Demo :

https://github.com/user-attachments/assets/6777c37c-7c9b-43fe-87aa-b7014c1be5d3


**Notes**

- Using the code above I was able to get five woods at time which unlocked a lot of features quickly and saved a lot of time.



## Step 6 : Planting Carrots

**Code**

```python
while True:
	for i in range(get_world_size()):
def planting():
	
	 elif num_items(Items.Carrot) < CarrotCap:
                if get_ground_type() == Grounds.Turf:
                    till()
                plant(Entities.Carrots)
		
```

**Explanation**


This code makes the drone to plant, water, and harvest carrots across the grid, trading for carrot seeds as needed and planting other crops if seeds are insufficient, until the required number of carrots is collected.

**Demo**

Video Demo :

https://github.com/user-attachments/assets/6777c37c-7c9b-43fe-87aa-b7014c1be5d3


**Notes**

- Using the code above I was able to get enough carrots to unlock other vegetables and plants.




## Step 7 : Planting Pumpkin

**Code**

```python
while True:
	for i in range(get_world_size()):
def planting():
	 elif num_items(Items.Pumpkin) < PumpkinCap:
                if get_ground_type() == Grounds.Turf:
                    till()
                plant(Entities.Pumpkin)
							
							
					
		
```

**Explanation**



This code makes the drone to plant and harvest pumpkins by traversing the grid, checking and recording empty cells, trading for seeds as needed, replanting at unoccupied positions, and iteratively revisiting and replanting until the required number of pumpkins is collected.

**Demo**

Video Demo :

https://github.com/user-attachments/assets/6777c37c-7c9b-43fe-87aa-b7014c1be5d3


**Notes**

- Using the code above I was able to get enough pumpkin to unlock advanced and useful data types which made the coding much simpler and shorter.




## Step 8 : Planting Sunflower

**Code**

```python
while True:
	for i in range(get_world_size()):
def planting():
    #sunflower
            if num_items(Items.Power) < PowerCap:
                if get_ground_type() == Grounds.Turf:
                    till()
                plant(Entities.Sunflower)
                PedalList.append(measure())
			
				
				
				
```

**Explanation**


This code guides the drone to plant, water, and harvest sunflowers across the grid, trading for seeds if needed, and later measures, locates, and harvests sunflowers with the maximum petals until the required power level is achieved.

**Demo**

Video Demo :

https://github.com/user-attachments/assets/61c765c4-a2e7-4268-8e72-292a0dab183b



**Notes**

- Using the code above I was able to get enough sunflower to unlock lower level of the games like maze, treasure and fertilizers.



## Step 9 : Treasure Harvesting

**Code**

```python
while True:
	for i in range(get_world_size()):
def SolveMaze():
	direction = North
	while get_entity_type() != Entities.Treasure:
		direction = TurnLeft(direction)
		if move(direction) == False:
			direction = TurnRight(direction)
		if move(direction) == False:
			direction = TurnRight(direction)
		else:
			direction = TurnLeft(direction)
			if move (direction) == False:
				direction = TurnRight(direction)
	harvest()
def TurnRight(direction):
	if direction == North:
		return East
	if direction == East:
		return South
	if direction == South:
		return West
	if direction == West:
		return North
def TurnLeft(direction):
	if direction == North:
		return West 
	if direction == West:
		return South
	if direction == South:
		return East
	if direction == East:
		return North
	
```

**Explanation**
This code defines a loop where an entity plants bushes, navigates to treasures while using fertilizer, and trades for items, repeating the process indefinitely.


**Demo**

Video Demo :

https://github.com/user-attachments/assets/d83616c3-8673-423f-b76e-23b864f9fabb


**Notes**

- Using the code above I was able to get Treasure to unlock cactus.










# Challenges and Learnings

## Challenges

In the Farmer is Replaced Python game, several challenges made gameplay both engaging and complex:

**1.Efficient Resource Management**: Balancing resources like seeds and water while meeting crop quotas requires careful planning and prioritization. Running out of seeds or water at the wrong time can disrupt the workflow and require backtracking to collect or trade for more.

**2.Grid Navigation**: Programming the drone to navigate the grid efficiently, especially with constraints on movement direction and positioning, is a challenge. Looping across the grid without missing cells or revisiting already-harvested spots requires precise logic.

**3.Conditional Logic for Mixed Actions**: Many tasks involve multi-step sequences (e.g., planting, watering, harvesting) with conditions, such as only planting specific crops in designated soil types or swapping to a fallback crop if resources are insufficient. Coding these steps with minimal redundancy demands effective use of loops and conditionals.

**4.Avoiding Infinite Loops and Recursion**: Some tasks, like replanting when resources are low, can lead to infinite loops if not handled carefully. Implementing checks to break out of loops and prevent unintended recursive calls is crucial.

**5.Prioritizing High-Yield Harvests**: When faced with limited resources, choosing which crops to prioritize (such as high-yield crops like pumpkins) adds strategic depth. Measuring factors like yield and growth time becomes essential to maximize output within constraints.




## Learnings

Playing and solving Farmer is Replaced provided valuable insights and learning experiences in several areas:

**1.Optimizing Code for Efficiency**: The game taught the importance of writing clean, efficient loops and conditionals to navigate the grid, reducing redundant actions and optimizing the drone’s path to save resources and time.

**2.Resource Management and Planning**: Balancing limited resources like seeds, water, and crop yields highlighted the need for strategic planning. This required understanding when to trade, plant, or harvest specific crops to meet requirements without waste.

**3.Conditional Logic and Problem Solving**: The complex, multi-step tasks involving conditional actions (e.g., harvesting only when crops are ready, switching to fallback crops) improved understanding of nested conditions and recursive functions, which are essential for advanced coding logic.

**4.Debugging and Avoiding Infinite Loops**: Encountering infinite loops or unexpected recursion due to resource shortages underscored the importance of setting clear exit conditions and using error handling to maintain control flow.

**5.Grid-Based Movement and Coordination**: Developing precise algorithms to direct the drone across the grid and handle edge cases (like boundaries or revisiting cells) was a practical exercise in spatial reasoning and algorithm design.



## References

1.[Olexa](youtube.com/channel/UC_l-VTgITlhdOqaff4LdCkw)

2.[Jack Hodkinson](www.youtube.com/@jack.hodkinson)

3.[Chatgpt](https://chatgpt.com)
