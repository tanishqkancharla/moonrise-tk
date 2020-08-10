# UIs driven by object handlers rather than event handlers

[https://twitter.com/tylerangert/status/1280342523945218048?s=21](https://twitter.com/tylerangert/status/1280342523945218048?s=21)

I thought this was an interesting idea, and in a way it reminded me of functional vs imperative programming. With imperative/object oriented programming, objects/view own the events. Flipping that means events own the objects, so the UI becomes interaction-based like functional programming responding to events happening (callbacks). I'm not sure if the analogy is 100% true though. I want to think of a good example to illustrate it.

Jul 24, 2020 

So if you abstract  a user interface to you, the user, it's basically a function with input where you tap on the screen or what gesture you use, to the output which is just some change in the visual user interface. Thinking about it from that perspective, it makes complete sense that the user interface should be built around the gesture the user performs. The user inputs some sort of event (click here, or pinch here) and expects a response (go to a different page, zoom out on map).

The problem is that in the eyes of the developer, it's actually the other way around. It would be a waste of time and space to create event handlers for every event that could happen anywhere on the screen. Most of the time, it's more like "if this event happens on this object perform this" which makes it much easier, since you can just attach the event handlers to the object.