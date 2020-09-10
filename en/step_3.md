## More colours

In this step, you will add code to make the camera detect more colours.

--- task ---

Right click on the `if ... then`{:class="block3control"} block and select **duplicate**, then add the new blocks to the bottom of your script. Repeat this a second time:

![image of target sprite](images/target-sprite.png)

```blocks3
when flag clicked
set video transparency to [0]
turn video [on v]
set [ghost v] effect to [80]
forever
if <touching color [#FF6E66] ?> then
say [red] for [2] secs
end
+if <touching color [#FF6E66] ?> then
say [red] for [2] secs
end
+if <touching color [#FF6E66] ?> then
say [red] for [2] secs
end
```

--- /task ---

--- task ---

Just as you did before, use the colour picker to change the colours of these new blocks, with different colours of paper. Also change the text in the `say`{:class="block3looks"} block:

![image of target sprite](images/target-sprite.png)

```blocks3
when flag clicked
set video transparency to [0]
turn video [on v]
set [ghost v] effect to [80]
forever
if <touching color [#FF6E66] ?> then
say [red] for [2] secs
end
+if <touching color [#00D6FF] ?> then
say [blue] for [2] secs
end
+if <touching color [#62E09A] ?> then
say [green] for [2] secs
end
``` 

--- /task ---

--- task ---

Test out your code, by clicking the green flag and holding up the different colours of paper over the target.

--- no-print ---

![gif showing the camera detecting three different colours](images/three-colour-detection.gif)

--- /no-print ---

--- print-only ---

![image showing the camera detecting the colour green](images/three-colour-detection.gif)

--- /print-only ---


--- /task ---

Depending on how the light in the room changes, the angle that you hold the paper at, and the quality of your webcam, you may find that sometimes the colour is not detected. To help with this, you can have the `touching color`{:class="block3sensing"} blocks detect more than one colour.

--- task ---

Add an `or`{:class="block3operators"} into the `touching color`{:class="block3sensing"} blocks:


![image of target sprite](images/target-sprite.png)

```blocks3
when flag clicked
set video transparency to [0]
turn video [on v]
set [ghost v] effect to [80]
forever
+if < <touching color [#FF6E66] ?> or < > > then
say [red] for [2] secs
end
+if < <touching color [#00D6FF] ?> or < > >  then
say [blue] for [2] secs
end
+if < <touching color [#62E09A] ?> or < > > then
say [green] for [2] secs
end
``` 

--- /task ---

The `or`{:class="block3operators"} block will allow for another `touching color`{:class="block3sensing"} block to be added into the `if ... then`{:class="block3control"}, so that more than one colour can be detected.

--- task ---

Add in three more `touching color`{:class="block3sensing"} blocks, and use the colour picker to select a different area on the paper. The colour recognition of your computer's camera will improve if you lighten the space you are working in. The camera may also get confused by similar colours in the room. For instance, the colour of your top, wall or chair. The below code allows for a slight variation of colours of red,  blue and green:

![image of target sprite](images/target-sprite.png)

```blocks3
when flag clicked
set video transparency to [0]
turn video [on v]
set [ghost v] effect to [80]
forever
+if <<touching color [#FF6E66] ?> or <touching color [#FF7E80] ?>> then
say [red] for [2] secs
end
+if <<touching color [#5DDCF5] ?> or <touching color [#00D6FF] ?>>  then
say [blue] for [2] secs
end
+if <<touching color [#62E09A] ?> or <touching color [#69E6A1] ?>> then
say [green] for [2] secs
end
``` 
--- /task ---

--- task ---

Test your code still works by clicking the `green flag`{:class="block3events"} and holding up the paper in front of the camera.

--- /task ---

--- collapse ---
---

title: More colours with nesting blocks

---

Some creatures are multi-coloured. It is possible to nest `or`{:class="block3operators"} blocks inside each other, so the camera looks for a number of colours in one creature. To do this, use the following code:

```blocks3
<<<touching color [#62EF9A] ?> or <touching color [#A9E6A1] ?>> or <<touching color [#A2F090] ?> or <touching color [#69C6AF] ?>>>
```

--- /collapse ---



--- save ---
