# SwiftUI for Web

I've really enjoyed using SwiftUI to develop user interfaces; I think it's an interesting idea to approach using SwiftUI for web development. Why separate web design into 3 different languages, html, css, and js, if one language can handle it all?

Some references:

[dokun1/Vaux](https://github.com/dokun1/Vaux)

This is a library that transforms SwiftUI views to html pages, but I'm imagining a browser that can just parse SwiftUI views directly instead of going through HTML.

[SwiftWebUI/SwiftWebUI](https://github.com/swiftwebui/SwiftWebUI)

SwiftWebUI is closer to what I'm imagining, but it's still mostly a compatibility layer between HTML and Swift.

Jul 15, 2020 

SwiftUI displaces HTML as a declarative framework to design. View Modifers replace CSS. Swift itself replaces javascript. It seems natural to suggest that it can replace the HTML/CSS/JS frameworks. WebKit stands at a particularly interesting position to have this come to life, since (I assume) they have access to the SwiftUI framework and Safari.