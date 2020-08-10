# Apple's iPadOS pointer matches the granularity between the user's input and the UI

In Apple's WWDC 2020 event, they released a video talking about the design behind the iPad cursor (which is quite different from any standard computer cursor):

[Design for the iPadOS pointer - WWDC 2020 - Videos - Apple Developer](https://developer.apple.com/videos/play/wwdc2020/10640)

There was a lot of really interesting points they mentioned, but the one that caught my attention the most was the idea of granularity and precision (starting at 2:45). The problem was that a traditional computer pointer interfaces with the UI elements at a pixel level precision, but the UI elements only care about a button level precision (i.e. they just care about which button you press rather than where you press on the button). The mismatch between precision leads to uncomfortable user experiences such as the traditional cursor. The iPadOS team took the opportunity to design a completely new cursor for the iPad that takes the form of the button its hovering over, matching the precision of the input provided by the user to the precision of the UI.

The concept of this is an example of how [[Matching form in a stream of information avoids fr dd945f77b19d4989aed5a08fddfa17b0 | matching form in a stream of information avoids friction]]. 

In the traditional cursor case, one source is the user (me), and the other source is the UI, and the information being transferred is my intention (I want to click the play music button) via the cursor. 

More technically, the output from me is the specific pixel position I hover the cursor on (and click), while the music app only uses the information that the position is hovering over the play music button. 

The information I'm providing is at a much higher granularity than the UI needs, and the "cost" is being paid by me, the user. The "cost" can be be understood in the context that [[User interfaces and users are a two way informatio de798acbf8d549c9a1fbdb7bdd197c50 | User Interfaces and users are a two way information transfer]]