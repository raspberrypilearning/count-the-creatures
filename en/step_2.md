## Detecting colours

In this step you will learn how to use the `video`{:class="block3extensions"} library to detect different colours on the screen. Get your three different coloured plain pieces of paper or objects ready!

--- task ---

Open a new Scratch project.

**Online:** open a new online Scratch project at [scratch.mit.edu](https://scratch.mit.edu/projects/editor/){:target=”_blank”}.

**Offline:** open a new project in the Scratch offline editor. If you need to, you can [download and install Scratch here](https://scratch.mit.edu/download){:target=”_blank”}.

--- /task ---

--- task ---

Begin by deleting **Sprite1**. Then create a new sprite using the **Paint** tool.

![image showing the new sprite paint tool being selected](images/paint-new-sprite.png)

--- /task ---

--- task ---

Use the **Circle** and **Line** tools, to create a target sprite at the centre of the canvas. You can fill the circle with any colour you like. Name the sprite **Target**.

![image of a drawn target](images/target.png)

--- /task ---

--- task ---

Click on the **Code** tab for your new sprite, and then the **Add Extension** button in the bottom left hand corner of the screen.

![image showing add extension button](images/add-extension-block.png)

Select the **Video sensing** extension block.

![image showing the graphic for the video sensing extension block](images/video-sensing-extension-block.png)

If asked, **Allow** access to your webcam.

![image showing Firefox prompt for allowing access to the webcam](images/camera-allow.png)

--- /task ---

Now you need to turn the video on to activate the computer's camera.

--- task ---

Add the following blocks: `green flag clicked`{:class="block3events"}, `set video transparency to`{:class="block3extensions"} `0`, `turn the video on`{:class="block3extensions"} and `set ghost effect to`{:class="block3looks"} `80`:

![image of target sprite](images/target-sprite.png)

```blocks3
when flag clicked
set video transparency to [0]
turn video [on v]
set [ghost v] effect to [80]
```
--- /task ---

--- task ---

Add a `forever`{:class="block3control"} loop to the bottom of your script, and within this place an `if ... then`{:class="block3control"} block:

![image of target sprite](images/target-sprite.png)

```blocks3
when flag clicked
set video transparency to [0]
turn video [on v]
set [ghost v] effect to [80]
+forever
+if <> then
```

--- /task ---

--- task ---

The `if ... then`{:class="block3control"} block will detect when a certain colour touches the **Target** sprite. Add in a `touching color`{:class="block3sensing"} block to the script:

![image of target sprite](images/target-sprite.png)

```blocks3
when flag clicked
set video transparency to [0]
turn video [on v]
set [ghost v] effect to [80]
forever
+if <touching color [] ?> then
```
--- /task ---

--- task ---

Click on the coloured oval within the `touching color`{:class="block3sensing"} block, and then select the **eye dropper** tool which you will find below the three colour sliders. 

![image showing the eye dropper tool](images/eye-dropper-tool.png)

Now hold up one of your coloured pieces of paper in front of the camera, and use the **eye dropper** tool to select the colour of the paper. The example uses red paper but remember you can use paper or objects and any colours you like.

![image showing the paper being held in front of the camera and the eye dropper tool being used to select the colour of the paper](images/select-colour.png)

That colour should now be visible in the `touching color`{:class="block3sensing"} block:

![image of target sprite](images/target-sprite.png)

```blocks3
when flag clicked
set video transparency to [0]
turn video [on v]
set [ghost v] effect to [80]
forever
+if <touching color [#FF6E66] ?> then
```

--- /task ---

--- task ---

Add a `say for 2 seconds`{:class="block3looks"} adding in the text for the colour you selected:

![image of target sprite](images/target-sprite.png)

```blocks3
when flag clicked
set video transparency to [0]
turn video [on v]
set [ghost v] effect to [80]
forever
+if <touching color [#FF6E66] ?> then
say [red] for [2] secs
```

--- /task ---

--- task ---

Click the `green flag`{:class="block3control"} and hold up the paper and wave it over the target a few times, and it should say `red`{:class="block3looks"}.

--- print-only ---

![image showing the colour red being detected](images/colour-detect.png)

--- /print-only ---

--- no-print ---

![gif showing the colour red being detected](images/colour-detect.gif)

--- /no-print ---
--- /task ---

--- save ---
