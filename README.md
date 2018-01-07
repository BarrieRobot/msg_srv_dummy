barrieduino

## activateOrder.msg
order_type: uint8
- 0: drop cup
- 1: hot drink
- 2: cold drink

selection: uint8
- TBD

## Move.msg
lane: uint8
- 1: hot drink lane
- 2: cold drink lane

location: uint8
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
  
