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
* Selects the mode in which the LED ring operates
  * 0: off
  * 1: progress mode
  * 2: pulsate/waiting mode
  * ...: TBD
### param: uint16
* Defines a paramameter to be used in a certain mode
  * Progress mode: value 0-1000, sets progress promillage
### color: HSL
* See [HSL](#HSL)

## HSL
Defines color for led ring
### hue: uint8
* hue value 0-255
### sat: uint8
* saturation value 0-255
### val: uint8
* lightness value 0-255

## diaphragm
### diaphragm: uint8
* 1: hot
* 2: cold
### position: bool
* true: open
* false: closed

## sensorRequest
### sensor: string
* `temperature`: temperature inside cooler
* `weight`:
* `spill`:
* `laser-0`:
* `laser-1`:
* `cold-stock-0`:
* `cold-stock-1`:
* `cold-stock-2`:
### return - status: uint8
*
### return - value: float32
* Value as measured by the requested sensor
