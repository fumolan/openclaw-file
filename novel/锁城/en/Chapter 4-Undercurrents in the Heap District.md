# Chapter 4: Undercurrents in the Heap District

Vera's hideout sat in the middle commercial strip of the Heap District—a transitional zone wedged between the New Generation area and the Old Generation area. Neither new nor old, cheap to rent, yet packed with more information per square foot than anywhere else in the city.

Cole arrived to find Vera behind a workbench buried under data fragments, an unlit cigarette dangling from her lips. She spotted him, plucked it out, and flicked it.

"Faster than I expected," she said. "Figured you'd dawdle until noon at least."

"Things won't wait."

"Sit." Vera gestured at the chair across from her. "I dug up some of what you asked for. But let's get one thing straight—this doesn't settle what you owe me."

"Fine."

Vera pulled a massive map from beneath the workbench and spread it across the surface. It was a panoramic view of the entire Heap District—from the Eden zone at the very bottom to the Old Generation area at the top, every region annotated with capacity, utilization rate, and object distribution.

She tapped the Old Generation area.

"Look here."

Cole leaned in. The Old Generation occupied the uppermost layer of the map, roughly a third of the Heap District's total area. Under normal conditions, its utilization should hover between sixty and seventy percent—long-lived objects took up permanent residence here, while the cleaners periodically reclaimed those no longer referenced.

But the number on the map made Cole frown.

"Ninety-three percent?"

"Yep." Vera's voice was unnervingly calm. "Old Generation utilization has surged from sixty-two to ninety-three percent in the past three days. And it's accelerating."

"What's causing it?"

"Object promotion." Vera drew an arrow on the map from the New Generation to the Old Generation. "Normally, objects in the New Generation that survive enough GC cycles get promoted to the Old Generation. But right now, huge numbers of objects are being promoted well below the normal age threshold."

"Who's lowering the promotion threshold?"

"Nobody's lowering it on purpose." Vera shook her head. "The New Generation can't hold. Look at Eden."

Her finger moved to the Eden zone at the bottom of the map. The figure showed Eden at ninety-eight percent utilization.

"Eden's about to overflow," Vera said. "When that happens, Minor GC in the New Generation fires constantly. Every cycle moves surviving objects from Eden into the Survivor spaces. But the Survivor spaces are full too—so survivors have nowhere to go but up, promoted early into the Old Generation."

Cole got it. Like an apartment building where the ground floor was packed, the stairwells crammed, and people who hadn't yet met the residency requirements were being forced into the upper floors ahead of schedule.

"So the root cause is too many objects in Eden?"

"Not exactly." Vera pulled another stack of papers from under the workbench. "These are the New Generation object creation logs from the past three days. Look at these entries."

She circled several lines with a red pen. Cole saw chains of creation records—type, size, timestamp, reference source.

"These object types—I've never seen them in the Heap District," Vera said. "Not standard types. Dynamically generated. Like someone drafted blueprints on the outside and found a way to inject them into the city."

"Dynamically generated types?" Cole's frown deepened. "Who could pull that off?"

"In Lockhaven, only two kinds of people can dynamically generate types." Vera held up two fingers. "First is Meta—she has full access to the Metadata Attic and can create new type definitions up there. But she'd never do something like this."

"And the second?"

"Custom class loaders." Vera's voice dropped low. "If someone built their own class-loading channel, bypassing Meta's review, and directly injected new types into the city from the outside—they could create unlimited objects."

Cole went silent.

Custom class loaders. In Lockhaven's rules, type information was loaded through a strict inheritance mechanism—Parents Delegate. Any class loader, before loading a new type, had to ask its parent whether it could handle it. If the parent could, the parent took over. Only if the parent couldn't would it fall to the child. This mechanism guaranteed type uniqueness and security.

If someone had bypassed Parents Delegate—

"How do you know these objects are dynamically generated?" Cole asked.

"Because their reference chains are abnormal." Vera flipped to the next page, which displayed a complex reference graph. Dozens of paths radiated outward from GC Roots, each one converging on the same node.

"All the anomalous objects—every reference chain ultimately points here." Vera jabbed the node. "But the node itself—I can't trace its origin. It's not an instance of any known type. It's as if it appeared out of thin air."

"Out of thin air?"

"In Lockhaven, nothing appears out of thin air." Vera paused. "But if someone created this object using a class loader that isn't in the system, then as far as Lockhaven is concerned, it did appear out of thin air—because it never went through the normal type-loading process."

Cole stared at the reference graph. Every lead pointed in the same direction: someone outside the city, through an illegal class-loading channel, was pumping massive amounts of anomalous types and objects into Lockhaven. These objects held strong references to Old Generation space, preventing the cleaners from reclaiming it. Space was being devoured, GC frequency climbing, pauses growing more frequent.

"Vera." Cole looked up. "Those shadows you mentioned—shadows moving during the pauses—did you see them yourself?"

Vera hesitated.

"Not with my own eyes. Someone told me."

"Who?"

"An Old Generation resident. Goes by Wei Aqi. Distant relative of Warden, the cleaner. He's lived in the Old Generation for years—pauses are routine for him. But he said the recent ones feel different."

"How?"

"He said that inside the gray ripples of the pauses, he sensed movement that wasn't his. Not the cleaners—he could distinguish their movement blindfolded. He said it was human movement. Fast, precise, purposeful. And more than one person."

Cole's pulse quickened.

"Is he still alive?"

"Don't know." Vera's expression darkened. "After the pause early this morning, I lost contact with him."

Another disappearance after a pause.

Cole stood.

"Vera, I need you to do something."

"Name it."

"Keep tracing that anomalous node's reference chain. No matter where it leads, I want to know its final destination."

Vera nodded. "Give me two days."

"One."

Vera rolled her eyes. "Fine. One day. But you have to promise me one thing."

"What?"

"If the trail leads to the Metadata Attic—you go ask Meta yourself. She and I don't get along."

Cole didn't answer. He looked at the anomalous node circled in red on the map and already knew the truth.

Not "if."

It would definitely lead to the Metadata Attic.

In Lockhaven, only two people could create new types: Meta, and whoever possessed a custom class loader. If Meta hadn't created the anomalous objects, that meant someone had built an illegal type-loading channel right under Meta's nose.

And the only place such a channel could be built was the Metadata Attic.

Cole stepped out of Vera's hideout and paused on the walkway of the Heap District's commercial strip, tilting his head back.

Full daylight now, but the sky above the Heap District was perpetually that indescribable grayish white—like gauze stretched overhead, or something higher up blocking the light.

The Old Generation sat at the very top of the Heap District. Looking up from below, Cole could see dark cracks spreading along its lower edge—a telltale sign of insufficient space. They were widening slowly, like a riverbed running dry.

What would happen if the Old Generation filled completely?

A city-wide pause. Total. Irrecoverable. The cleaners would trigger a Full GC—not a localized mark-and-sweep, but a comprehensive scan and compaction of the entire Heap District. That pause would be measured in minutes. Maybe longer.

The people who vanished during a pause like that wouldn't number eleven.

It would be hundreds. Thousands.

Cole quickened his pace.

He needed to see Donovan. Not tomorrow. Not this afternoon.

Now.
