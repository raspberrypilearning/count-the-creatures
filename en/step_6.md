## More animals

Add more coloured animals to count!

--- task ---

Right-click on your **Toucan** sprite (or animal sprite of your choice), **duplicate** it, and then go to the **Costumes** tab to recolour the sprite, or give it a completely new costume.

--- print-only ---

![gif showing duplication and re-colouring of the sprite](images/duplicate-colour-sprite.gif)

--- /print-only ---

--- /task ---

--- task ---

Repeat this process so that you have three animal sprites that match the colours of your paper or objects. The code will also be duplicated for each sprite.

--- /task ---

--- task ---

Edit the code so that each of the sprites has a unique starting position:

![image of blue toucan sprite](images/blue-toucan.png)

```blocks3
when flag clicked
hide
erase all
go to x: [-200] y: [-120]
```

![image of green toucan sprite](images/green-toucan.png)

```blocks3
when flag clicked
hide
erase all
go to x: [-200] y: [-150]
```
--- /task ---

Now, you need to change the `broadcast`{:class="block3events"} blocks to match the different colours in your code.

--- task ---

Change the broadcast trigger (currently set to `red`{:class="block3events"}, or the colour of your first piece of paper or object) for each of the new sprites:

![image of blue toucan sprite](images/blue-toucan.png)

```blocks3
+when I receive [blue v]
show
stamp
change x by [10]
hide
```

![image of green toucan sprite](images/green-toucan.png)
```blocks3
+when I receive [green v]
show
stamp
change x by [10]
hide
```

--- /task ---

--- task ---

Test your code.

Hold up the pieces of paper or objects in front of the camera, one at a time, and make sure that the correct sprites advance and create a stamp each time.

--- /task ---

--- save ---
