# Creating a personal website with Notion

Notion is a pretty great tool, one of the best things about it is the consistent design language everywhere, and how easy it is to add content. Using it as a CMS for a personal website is a good idea, though I wonder if the limitations of Notion would restrict me too much.

I've also put a lot of work into my other website:

[Home](http://tkancharla.com/)

although I put work in a long time ago and I'm not particularly attached to it. It's hard to add content to it quickly (have to go through wordpress admin etc.) so I haven't added anything to it in a while.

I succeeded in moving my site to moonrise.tk, although I have to admit, I was looking at the script for how it works (on fruitionsite.com) and I have no idea how it does what it does. It deals with a lot of CORS header manipulation. Also, databases don't show up, so posts like this don't show up.

Turns out databases do show up, and I took a much closer look at the code. Essentially what it does is, when a client requests the domain, a cloudflare worker runs the javascript code, retrieves the public facing notion website, makes some modifications to remove the notion logo etc. and returns it to the client. The pro is that you never even really have to have a server; the worker code returns the whole website so you can point your domain to any random server. The con is that it's very slow. Notion sites are already not very performant (I peeked into the javascript   code and saw that a lot of the code being returned was actually a gigantic dictionary mapping commands to emojis...for example `:raised_hand:` maps to 🤚). So that makes website loading quite a bit slow...but updates are so easy. Maybe eventually once I have my own notes system, I'll be able to move everything over.

As a followup, I've really enjoyed using Notion as a personal website. Making edits is so easy, but since it's setup on an unreliable system, it's possible a future Notion update will just break something. That's a problem for the future though.