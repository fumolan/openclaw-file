# Chapter 13: Secrets of the Old Generation

Vera's message came with six hours left on her one-day deadline.

"Found it. Come to the Old Generation entrance."

By the time Cole arrived, Vera was already waiting. She wore a dark red jacket and had her hair pulled back—the sign she was working in earnest.

"Let's go." She didn't waste words and led the way into the Old Generation.

The Old Generation was the Heap District's uppermost, oldest, most silent region. Walking its corridors, the air felt heavier than below. The buildings on either side loomed tall and hushed, like rows of silent giants. Each building housed long-lived objects—entities that had existed in Lockhaven for a long time, used repeatedly, never discarded.

But today's Old Generation was different.

Cracks had appeared in the buildings lining the corridor. Not hairline fractures—great rents cleaving entire walls. Through the gaps, the buildings' internal structures were visible: layer upon layer of reference chains, like coils of rope, binding the objects firmly in place.

"Running out of room." Vera said as she walked. "The Old Generation was designed to house long-lived objects—data that's used persistently, not easily discarded. But now, huge numbers of objects that don't belong here have been shoved in. They're taking up space meant for genuinely long-lived objects."

"The objects that don't belong—those are the leaked objects held in place by reference chains?"

"Right." Vera stopped at a half-open door. "Look inside."

Beyond the door stretched an enormous space. The ceiling was high but already cracking. In the center floated countless luminous spheres—each sphere representing one object. They ranged in size from fist to basketball.

Under normal conditions, these spheres would have been stationary—Old Generation objects don't move frequently. But now, the spheres were slowly rotating, jostling against each other, fighting for space.

"Look at the spheres with the red lines on them." Vera pointed at a cluster. "Those are the leaked objects."

Cole looked. Those spheres were visibly different—threaded across their surfaces were fine red lines. The lines extended from the spheres, passed through the ceiling, and vanished above.

"The red lines are strong references." Vera said. "Each line represents a reference relationship. Normal objects might have a few reference lines—indicating a few places using them. But look at those leaked objects—"

Cole counted carefully. The nearest sphere was wrapped in at least forty red lines. Those further away were worse—some spheres were so densely covered in red that their original color was invisible.

"They've been artificially loaded with references." Cole said.

"Exactly. And these references aren't random—they form a deliberately engineered structure." Vera pulled a compact projector from her pocket and opened a reference relationship map.

The map showed a complex network. At its center sat a node—the custom class loader. From it branched dozens of paths, each leading to a malicious type. Each malicious type branched further into the objects it had created. Each object sprouted reference lines pointing to other objects.

The entire network was a closed loop. Every reference line's endpoint pointed to another node within the network. Not a single line pointed to a normal object outside the network—which meant that when the cleaners performed reachability analysis, they would mark all these objects as "reachable," because they referenced each other internally, forming a self-sustaining ecosystem.

"The closed-loop design of the reference chains is remarkably clever." Vera said. "Normally, if an object has no external references, the cleaners mark it as reclaimable. But these leaked objects, while having no reference relationships with the outside world, reference each other internally—forming a dense reference web. Tracing reachability from GC Roots, these objects are all mutually reachable, so the cleaners consider them alive."

"But they're not alive. They've just been engineered to look alive."

"Right." Vera closed the projector. "That's the Old Generation's secret—it's not that the cleaners are malfunctioning. Someone is gaming the reachability analysis rules."

Cole gazed at the vast space filled with floating spheres. They rotated slowly, the red lines quivering. In the distance, more spheres were drifting in from the New Generation direction—newly promoted objects.

The space was visibly shrinking.

"There's one more thing." Vera's voice turned hesitant.

"What?"

"When I traced the red lines—the reference chains—back to their source, I found something unexpected." She pointed toward the ceiling. "All the red lines ultimately converge above. Not in the direction of the Metadata Attic—higher than that."

"Higher? What's above the Old Generation?"

"Direct memory." Vera said. "Above the Old Generation, at the very top of the Heap District, there's a region outside normal Heap District management. That's direct memory—space allocated directly, bypassing the Heap."

"What's in direct memory?"

"I don't know." Vera's tone carried a rare sense of helplessness. "Direct memory is outside my intelligence network. There are no normal reference relationships there, no standard object structures. I can't get in."

"Who can?"

Vera thought for a moment. "Nova. Her channel monitoring ability might be able to sense the data flows inside direct memory."

Cole filed that away mentally.

He took one last look at the space filling up with spheres. The Old Generation's capacity was nearing its limit. By Vera's estimate, it would be completely packed in another thirty-odd hours.

Then—Full GC.

"Vera, thank you."

"Don't thank me." Vera turned to leave. "Remember you still owe me."

"I know."

Vera reached the doorway and stopped.

"Cole—those three hundred forty-seven people not on the list." Her back was stiff. "I know where they are."

"Where?"

"Right here." She gestured into the Old Generation's interior. "They're among the spheres. Beside every leaked object stands a faceless thread person. They're maintaining references—every moment, their hands rest on the red lines, making sure the lines don't break."

Cole's fists tightened.

"Are they alive?"

"Alive. But they have no consciousness." Vera said. "They were created by the class-loading device—their sole purpose is to maintain references. They don't know what they're doing, don't know why they're doing it. They're just—"

"Tools."

"Yes. Tools." Vera's voice dropped. "But they're alive."

She left.

Cole stood alone at the Old Generation entrance, watching the faceless thread people moving among the spheres. Their movements were perfectly synchronized, like marionettes on the same strings.

Three hundred forty-seven living tools.

They didn't know they were tools. They didn't know the references they maintained were killing the city.

Cole closed his eyes.

In Lockhaven's rules, objects with references are alive. These three hundred forty-seven people had references, so they were alive. The objects they maintained had references, so those objects were alive too.

But being alive didn't mean being meant to live.

That distinction was Lockhaven's deepest contradiction.

In the distance, another crack appeared in the Old Generation's ceiling.

The light seeping through the crack was gray.
