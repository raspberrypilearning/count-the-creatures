## Broadcast colours

Use `broadcast`{:class="block3events"} blocks to send messages about colour from the **Target** sprite to the other sprites.

--- task ---

Import a new animal sprite into your project. You can choose any sprite you like, but in this example, we will use a **Toucan** sprite.

![An illustration of a toucan with a large orange and black beak, standing on a light background, with the label 'Toucan' underneath.](images/toucan.png)

--- /task ---

--- task ---

Click on the **Costumes** tab and change the colour of the animal so that it matches one of the colours of your paper or objects.

![image of the toucan sprite, now coloured red.](images/animal-sprite.png)

--- /task ---

--- task ---

Go back to your **Target** sprite. From the `Events`{:class="block3events"} blocks menu, drag a `broadcast message1`{:class="block3events"} block and then create a **New message**.

![image of the menu selection for a broadcast block](images/new-message.png)

Call the message `red` (or whatever the colour of your first piece of paper or object was).

![image showing the naming dialogue box, with red typed in](images/message-red.png)

--- /task ---

--- task ---

Add the new `broadcast red`{:class="block3events"} block into your script, so that it occurs when the camera sees the colour red (or the colour of your first object — remember to use the `broadcast`{:class="block3events"} block that shows the message that you just created!):

![image of target sprite](images/target-sprite.png)

```blocks3
when flag clicked
set video transparency to [0]
turn video [on v]
set [ghost v] effect to [80]
forever
if <<touching color [#FF6E66] ?> or <touching color [#FF7E80] ?>> then
+ broadcast [red v]
say [red] for [2] secs
end
if <<touching color [#00D6FF] ?> or <touching color [#00D6FF] ?>>  then
say [blue] for [2] secs
end
if <<touching color [#62E09A] ?> or <touching color [#69E6A1] ?>> then
say [green] for [2] secs
end
``` 

--- /task ---

--- task ---

Repeat this for the other colours:

![image of target sprite](images/target-sprite.png)

```blocks3
when flag clicked
set video transparency to [0]
turn video [on v]
set [ghost v] effect to [80]
forever
if <<touching color [#FF6E66] ?> or <touching color [#FF7E80] ?>> then
broadcast [red v]
say [red] for [2] secs
end
if <<touching color [#00D6FF] ?> or <touching color [#00D6FF] ?>>  then
+ broadcast [blue v]
say [blue] for [2] secs
end
if <<touching color [#62E09A] ?> or <touching color [#69E6A1] ?>> then
+ broadcast [green v]
say [green] for [2] secs
end
```
--- /task ---

--- task ---

Click back to your **Toucan** sprite (or the animal sprite that you chose earlier). Position and size your sprite so that it fits nicely on the left-hand side of the Stage, below the **Target** sprite.

![image showing animal sprite on lower left hand side of the stage](images/sprite-on-stage.png)

--- /task ---

--- task ---

Add code so that the sprite moves across the Stage each time it receives the `red`{:class="block3events"} broadcast:

![image of the toucan sprite](images/animal-sprite.png)

```blocks3
when I receive [red v]
change x by [10]
```

**Note:** If you have used a different animal sprite, make sure that you add code to your animal sprite instead. If you have used a different colour, make sure that you use the `broadcast`{:class="block3events"} block that shows the colour of your choice.

--- /task ---

--- task ---

Hold up your paper so that it touches the target. Test that the **Toucan** sprite (or animal sprite) moves across the Stage when the colour is recognised.

--- /task ---

--- save ---





