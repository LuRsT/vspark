vspark
======

Like spark, but vertical.

Create utf8 or ascii vertical graphs with ease.

    vspark 1 20 400 300 200
    ▏
    ▏
    █
    ▊
    ▌

or via STDIN:

    seq 0 10 | sort -R | vspark
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

You can also choose how many columns do you want the graph to spread out, by changing the env var TERM\_SIZE:

    seq 10 | TERM_SIZE=10 vspark
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


You can create the shadow of a file:

    awk '{ print length($0) }' vspark | TERM\_SIZE=57 vspark
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


You can display a graphic that spreads out through all your console wideness (in bash):

    seq 10 | TERM_SIZE=`tput cols` vspark
    [Too big a graph to show]


You can also have ASCII output using `CUSTOM_CHAR`:

    seq 10 | TERM_SIZE=5 CUSTOM_CHAR="=" vspark
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

