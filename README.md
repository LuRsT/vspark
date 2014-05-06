vspark
======

Create utf8 or ascii vertical graphs with ease.

## Setup

    $ curl https://raw.githubusercontent.com/LuRsT/vspark/master/vspark > ~/bin/vspark
    (Examine ~/bin/vspark)
    $ chmod +x ~/bin/vspark

## How to use

With a set of numbers:

    $ vspark 1 20 400 300 200
    ▏
    ▏
    █
    ▊
    ▌

or via STDIN:

    $ seq 0 10 | sort -R | vspark
    ▏
    ▌
    ▍
    ▊
    █
    ▎
    ▉
    ▋
    ▍
    ▏
    ▋

You can also choose how many columns do you want the graph to spread out, by changing the `GRAPH\_SIZE` env variable:

    $ seq 10 | GRAPH_SIZE=10 vspark
    █▏
    ██▏
    ███▏
    ████▏
    █████▏
    ██████▏
    ███████▏
    ████████▏
    █████████▏
    ██████████▏

And if it strikes your fancy, you can display the numbers next to each bar, by
using `DISPLAY\_NUMBERS` env variable (just needs to have some value in it):

    $ seq 10 | GRAPH_SIZE=10 DISPLAY_NUMBERS=1 vspark
     1 █
     2 █▉
     3 ██▊
     4 ███▋
     5 ████▋
     6 █████▌
     7 ██████▍
     8 ███████▎
     9 ████████▏
    10 █████████▏


You can also have ASCII output using `CUSTOM_CHAR`:

    $ seq 10 | GRAPH_SIZE=5 CUSTOM_CHAR="=" vspark
    =
    =
    ==
    ==
    ===
    ===
    ===
    ====
    ====
    =====

## Creative uses

You can create the shadow of a file:

    $ awk '{ print length($0) }' vspark | GRAPH_SIZE=57 vspark
    █████████████▍
    ▏
    █████████▉
    ███████████▋
    ▏
    █████████████████████████████████████████
    ██████████████████████████████▎
    ▏
    ▏
    █████████████████████████████████▉
    ▏
    ████████████████████████████████▏
    ▏
    ██████████████████▊
    ███████████████████████████████████████████▋
    █
    ▏
    █████████
    ██████████████████▊
    ██████████████████▊
    ██████████████████▊
    ▏
    █████████████████████████████████
    ▏
    ██████████████████████████████████▊
    ██████████████████████████████████▊
    ▏
    ████████████████████████████████████████████████████████▏
    ▏
    ████████████████████████████████████████████████████▌
    ████████████████████████████████████████████████████▌
    ▏
    ██████████████▎
    █

Add yours...

## Vspark in other languages

* Add yours here

## Licence

The MIT License (MIT)

## FAQ

#### Why perl?

Because, chances are, you already have it installed.

#### Can you change the LICENCE to XXXXXX?

Nope, I chose the MIT Licence because that's the one I want to use.

#### Can I create this in XXXX language?

Of course, but send a pull request to me with the link so I can add to this README file.
