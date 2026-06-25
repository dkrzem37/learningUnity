# learningUnity
Here is my small adventure of getting familiar with Unity. Notes on what I've learned and created.


DAY 1
Navigating the scene. Moving objects. Creating my own prefabs, materials. Understanding collision, and components. Adding lights. Adding audio to the scene. Creating scripts. Coding movement and rotation.

DAY 2
Learned implementing jumping by adding force to the physical body. Learned triggers. triggering opening the door with animation. triggering particle effect after picking up a collectible.
Learning 2D. Movement, Collectibles, setting furniture and their physics, creating walls, adding UI that updates collectibles left. Creating a trigger zone that starts playing music. Uploading the game to unity play so that others can play it.


https://github.com/user-attachments/assets/4cfd368c-49fc-4c7d-b7ed-a3b88c4a90d6




DAY 3
Recording the project in unity. Learning how to program movement for a 2d platformer using unity's input system. Surprisingly complicated.
Problem #1 encountered:
my character trips on the ground and rolls over. Could be because of the box collider and unity physics.
Seems like the problem is having multiple box colliders as ground. It should be a smooth surface but I think that unity's physics fuck with it a bit. Making a separate, single box collider to cover all of the sprites that make up the ground solves the issue.
Problem #2
Most of the time I can't change the direction of the player when he is in air.
That's because I made it so that player can't change velocity of the character if it's greater than maxVelocity variable. The unity physics make the character slow down on the ground but they don't in the air.
Problem #3
The character seems to slow down a lot when hitting the ground. Don't know why. Probably unity physics.

Solution to problem #2 and #3 is to not rely on the unity's physics system. Although I could just change the logic of the code to solve #2.
Learned how to freeze the rotation of an object.



https://github.com/user-attachments/assets/eb13c18b-4368-4f36-8984-0f6b5f6adf3b



DAY 4
Adding animations to the player and tweaking movement. Finished all animations. IsGrounded check would be nice to prevent some animation bugging where the character is hanging by it's belly on an edge. I just removed circleCollider2D from the body and used one single boxCollider for the whole body instead. For now. Enough movement for now. Time to design a simple level and an exit. Camera as well.
Setting limits of the camera. Making the camera follow the player.
Implement end door to level, dying zone, collectible, instructions to movement
Learned how to use tile palette to create a grid map. Learned how to make text appear when player enters a box collider and how to make it disappear when the player exits the area.
Created a death zone. Learned how to switch between scenes (levels). Learned how to enable and disable components through code.



https://github.com/user-attachments/assets/8b1330e9-d173-4897-b7f5-2bc275fc1a98



DAY 5
Add a chest with animation and an item. lasers, moving spikes, falling blocks. Make movement better. make it so player can only jump once.
Added moving platforms. Made levels look better. Added spikes. Learned how to change physics shape of a tile in tile palette. Needed to disable and enable game object for the box collider to change in different levels. Need to remember for the future. Enabled the player to change directions even when he is moving at max speed. This makes it so player can change directions in the air now. Make jumping better in the future. Not so floaty.
Learned how to cast a raycast and how to apply a mask to it to ignore layers.
Made the player only be able to jump when grounded.
movement on the ground is a bit slower than the max allowed value because of the drag of the ground.



https://github.com/user-attachments/assets/0273cb12-bb67-44a1-8232-138bcbfca12f



DAY 6
Made a simple menu and created buttons that work. Make options work in the future ( audio volume). Made another level that will have double jump item. Finally added a working chest that spits out an item and has animation.
platforms and ground and isgrounded is a bit fucked.
I want to add an animation to an item coming from the chest.
Checking if I'm grounded with a raycast is not great. When I'm jumping through the platform I can jump again because the raycast is catching the platform.

DAY 7
My god... A lot of debugging and slow progress. Finally made double jump work. Also made it so that IsGrounded returns true only if velocity y is ==0.
Something with the moving platform fucks up the movement. Also on changing level canDoubleJump resets to false.
How do i make it so that when player jumps off platform he gets less jumps?
Learned how to change variables that are located in another script.



https://github.com/user-attachments/assets/2aa22824-7f35-4305-9943-69c39ea09b10



DAY 8
Rest

DAY 9
Pondered the point of existence.

DAY 10
Made transitions between levels.
Created spikes that come out of the ground using animation. The only thing is that if I want to create different timers for these spikes I need to create new animation.



https://github.com/user-attachments/assets/60cae062-f46d-4a24-b336-01bd339b8d6f

