## Chess ARM

"Chess ARM" is a piece of hardware that takes commands in the form of:

```javascript
Arm.move('e2', 'e4'); // blocks and returns when move is completed
```

and does the actual moves on the board. It can be configured like this:

```javascript
Arm.configure({
    board_lower_left: (3.26, 3.20),
    board_upper_right: (36.4, 37),
    board_height: 1.1,
    graveyard_position: (20.2, 1.4),
    memory_positions: {
        'm1': (30, 31.1),
        'm2': (30, 33.1),
        'm3': (30, 35.1),
        'm4': (30, 37.1)
    }
})
```

It can move pieces to the graveyard:

```javascript
Arm.move('e4', null) // Removes a piece off the board
```

or from/to "memorized" positions:

```javascript
Arm.move('m', 'c8')  // Promotion from "memory" square
```
