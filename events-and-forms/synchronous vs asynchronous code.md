# Synchronous

Your code instructions will run in a sequential manner, one after the other, in the order that you have written them in. If a function is called at any point during the sequence, then the program execution jumps to the instructions inside that function and runs them sequentially until a result is return / the function block is finished, at which point the program jumps back to where the function was called and continues running.

# Asynchronous

In asynchronous code, we let the JS Engine run specific functions at a later stage. Ie. our main script has finished running, but we left instructions to the Engine to run other functions at a later date. In particular:

- We might have setup timers that when elapsed will call a function that runs some code
- We might have registered to react to an event that the user creates (ie. by interacting with the page), so that when the user interacts, the callback function is run
