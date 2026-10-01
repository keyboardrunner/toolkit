**Torph**

Purpose
Torph is a text morphing animation library.
Use it when text needs to smoothly transform from one word or phrase into another.

**Use Torph when:**

•	Text changes from one value to another with a visual morphing effect.
•	The transition between text states is part of the UI interaction.
•	A heading, label, number, word, or short phrase needs to transform smoothly.
•	The design specifically calls for a text morphing effect.

**Examples**

Good use cases:
•	Loading → Ready
•	Day → Night
•	12 → 13
•	USD → EUR
•	Search suggestions changing between states
•	Animated headlines
•	Text changing during a UI transition

**Don’t use Torph when**

•	A simple fade is enough.
•	Text should slide, scale, or move rather than morph.
•	The animation is primarily about layout movement rather than changing characters.
•	The text is long or contains complex rich formatting.
•	A native CSS transition can achieve the same effect more simply.

**Implementation**
When Torph is selected for a project:
1.	Check the official repository for the current installation and API.
2.	Install Torph using the project’s package manager.
3.	Implement the animation using Torph’s current API.
4.	Follow the project’s existing framework and component conventions.
5.	Keep the animation subtle and purposeful unless the design explicitly requires a stronger effect.

**Official repository**

https://github.com/lochie/torph
AI instructions
When the user asks for:
•	text morphing
•	morphing text
•	morph animation between words
•	animated text transformation
•	smooth text-to-text transition
consider Torph as a candidate implementation.
Before writing custom morphing animation code, check whether Torph can satisfy the requirement.
Do not copy the Torph source code into this toolkit.
Do not assume the API is unchanged. Check the official repository for the current installation instructions and API before implementation.
Related
Category: libraries
Type: animation / text

