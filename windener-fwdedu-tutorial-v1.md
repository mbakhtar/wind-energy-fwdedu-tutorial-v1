# Wind Energy CAK V2.1 fwdEDU

```package
fwdSensors=github:climate-action-kits/pxt-fwd-edu
jacdac=github:microsoft/pxt-jacdac
touch=github:climate-action-kits/pxt-fwd-edu/fwd-touch
fwd-edu-common=github:climate-action-kits/pxt-fwd-edu/fwd-common
````

## @showhint
Create a ``||Variables:Variable Revolutions||`` and nest 
``||Variables:set Revolutions to 0||`` 
under ``||basic:on start||`` block
```blocks
let Revolutions = 1
```

## @showhint
Now add ``||logic:If true then||`` block and nest it under
``||basic:forever||`` loop
```blocks
let Revolutions = 0
Revolutions = 1
basic.forever(function () {
if (true) {
        }
    })
```
## @showhint
Now add the true condition ``||modules:on button4 pressed||`` it replaces the true text loop
```blocks
let Revolutions = 0
Revolutions = 1
basic.forever(function () {
    if (fwdSensors.touch.fwdIsPressed()) {
        }
})
```
## @showhint
Add a ``||Variables:change Revolutions by 1||`` from the ``||Variables:Variables||`` drawer and 
then place it under the true condition of the ``||logic: if then||`` loop
```blocks
let Revolutions = 0
Revolutions = 1
basic.forever(function () {
    if (fwdSensors.touch.fwdIsPressed()) {
    Revolutions += 1
        }
})
```
## @showhint
Add a delay between the ``||modules:on button4 pressed||`` detecting a 
``||modules:touch or tap||``. 
Add a ``||basic:pause||`` block from ``||basic:basic||`` drawer
```blocks
let Revolutions = 0
Revolutions = 1
basic.forever(function () {
    if (fwdSensors.touch.fwdIsPressed()) {
        Revolutions += 1
    }
    basic.pause(20)
})
```
## @showhint
Add an ``||input:on button A pressed||`` block. 
This will be used to display a value stored in a 
``||Variables:Variable||``
```blocks
input.onButtonPressed(Button.A, function () {
   
})
let Revolutions = 0
Revolutions = 1
basic.forever(function () {
    if (fwdSensors.touch.fwdIsPressed()) {
        Revolutions += 1
    }
    basic.pause(20)
})
```
## @showhint
Nest the ``||basic:show number||`` block under the ``||input:on button A pressed||``
```blocks
input.onButtonPressed(Button.A, function () {
    basic.showNumber()
})
let Revolutions = 0
Revolutions = 1
basic.forever(function () {
    if (fwdSensors.touch.fwdIsPressed()) {
        Revolutions += 1
    }
    basic.pause(20)
})
```
## @showhint
Now insert ``||Variables:Revolutions||`` oval block in the 
``||basic:show number||`` block
```blocks
input.onButtonPressed(Button.A, function () {
    basic.showNumber(Revolutions)
})
let Revolutions = 0
Revolutions = 1
basic.forever(function () {
    if (fwdSensors.touch.fwdIsPressed()) {
        Revolutions += 1
    }
    basic.pause(20)
})
```

## @showhint
This is the final code
```blocks
input.onButtonPressed(Button.A, function () {
    basic.showNumber(Revolutions)
})
let Revolutions = 0
Revolutions = 1
basic.forever(function () {
    if (fwdSensors.touch.fwdIsPressed()) {
        Revolutions += 1
    }
    basic.pause(20)
})
```