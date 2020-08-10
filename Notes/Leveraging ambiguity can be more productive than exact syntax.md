# Leveraging ambiguity can be more productive than exact syntax

[https://twitter.com/iopeak/status/1283223085894656000?s=20](https://twitter.com/iopeak/status/1283223085894656000?s=20)

I've often stood against Siri/Alexa and other NLP engines due to the following situation: you request something, and the voice assistant does not recognize it or misinterprets it, you lose trust in the system. For this reason, I've always been against no-code movements too, since they often prefer ambiguous natural-speak statements over code-like statements. Of course a perfect system that mirrors the way people think would be ideal for tasks but NLP algorithms are not there yet. 

Steve from Storyscript gets around this problem but having the UI provide subtle feedbacks/suggestions to the user as they type. The suggestions (obviously) are the commands the system understands. This sort of feedback is not provided by voice assistants (vocal feedback is much more clunky), but visual feedback is easily understood by people. This all goes back to how [User interfaces and users are a two way information transfer](https://www.notion.so/User-interfaces-and-users-are-a-two-way-information-transfer-de798acbf8d549c9a1fbdb7bdd197c50). 

This system is pretty unique...in a way it mostly is code, except there are multiple ways to do the same thing. In code, if you want a `for` loop, you use a `for` loop. In the Storyscript system, you can use the same `for` loop saying `For items in this` or `Loop over these` or `As this happens`, etc. The benefits of this seem to be that it's easier for a user who may not know what a `for` loop is to ask for it in the way familiar to them. 

As easy to use as the interface can be, on the other end of the spectrum is power. Since the Storyscript model of writing algorithms matches the ambiguous thought of a person, it is also limited by the same. With rigid code, one person can build a very complex system by effectively isolating and working on separate tasks. If Storyscript could provide the same, it should allow writing "functions" and then assigning them natural descriptions. For example an isolated task to send messages to your team about something would be

```arduino
send mark an email about this
send emily an email about this
send a slack message in the team chat about this
```

and then you could assign that `message the team about this` (and it expects an input).

Created an idea about this:

[Ambiguous Programming Language](https://www.notion.so/Ambiguous-Programming-Language-61ee410dd38f4d05ae3e218b5d3e57be)