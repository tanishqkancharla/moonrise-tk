# Programming is a cycle of generalizing and implementing

I've found that I often think of code as generalizing then implementing. Generalizing involves thinking of the structure at hand, i.e. the purpose of your program or feature in context of the other features, what inputs it needs, what outputs it provides etc. 

This sort of cycle follows not only through development, but also past the release in forms of software updates, and it also applies to UI as much as back end.

Usually you start with some sort of localized feature, such as Slack allowing you to turn notifications for the app on and off. Then either through user feedback or their own testing, they realize users may want a lower granularity, so Slack lets you turn off some notifications and leave others on such as direct mentions etc. After years, people have used the product so much that the feature needs to be generalized even further, letting you edit specific times and days you can receive notifications.

The problem with this approach is that as a product and its features become more and more generalized, new users find it more difficult to understand the program. In the case of UI, it's actual users, and in the case of back end, it may be new developers looking to improve the system.