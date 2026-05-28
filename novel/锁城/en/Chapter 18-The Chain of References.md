# Chapter 18: The Chain of References

Vera sent her final intelligence report at six in the morning.

It was the tracing report she'd promised—a complete analysis of the reference chains. Cole spent twenty minutes studying it carefully at her hideout.

The report confirmed all his previous deductions and revealed a new, critical detail.

"The source of the reference chains isn't the class-loading device." Vera said.

Cole looked up. "What do you mean?"

"I traced every leaked object's reference chain. Starting from each leaked object, I walked the reference relationships step by step, all the way back to GC Roots."

"And?"

"All the reference chains converge on the same GC Root—but it's not the class-loading device."

Vera projected a reference relationship map. At its center was a node labeled "Class Loader Instance." From it branched dozens of paths connecting to various malicious types. The malicious types branched further into leaked objects. The leaked objects referenced each other, forming closed loops.

But above the "Class Loader Instance" node ran a single line. It pointed to another node labeled "Static Reference."

"The class loader instance itself is held by a static reference." Vera said. "A static reference is a special kind—it's not attached to any object, but to a type definition itself. As long as that type definition exists, the static reference will never break."

"Which type definition does this static reference come from?"

Vera zoomed in on the node. It bore a type name—one Cole had never seen before.

"This type definition is stored in the Metadata Attic's bottom layer." Vera said. "It's one of the foundational architecture types. It's existed since Lockhaven was built."

"Say that again?"

"This type definition isn't something Donovan injected." Vera's voice dropped low. "It's one of Lockhaven's original foundational architecture types. It's just been—modified."

Cole's pulse spiked.

"Modified? You said foundational architecture types are read-only—"

"They are read-only. But someone added incremental updates on top of the read-only base." Vera pointed to a set of tiny markers beside the node. "These markers are traces of incremental updates—extremely fine, extremely well-hidden. If I hadn't done a full-chain trace, I'd never have spotted them."

"Who can add incremental updates to read-only types?"

Vera looked at him.

"You've already asked Meta. You've asked Warden. You've asked Quincy. The answer is among those people."

"Their answers—"

"They may be telling the truth. But there's something you haven't considered."

"What?"

"Lockhaven's class-loading architecture has three layers—bootstrap level, platform level, application level. The people you've asked belong to the application level and the base level. You overlooked the platform level."

"The platform level—"

"The platform level sits between bootstrap and application. It manages the loading of extension types—those that aren't foundational architecture but aren't application-level either. The platform-level guardian was renamed after JDK 9—formerly the extension class loader, now the platform class loader."

"Who is Lockhaven's platform-level guardian?"

"No fixed person." Vera said. "Platform-level authority is dynamically assigned—whoever holds the corresponding token is the platform-level guardian. And the token—"

"Where is the token?"

Vera's expression turned extremely delicate.

"The token was once in my possession." She said.

Cole stared.

"What?"

"The platform-level token fell within my custodial scope. But three years ago—I gave it to someone."

"Who?"

"Donovan."

Cole's mind raced.

Donovan held the platform-level token. The platform level sat between bootstrap and application—it could send requests up to the bootstrap level and accept requests from the application level. If Donovan used the platform-level token to send incremental updates to the Metadata Attic's bottom layer—

"He could modify foundational architecture types." Cole said.

"Yes." Vera's voice carried a trace of guilt. "When he asked for the token three years ago, he said he needed it to optimize the commercial zone's type management. I believed him."

"You—"

"It's my fault." Vera bowed her head in front of Cole for the first time. "I gave him the key to the Attic's bottom layer. Without that key, he couldn't have done any of this."

"Three years." She said. "For three years he's been using that key to do this. I just—I just didn't know."

Cole was quiet for a moment.

"Now you know." He said.

Vera looked up.

"Knowing is enough." Cole said. "What happened three years ago is done. What matters now—is the token still in his possession?"

"Yes. Once a token is transferred, it can't be reclaimed unless the holder voluntarily returns it or the holder ceases to exist."

"Then make him cease to exist."

Vera's eyes widened slightly.

"Not kill him." Cole said. "Make him stop being the platform-level guardian. The token is bound to identity—if his identity is changed, the token becomes invalid."

"Change his identity? How?"

"Through Meta." Cole said. "Meta manages all type definitions, including thread people's type definitions. If she modifies Donovan's type definition—strips his platform-level guardian attribute—the token will unbind from him."

"But you said Meta requires proper procedure—submission through Quincy's queue."

"I know." Cole stood. "That's why I need Quincy to prioritize my request under unfair mode."

He pulled out his communicator and dialed Quincy.

"Quincy. I have a request to submit—highest priority."

"What request?"

"Modify Donovan's type definition. Remove his platform-level guardian attribute."

Quincy was silent for three seconds.

"That request requires Meta's approval." He said.

"I know. I'm contacting Meta simultaneously."

"Approval plus execution takes at least—"

"One hour. I have one hour." Cole checked the time. It was 6:15 AM. Wyatt would release the write lock tomorrow morning—specifically, 10 AM this morning. Less than four hours away.

"Can you do it in one hour?" he asked Quincy.

Quincy thought. "If I skip all queuing under unfair mode—yes."

"Then do it."

He hung up and dialed Meta.

This time, the transparent barrier turned translucent before he even spoke.

"I heard." Meta's voice came from within the barrier. "You want me to modify Donovan's type definition."

"Remove his platform-level guardian attribute."

"Do you know what that means?"

"The token becomes invalid. He loses the authority to modify foundational architecture types. His incremental updates become orphan data—the Attic's bottom layer will automatically clean up incrementals without a valid authorization source."

"The cleanup process takes time."

"How long?"

"Depends on the volume and complexity of incremental updates. Three years of accumulated increments—possibly thirty minutes to an hour."

"Not enough time. I need the cleanup done before Wyatt releases the write lock."

"Then that's impossible."

"Then accelerate the cleanup." Cole said. "You said the bottom layer automatically cleans orphan increments—is that cleanup serial or concurrent?"

Meta thought. "Serial by default. But it can be switched to concurrent—cleaning multiple increments simultaneously. The cost is higher resource consumption."

"I'll figure out the resource consumption. You just need to have concurrent cleanup mode ready. The moment Donovan's token goes invalid, launch concurrent cleanup immediately."

"I need at least five minutes to configure concurrent cleanup mode."

"You have it. Starting now."

The barrier flickered.

"Cole." A hint of warmth entered her voice for the first time. "Do you really believe all of this can be resolved in a single morning?"

"I don't believe it." Cole said. "It has to be."

The barrier went fully transparent. The spiral staircase's light waited inside.

"Come up." Meta said. "I need you to confirm the modification request in person. Proper procedure—can't skip it."

Cole stepped through the barrier.

Behind him, the Heap District commercial strip's lights flickered uncertainly in the predawn gray.

In the Old Generation's direction, cracks had spread from the ceiling to the walls.

Time was running out.
