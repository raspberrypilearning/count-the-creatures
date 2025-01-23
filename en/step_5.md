## Count colours

Get your chosen animal sprite to stamp a copy of itself on the Stage each time it passes the Target. Use these stamps to track how many animals of that colour have crossed the camera.

--- task ---

Select your animal sprite, and then in the **Code** tab, add the `Pen`{:class="block3extensions"} extension. In this example we will use the **Toucan** sprite.

![A pen icon emitting a rainbow trail, accompanied by the title 'Pen' and the text 'Draw with your sprites' on a green background.](images/pen-extension.png)

--- /task ---

--- task ---

Each time the **Toucan** sprite moves, it needs to `stamp`{:class="block3extensions"} an image of itself on the Stage:

![image of the toucan sprite](images/animal-sprite.png)

```blocks3
when I receive [red v]
+ stamp
change x by [10]
```
--- /task ---

--- task ---

Click on the green flag and then hold your coloured paper or object up to the camera. You should see the **Toucan** sprite move across the Stage, and leave behind a stamped image of itself.

--- /task ---

At the moment, because the **Toucan** sprite is visible, your total includes one animal too many. To solve this, you can hide the sprite.

--- task ---

Add the following blocks, to `show`{:class="block3looks"} and `hide`{:class="block3looks"} the **Toucan** sprite as it moves:

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

Click on the green flag and test how the **Toucan** sprite moves and creates stamps while you hold up the coloured paper or object to the camera.

--- /task ---

To finish off, the Stage needs to be reset each time the green flag is clicked on.

--- task ---

Add the following script to the **Toucan** sprite, to reset the **Toucan** sprite's position and clear the Stage of the stamps:

![image of the toucan sprite](images/animal-sprite.png)

```blocks3
when flag clicked
hide
erase all
go to x: [-200] y: [-90]
```

--- /task ---

--- task ---

Click on the green flag again and the Stage should clear. Hold up the coloured paper or object to see the **Toucan** sprite advance and create a stamp.

--- /task ---

--- save ---
