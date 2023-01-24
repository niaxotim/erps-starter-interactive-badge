### @activities true
### @explicitHints true

# ERPS :: Interactive Badge - Tutorial

## Introduction
### Introduction Step @unplugged
Welcome to your first turorial with the BBC micro:bit!
You are going to make an interactive badge, that will show your mood to your friends.
![Interactive badge](https://raw.githubusercontent.com/niaxotim/erps-starter-interactive-badge/master/assets/badge.png)

## Displaying an image
### Step 1
To draw an image on your micro:bit when it's powered on, drag a ``||basic:show leds||`` block from the code area (on the left) inside the ``||basic:start||`` block.

### Step 2
To create an image to display, click on leds that you want to light up.

#### ~ tutorialhint
```blocks
basic.showLeds(`
    . . # . .
    . # . # .
    # . . . #
    . # . # .
    . . # . .
    `)
```

### Step 3 @unplugged
Your code will run automatically in the emulator on the left.
![Emulator](https://raw.githubusercontent.com/niaxotim/erps-starter-interactive-badge/master/assets/emulator.png)

### Step 4 @unplugged
Connect your BBC micro:bit and click ``|Download|``.  
  
This will create and download a **.hex** file that will run on your micro:bit.  
  
Use the USB cable to plug your micro:bit into your computer. You should then see your micro:bit appear in your computer's file manager as a USB drive.  
  
A light on the back of your micro:bit will flash while the file is being copied. Once this has stopped your program will run. You can click the reset button on the back of your micro:bit to restart the program.

## Displaying a happy face
### Step 5
Let's show a happy face on your micro:bit when the 'A' button is pressed.  
  
So far, you've only run code when the micro:bit is powered on. You can also run code when a button is pressed.  
Drag an ``||input:on button A||`` block from input and make sure 'A' is selected.

#### ~ tutorialhint
```blocks
input.onButtonPressed(Button.A, function () {
})
```

### Step 6
Any code added inside this block will run when the 'A' button on your micro:bit is pressed.  

Drag another ``||basic:show leds||`` block inside your new event, and draw a happy face pattern.

#### ~ tutorialhint
```blocks
input.onButtonPressed(Button.A, function () {
    basic.showLeds(`
        . # . # .
        . # . # .
        . . . . .
        # . . . #
        . # # # .
        `)
})
```

### Step 7 @unplugged
Test out your new code in the emulator. Press the 'A' button and you should see a happy face on your micro:bit.
![Emulator happy](https://raw.githubusercontent.com/niaxotim/erps-starter-interactive-badge/master/assets/emulator_happy.png)


## Challenge: Displaying a sad face
### Step 8
Can you make your micro:bit display a sad face when the 'B' button is pressed? You'll need to use a  ``||input:on button B||``  block to do this and select 'B'.

#### ~ tutorialhint
```blocks
input.onButtonPressed(Button.B function () {
    basic.showLeds(`
        . # . # .
        . # . # .
        . . . . .
        . # # # .
        # . . . #
        `)
})
```

## Creating a simple animation
### Step 9
Let's create a (very) simple animation for your happy and sad faces.

Add a second ``||basic:show leds||`` block to your ``||input:on button A||`` block, with a neutral face.

#### ~ tutorialhint
```blocks
input.onButtonPressed(Button.A function () {
   basic.showLeds(`
        . # . # .
        . # . # .
        . . . . .
        # # # # #
        . . . . .
        `)
    basic.showLeds(`
        . # . # .
        . # . # .
        . . . . .
        # . . . #
        . # # # .
        `)
})
```

### Step 10
If you run this code to test it, you'll notice that the pattern changes quickly. For a longer delay, you'll need to add a ``||basic:pause||`` block between the two images being displayed.

#### ~ tutorialhint
```blocks
input.onButtonPressed(Button.A function () {
   basic.showLeds(`
        . # . # .
        . # . # .
        . . . . .
        # # # # #
        . . . . .
        `)
    basic.pause(100)
    basic.showLeds(`
        . # . # .
        . # . # .
        . . . . .
        # . . . #
        . # # # .
        `)
})
```


### Step 11
To choose how many milliseconds to wait, click the down-arrow and enter a number. 1000 milliseconds is 1 second, so 250 milliseconds is a quarter of a second.  

You'll also need to animate your sad face. The easiest way to do this is to duplicate the blocks you've just created. Right-click on a block to duplicate it. Note that the PXT editor just duplicates one block at a time (not multiple blocks like Scratch.)  

You can then drag these blocks into your ``||input:on button B||`` block.


#### ~ tutorialhint
```blocks
input.onButtonPressed(Button.B function () {
   basic.showLeds(`
        . # . # .
        . # . # .
        . . . . .
        # # # # #
        . . . . .
        `)
    basic.pause(1000)
    basic.showLeds(`
        . # . # .
        . # . # .
        . . . . .
        . # # # .
        # . . . #
        `)
})
```

### Step 12 @unplugged
Test your code, and you should see your animated happy and sad faces when you press button A and B.

![Final badge](https://raw.githubusercontent.com/niaxotim/erps-starter-interactive-badge/master/assets/badge-final.gif)

### Animated Badge tutorial Complete @unplugged
Great work! Congratulations on your first micro:bit project!
![Great job](https://raw.githubusercontent.com/niaxotim/erps-starter-interactive-badge/master/assets/great_job.png)
