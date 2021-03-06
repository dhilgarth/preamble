Preamble
========

Introduction
------------

The preamble gem lets you add a yaml preamble to your files, much like the Jekyll static site generator


Example
-------

    ---
    key1: value1
    key2: [1, 2, 3]
    ---

    Your body content goes here.


Usage
-----

    Preamble.load("./file.xyz") 
    Preamble.load_multiple("./file.xyz", "./file.abc") 


Output
------

The Preamble.load function returns an array. The first part is your data, the second is the body conent.

    [ { "key1" => "value1", "key2" => [1, 2, 3] }, "\nYour body content goes here"]


Notes
-----

1. The preamble must begin and end with three dashes '---'
2. Whitespace can go above the preamble, but no content
3. This gem is template-agnostic. It doesn't care what your body content is. It just gives it to you as a string.


