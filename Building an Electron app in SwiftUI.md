# Building an Electron app in SwiftUI
I thought more about my note taking app and I realized that if I want to make the app available for Web, Windows, and Android eventually, I'm not gonna be able to use SwiftUI. A cross-platform app framework like Electron lets you make apps with web technologies but I despise the HTML/CSS/Javascript workflow. SwiftUI could do the same thing far better. Javascript is a very high level language without typechecking and it tends to be a lot less performant than lower level languages like Rust or Swift.

Luckily I found the SwiftWASM project. Ideally, what I'm trying to get working is compile SwiftUI to WASM which can then be used in an Electron app. I feel like I'm thinking of such bold ideas with having basically zero experience in WASM and Electron and only a little experience with Swift, but if this works, this could honestly be a game-changer. 

