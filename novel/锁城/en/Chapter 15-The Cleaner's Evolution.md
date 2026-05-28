# Chapter 15: The Cleaner's Evolution

Warden didn't go straight to battle readiness. Before making the final call, he brought Cole to the cleaners' headquarters—a subterranean space hidden beneath the Old Generation's lowest layer.

"Let me show you my evolution." Warden said. "So you know cleaners aren't some unchanging fossils."

The underground space was vast, divided into three zones. Each displayed a different cleaning method and equipment set.

The first zone was the oldest. Mounted on the wall was a gray-white uniform with "Serial" stitched across the chest. Beside it hung a heavily worn marking wand—the original model.

"This was the earliest cleaning method." Warden pointed at the uniform. "Serial—serial sweeping. One cleaner, one task at a time. Mark, then sweep. Sweep, then compact. City-wide pause; everyone waits."

"Low efficiency?"

"Very low. But simple." Warden said. "No complex data structures to maintain, fast initialization. When Lockhaven was first built, there were few thread people, few objects. Serial sweeping was enough."

"And then?"

"The city grew. More thread people, more objects. Serial sweeping pauses stretched from seconds to minutes, from minutes to tens of minutes." Warden moved to the second zone. "So we evolved."

The second zone was much larger. Three uniforms hung on the wall—white with blue trim, white with red trim, white with green trim. The equipment beside them was far more complex: multiple marking wands, multiple scanners, and a large synchronization coordinator.

"Concurrent sweeping." Warden said. "Cleaners operate simultaneously with normal city operations. No more city-wide pauses—we sweep while the city runs."

"How?"

"The marking phase can run concurrently with city operations." Warden pointed at the coordinator. "While we scan objects, thread people can continue their activities. They can create new objects, modify reference relationships. But this introduces complexity—if thread people modify references while we're marking, our earlier marks may become invalid."

"How do you handle that?"

"Incremental updates and remarking." Warden said. "First, an initial mark—this phase is brief, only marking objects directly referenced by GC Roots. Then a concurrent mark—while cleaners and the city operate simultaneously, we trace all reachable objects along their reference chains. Finally, a remark—correcting any reference changes that occurred during concurrent marking."

"Sounds much more complex than serial."

"Far more complex. But pauses are shorter." Warden walked to the third zone.

The third zone didn't display uniforms and equipment like the previous two. Instead, a massive holographic map dominated the space—a panoramic view of the Heap District, divided into equal-sized small squares.

"This is the latest." Warden said. "Regional sweeping."

Cole studied the map. Each small square represented an independent region. The squares were color-coded—green for free, blue for in-use, red for needing cleanup.

"The entire Heap District is divided into many small regions." Warden said. "We no longer sweep the entire Heap at once—we go region by region. Each time, only a region-sized space pauses; everything else keeps running."

"Pause duration?"

"Controllable." Warden said. "We can set a target pause time. The cleaners automatically adjust the number of regions swept per cycle and the strategy to hit that target."

"Sounds perfect."

"It's not." Warden shook his head. "Regional sweeping costs more memory overhead and requires more complex data maintenance. And—regional sweeping still can't solve the fundamental problem."

"What fundamental problem?"

"The leaking bucket I mentioned." Warden pointed at the red squares on the holographic map. "Those red regions are space occupied by leaked objects. No matter what method I use, if the leaked objects' reference chains hold, I can't sweep them away. My methods evolved from serial to concurrent to regional—efficiency increased by tens of times. But what I can't sweep, a thousand times more evolution still won't sweep."

He turned to face Cole.

"So you understand why I'm willing to try your plan. Because cleaning isn't the answer. Cleaning is just symptom management. The real answer—"

"Is plugging the leak."

"Exactly." Warden said. "Shut down that class-loading device. Sever that 'maintain references' channel. Let the reference chains return to normal. Once that happens, no matter which cleaning method I use, I can clear out the garbage."

Cole looked at the holographic map. Red squares dominated the Old Generation's area—like infected skin. The New Generation was starting to show red too—leaked objects were spreading into younger regions.

"Warden." Cole said. "How long have you been a cleaner?"

"Forty years."

"In forty years, what was the worst leak you've seen?"

Warden thought for a moment. "Fifteen years ago. A framework didn't properly release references while loading dynamic types, filling the Old Generation with废弃type information. That Full GC paused for twelve minutes. Seven people vanished."

"Seven people."

"Yes." Warden's voice sank. "I remember every one of their names to this day."

"And this time—if Full GC pauses for half an hour—"

"I won't let it happen." Warden cut him off. "Even with only a thirty percent chance. I'm going to try."

His gray eyes shone with determination in the underground space's dim light.

"Tomorrow morning." He said. "I'm ready."

Cole nodded once and turned toward the exit.

Halfway there, he stopped.

"Warden."

"Yeah?"

"In all your years as a cleaner—have you ever done anything besides cleaning during pauses?"

Warden's back stiffened.

"What do you mean?"

"Meta said there are no more than five people in the city capable of guiding the bootstrap level. You're one of them." Cole's voice was calm, but every word drove into the air like a nail. "You're the only one active during pauses. If you wanted to do anything—anything—no one would see."

Warden slowly turned around.

"Are you suspecting me?"

"I'm eliminating possibilities." Cole said. "Tell me you only clean during pauses and do nothing else."

Warden looked at him. A long silence.

"I only clean during pauses." He said. "Forty years. Never once different."

Cole held his gaze for five seconds.

"I believe you." He said.

Then he left.

Warden stood alone, watching Cole's silhouette disappear into the light at the exit.

He looked down at his own hands. Cleaner's hands—hands that had marked countless objects and swept away countless spaces for forty years.

Clean hands.

He clenched his fists and turned back to the holographic map.

The red squares were blinking.

Tomorrow morning, he would lead his cleaners into an operation they'd never attempted before.

Not for cleaning.

But to buy Cole those few seconds of window.

Those few seconds would decide everything.
