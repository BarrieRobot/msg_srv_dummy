barrieduino

## activateOrder.msg
### order_type: uint8
- 0: drop cup
- 1: hot drink
- 2: cold drink

### selection: uint8
- TBD

## Move.msg
### lane: uint8
- 1: hot drink lane
- 2: cold drink lane

### location: uint8
* 0: zero location
  * hot: under cup dispenser
  * cold: can drop height (before the move down motion)
* 1: fill location
  * hot: under coffee machine
  * cold: fully down
* 2: pre-present location (right under present height without the drink hitting the diaphragm)
  * This movement consists of 2 stages for the hot drinks as it needs to switch from horizontal to vertical movement
* 3: presentation
  * Both for hot and cold the upper-most position where the drink sticks out through the presentation hole

## ledRing
### ring: uint8
* 1: hot
* 2: cold
### mode: uint8
* ?
### param: uint16
* ?
### color: HSL
* See [HSL](#HSL)

## HSL
Defines color for led ring
### hue: uint8
* hue value 0-255
### sat: uint8
* saturation value 0-255
### val: uint8

