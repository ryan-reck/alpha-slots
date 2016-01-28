# alpha-slots
An alphabetic slot machine simulator. Basically instead of a regular slot machine with pictures this one has wheels with letters and you win by spelling a word.

Since it was written quickly to scratch an itch while I was on vacation, it's just a terminal app with a curses ui. Though it still manages to animate the wheels when you spin and use colorful highlights to illuminate anything that wins. It also uses aspell to determine if you've spelled a letter.

Scoring and letter distribution on the wheels are derived from scrabble. i.e. vowels are worth one point and theremre lots of them while *q*, *j* and *z* only occur once each and are worth many more points.

# gameplay

You start the game with $100. Each turn you put coins in then pull the handle to spin. The more coins you play they more betting lines are active and the better your chances of winning. The default game only has 5 lines available (the obvious straight ones) but more can be made available with the --lines command-line option. In game help will cycle through all the available lines, highlighting each one. Pulling the handle, or pushing *s*, will start the wheels spinning. Once they come to a stop, your winnings are tallied and the game continues.

All play is for entertainment purposes only. This is not an actual gambling machine. No real money can be won or lost.

# keys

```
c:   insert coin
s:   spin
q:   quit
a/m: play maximum coins / all lines (money permitting)
h:   show in game help
l/space-bar: repeat last play (money permitting)
up:  display previous message
down: display subsequent message
```

# options

```
h, --help            show this help message and exit
  -r ROWS, --rows ROWS  Number of rows on the display.
  -w WHEELS, --wheels WHEELS
                        Number of wheels.
  -l {pure diagonals,zigzags11,zigzags1,knights,zigzags2,any diagonals}, --lines {pure diagonals,zigzags11,zigzags1,knights,zigzags2,any diagonals}
                        Additonal line sets to play.
  -s SIMULATED_TURNS, --simulate SIMULATED_TURNS
                        number of spins to simulate
  -S SEED, --wheel-seed SEED
                        seed for wheel generation.
```

# dependencies
 * Python2.7
 * aspell-python-py2
 * curses
