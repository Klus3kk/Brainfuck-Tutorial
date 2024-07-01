# Brainfuck-Tutorial
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#overview">Overview</a>
      <ul>
        <li><a href="#what_is_brainfuck?">WHAT is Brainfuck?</a></li>
      </ul>
      <ul>
        <li><a href="#what_do_you_need?">What do you need?</a></li>
      </ul>
      <ul>
        <li><a href="#basics">BASICS</a></li>
      </ul>
      <ul>
        <li><a href="#examples">EXAMPLES</a></li>
      </ul>
      <ul>
        <li><a href="hello_world">"Hello world" PROGRAM</a></li>
      </ul>
    </li>
  </ol>
</details>


## Overview
This repository consists of the easy-to-understand tutorial of Brainfuck with some examples of usage.


## WHAT is Brainfuck?
Brainfuck is (or will be) the most complicated programming language you'll use because of how different the rules of writing are. The language is Turing-complete and it only consists of 8 operators. The language itself might be really challenging for begginers.


## What do you need?
Firstly, you need a compiler/interpreter (you can download one from here: https://github.com/fabianishere/brainfuck, requires C/CMake to work). You can also use the online one: https://www.tutorialspoint.com/execute_brainfk_online.php. Also, make sure that you have an ASCII chart ready because you'll use it A LOT for writing text as the output. Also, the calculator, for calculations.


## BASICS
Let's start from explaining what does each operator do:


* '<' - moves the pointer to the right by one block
* '>' - moves the pointer to the left by one block
* '+' - increases value stored at the block by the memory pointer
* '-' - decreases value stored at the block by the memory pointer
* '[' - it's like while(current_value_of_the_block != 0)
* ']' - end of while loop (if the current value of the block is 0)
* ',' - inputs one character
* '.' - prints 1 character

  
Any other characters are considered as comments. All memory blocks are set to zero at the beggining.


## EXAMPLES
Here are some examples:


```
>>>-<+
```


- First, we're moving the pointer by three position, so the pointer should point at the block index 3 (because we're starting from index 0 block)
- Then we're decreasing the value of the current pointed block by 1 (so it's -1)
- Then we're moving back by one and we're increasing the value of the block by 1
Final results:
```
[0] [1] [2] [3].....
 0   0   1  -1
         ^
```
<br>

```
+++[->+<]
```
- We're increasing current memory pointers (index 0) value to 3 (+++)
- Then we're entering the loop which decreases the value of the current value of the index 0 block by one,
- After that we move to the index 1 block and we increase it's value by one
- Then we revert back to the first block
- The loop breaks when the first index value will be 0
So the final results should look like this: 
```
[0] [1] [2] [3].....
 0   3   0   0
 ^
```
## Hello world
Here's the basic program that writes "Hello World!" at the screen (here's when you use ASCII table c:)


```
++++++++++[>+++++++>++++++++++>+++>+<<<<-]>++.>+.+++++++..+++.>++.<<+++++++++++++++.>.+++.------.--------.>+.>.
```
