## Count colours

In this step, the sprite will stamp a copy of itself on the Stage. Each stamp will represent how many animals of that colour have passed the **Target** sprite. By counting the number of stamped animals on the screen, you will know how many have passed the camera.

--- task ---

Select your animal sprite, and then in the **Code** tab, add the `Pen`{:class="block3extensions"} extension.

--- /task ---

--- task ---

Each time the sprite moves, it can `stamp`{:class="block3extensions"} an image of itself on the Stage:

![image of the toucan sprite](images/animal-sprite.png)

```blocks3
when I receive [red v]
+ stamp
change x by [10]
```
--- /task ---

--- task ---

Click on the green flag and then hold your coloured paper up to the camera. You should see the animal move across the Stage, and leave behind a stamped image of itself.

--- /task ---

At the moment, because the sprite is visible, you are counting one too many animals. To solve this, you can hide the sprite.

--- task ---

Add the following code, to hide and show the sprite as it moves:

![image of the toucan sprite](images/animal-sprite.png)

```blocks3
when I receive [red v]
+show
stamp
change x by [10]
+hide
```

--- /task ---

--- task ---

Click on the green flag and test the motion and stamping of the sprite while you hold up the coloured paper to the camera.

--- /task ---

To finish off, the Stage needs resetting each time the green flag is clicked on.


--- task ---

Add the following script to the animal sprite, to reset the animal's position and clear the screen of the stamps:

![image of the toucan sprite](images/animal-sprite.png)

```blocks3
when flag clicked
hide
erase all
go to x: [-200] y: [-90]
```

--- /task ---

--- task ---

Click on the green flag again and the screen should clear. Hold up the coloured paper to advance and stamp the sprite.

--- /task ---

--- save ---
