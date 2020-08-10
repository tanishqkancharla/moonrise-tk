# Inconsistency between how easy it is to describe a change and how hard it is to do it

At first glance this is pretty obvious, but I'm actually referring to something fairly deep here. Suppose I have an idea, and it's fairly clear: it's a note-taking app. It's all great, but an idea comes up that exporting to PDF would be a useful feature. Implementing this idea could actually be quite a bit of work;  you'd have to create some sort of encoder between the model your app stores the notes in and the supported PDF format. Then you'd have to build some user interface and create storage to supply that PDF. It's a lot of work for an idea that can be described so easily; how does this happen?

Well taking notes is common; people have taken notes on something or another all throughout their life. Exporting digital notes to a PDF is a simple feature to describe and ask for since it is so deeply associated with note-taking itself. On the other hand, your note-taking app (at least not yet), is not so closely associated with exporting to PDF. Perhaps you have used some custom-made format that requires a lot of work to export to PDF. 

This is important because your custom-made format ends up "simulating" the note-taking experience for the user. That's why it's so easy for the user to make the connection to a pdf export.

However, since it's just a "simulation", *actually* adding a pdf export function can be pretty difficult.

I actually picked a fairly unclear example, so to make it more clear, let me describe the gradient in which all software falls: Image ↔model.