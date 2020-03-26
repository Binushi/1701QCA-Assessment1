# Inventor Kit Experiments

*Markdown reference: https://guides.github.com/features/mastering-markdown/*

## Instructions ##

*For a selection of 5 inventor kit experiments that you choose, fill out the following sections.

### Using RGB LED Experiment 10 ###

(Using RGB LED Experiment 10)

#### Photo of completed project ####
let Blue = 0
let Green = 0
let Red = 0
basic.forever(function () {
    pins.analogWritePin(AnalogPin.P0, Red)
    pins.analogWritePin(AnalogPin.P1, Green)
    pins.analogWritePin(AnalogPin.P2, Blue)
    if (pins.digitalReadPin(DigitalPin.P8) == 1 && Green < 1020) {
        Green = Green + 10
    } else if (pins.digitalReadPin(DigitalPin.P8) == 1 && Green == 1020) {
        Green = 0
    }
    if (pins.digitalReadPin(DigitalPin.P12) == 1 && Red < 1020) {
        Red = Red + 10
    } else if (pins.digitalReadPin(DigitalPin.P12) == 1 && Red == 1020) {
        Red = 0
    }
    if (pins.digitalReadPin(DigitalPin.P16) == 1 && Blue < 1020) {
        Blue = Blue + 10
    } else if (pins.digitalReadPin(DigitalPin.P16) == 1 && Blue == 1020) {
        Blue = 0
    }
})

![Image](missingimage.png)

There are 3 buttons, one for the red, one for the blue and one for the red. When you press the button the amout of that color shown on the RGB LED changed.

#### Reflection ####

In this experiment, something new to me was or something I learned was, how to use the RGB LED and that the 4 pins on the RGB LED coresponds to a colour and ground. I also learnt some Java Script.

This experiment could be the basis of a real world application such as drecortive lighting in a room or shop.

### Experiment name ###

(Replace this with the experiment name)

#### 3 Dimming an LED using a potentiometer ####
let light_state = 0
input.onPinPressed(TouchPin.P0, function () {
    if (light_state == 0) {
        light_state = 1
    } else {
        light_state = 0
    }
})
basic.forever(function () {
    if (light_state == 1) {
        pins.analogWritePin(AnalogPin.P2, pins.analogReadPin(AnalogPin.P1))
    } else {
        pins.digitalWritePin(DigitalPin.P2, 0)
    }
})


![Image](missingimage.png)

There is a dile on micro bit when you  turn it to the righ the brightness goes up when it turn it to the right the brightness goes down. 

#### Reflection ####

In this experiment, something new to me was or something I learned was how to use the dile.

This experiment could be the basis of a real world application such as again lighting ina room or shop.

### Experiment name ###

(Replace this with the experiment name)

#### 2 Using a light sensor and analogue inputs ####
let light = 0
basic.forever(function () {
    light = pins.analogReadPin(AnalogPin.P0)
    if (light > 200) {
        basic.showLeds(`
            # . # . #
            . # # # .
            # # # # #
            . # # # .
            # . # . #
            `)
    } else {
        basic.showLeds(`
            # # # . .
            . # # # .
            . . # # .
            . # # # .
            # # # . .
            `)
    }
})

![Image](missingimage.png)

depending on how much light is on the phototransistor a sun or a moon will be displayed on the micro bit.

#### Reflection ####

In this experiment, something new to me was or something I learned was what the Phototransistor is and how to use it.

This experiment could be the basis of a real world application such as a streetlights they detect the amout of light there is and turn on is needed.

### Experiment name ###

(Replace this with the experiment name)

#### 9 Copastor charge  ####
let percentage = 0
let cap_voltage = 0
basic.forever(function () {
    cap_voltage = pins.analogReadPin(AnalogPin.P0)
    percentage = cap_voltage / 10
    basic.showNumber(percentage)
    if (percentage > 1 && percentage <= 2) {
        pins.digitalWritePin(DigitalPin.P1, 1)
    } else if (percentage > 2 && percentage <= 3) {
        pins.digitalWritePin(DigitalPin.P1, 1)
        pins.digitalWritePin(DigitalPin.P2, 1)
    } else if (percentage > 3 && percentage <= 4) {
        pins.digitalWritePin(DigitalPin.P1, 1)
        pins.digitalWritePin(DigitalPin.P2, 1)
        pins.digitalWritePin(DigitalPin.P8, 1)
    } else if (percentage > 4) {
        pins.digitalWritePin(DigitalPin.P1, 1)
        pins.digitalWritePin(DigitalPin.P2, 1)
        pins.digitalWritePin(DigitalPin.P8, 1)
        pins.digitalWritePin(DigitalPin.P12, 1)
    } else {
        pins.digitalWritePin(DigitalPin.P1, 0)
        pins.digitalWritePin(DigitalPin.P2, 0)
        pins.digitalWritePin(DigitalPin.P8, 0)
        pins.digitalWritePin(DigitalPin.P12, 0)
    }
}) 


![Image](missingimage.png)

(Insert a caption here)

#### Reflection ####

In this experiment, something new to me was or something I learned was (insert something here).

This experiment could be the basis of a real world application such as (insert something here).

### Experiment name ###

(Replace this with the experiment name)

#### Hellow World ####
input.onButtonPressed(Button.A, function () {
    basic.showLeds(`
        . # . # .
        . # . # .
        . . . . .
        # . . . #
        . # # # .
        `)
})
input.onButtonPressed(Button.B, function () {
    basic.showString("Hello world!")
})
input.onButtonPressed(Button.AB, function () {
    basic.showLeds(`
        . # # # .
        # . # . #
        # # # # #
        # # # # #
        # . # . #
        `)
})


![Image](missingimage.png)

The micro bit drsplays the words hellow world

#### Reflection ####

In this experiment, something new to me was or something I learned was how to use the micro bit.

This experiment could be the basis of a real world application such as billboards or on the side of buildings. 

