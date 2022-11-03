**Stonks on PicoCtf by Ne0exe 03.11.2022**

Today Pico prepared a program written in C to analyse. We also got a netcat connection to see how it works in real life. Let's start by checking out how it works.

Okay, nothing special except that API token. 
Basically, API is Application Programming Interface and it's just a way of interacting with webpage. It's just like scrolling down the social media app but in a different way. 
Enough of this lecture, let's check out what's inside it.

Alright, this is the first time I need to understand a program so let's break it down. I've been writing in C years ago but syntax is still familiar to me. 
Let me write stuff down.
1) `int main(int argc, char *argv[])` gets 2 arguments: *argc* which is just amount of parameters provided at the beginning of the program whereas *argv* is a table (well, to be more precise there is char `*argv[]` which means it's a pointer to the first element in table with characters) of size provided by *argc*.
We dont'n know anything about the parameters or even number of them.
2) Next, program is calling two functions: `setbuf(stdout, NUll)` and `srand(time(NULL))`
`setbuf()` - 