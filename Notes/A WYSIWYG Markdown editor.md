# A WYSIWYG Markdown editor

I've been racking my head recently over how a WYSIWYG Markdown editor should feel. Notion actually supports this, for example **bold** and *italic* hide the markdown tags, but then it's no longer possible to edit the tags.

[[Screen_Shot_2020-07-21_at_10.19.28_AM.png]]

Typora does this differently. It hides the tags too, but then when your cursor becomes active on the text, it shows the tags again. The problem with this is that all of the text you've written after it get pushed (since the markdown characters take up space again) but then get pulled back once you lose focus on the markdown token. 

There's also another popular way of doing it, which is just render the tokens but don't hide the markdown characters. For example `**bold**` will write the text "bold" in bold but keep the tags. This is not preferable since you have all these characters all over your text and it no longer looks clean.

One iteration that may be possible to try is when you focus on the text, have the markdown characters somehow take up no space (for example, if they showed up above the text or something). That way, the text doesn't get pushed. You would still need some way to edit the characters though. 

So I've been thinking more about how to do this and talked to Ellie. I think the idea that I have with the markdown characters taking up no space and showing up above the text could work pretty well.

However, the issue of how to render markdown text in real time is actually a pretty tough problem to solve. The "easy" way to do it is keep a copy of the styled version and the unstyled version of the text at once. Then, as users type text, they edit the "unstyled" version, which re-renders into the styled version every time. 

There are two problems with this; since you're showing users the styled version but letting them edit the unstyled version, somehow you'd have to keep track of where they're editing so you can properly propagate that to the unstyled version. The other problem is that re-rendering the whole page for one new character can be an extremely costly operation, making editing of long documents slower. 

Instead you can do something like notion and instead do a form of "on the fly" editing. This is much trickier than it seems though. Currently, it seems like the way they do it is monitor the character input and map it to the markdown equivalent if it is detect. For example, one asterisk will shift it into italic mode, two will shift into bold. This works well in most cases but it definitely breaks. For example , typing `exa*mple*` then going back and putting a space in between the "exa" and "mple" will not incorrectly leave the asterisks there. 

It's tough figuring out how the edit the user made actually affected the markdown document without re-rendering the whole thing. You'd have to store the styled/unstyled text a different way than just an array of strings.

Alright I've decided to do the sensible thing and before trying to implement this by myself in Swift, I'm learning more about how Prosemirror works. I want to be able to eventually build a similar Swift package, but that seems ages away; Prosemirror is a huge library.