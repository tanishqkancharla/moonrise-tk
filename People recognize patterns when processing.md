# People recognize patterns when processing

Let's say I ask you to compute the 100th Fibonacci number. Obviously it's a very involved task, but supposedly you'd start with calculating f(99)+f(98), then you'd write 2*f(98)+f(97). Very quickly, you'll realize you'll have to start all the way at f(1) and work your way up to 100, so instead, you choose to start at f(1) instead and work your way up one by one.

It's a little bit contrived but this is a great example of how [[People improve solutions iteratively]]. If we were to remove the optimization you performed, you would have worked all the way down recursively to f(1) and then worked your way back up to f(99). After doing it this way, you would've realized since you're going all the way down to f(1), you might as well just start there anyway, and if you're asked to perform the task again (given you don't remember the answer), you'd start from f(1).

Humans are smart enough to not only reflect on solutions and make them better but also reflect on them "on the fly" i.e. while you're applying the first approach.

How did you realize the problem with the first approach? Well you mostly noticed a pattern: after writing f(98) and f(99), it seems like f(100) will eventually require all the Fibonacci numbers. This represents humans' insane ability to recognize patterns. However, the pattern is still a hypothesis; you're not *completely* sure that calculating f(98) will end at f(1). To do that you need to prove it.