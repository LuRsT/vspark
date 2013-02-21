vspark
======

Like spark, but vertical.

Create utf8 vertical graphs with ease.

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

With this, you can display a graphic that spreads out through all your console wideness (in bash):

    seq 10 | TERM_SIZE=`tput cols` vspark
    [Too big a graph to show]
