# Chapter 16: The Truth of Segment Three

Cole entered Segment Three for the second time at four in the morning.

This time he wasn't alone—Jace and Nova had both come. Jace to prepare for the critical CAS operation, Nova to monitor the five hidden channels in real time.

"Situation's changed." Nova murmured into her comm unit. "The red channel—the one sending 'maintain references' instructions—its frequency is increasing. From once every eight seconds to once every five."

Cole frowned. "Does it know we're coming?"

"Not necessarily. It could be an acceleration response to Old Generation space pressure—the class-loading device is straining to maintain more references, preventing leaked objects from collapsing under spatial stress."

"Or it's because of Wyatt's write lock." Cole said. "While Wyatt holds the write lock, the anomalous write window is closed. The class-loading device has a backlog of unexecuted write operations. When Wyatt releases the lock tomorrow morning, the backlog will flood in all at once. The device is preparing for that."

"Which means my CAS window is even smaller." Jace said.

"Right." Cole said. "Which is why we have to finish preparation tonight."

The three slipped through the narrow door in Segment Four and entered Segment Three's interior. The data cables along the corridor walls were denser than last time—the light flowed faster too. The class-loading device was running at full capacity.

When they reached the device's chamber, Donovan wasn't there.

"He left?" Jace was surprised.

"Probably went to rest." Cole said. "I cornered him here during the day; he has to go back sometime. He's still managing fifteen other segments in his commercial zone."

Cole walked up to the class-loading device and studied its structure carefully. The device was a cylinder three meters tall, its surface covered with glowing runes—encodings of type definitions. At the top, a rotating lens spun continuously; each revolution sucked in a new batch of type data from the outside.

"This is the custom class loader." Cole said.

Jace circled the device and crouched to examine its base. "The base connects to a massive number of data cables. They split in two directions—one set goes down, connecting to the Old Generation; the other goes up, through the ceiling, connecting to—"

"Direct memory and the Metadata Attic." Nova finished, eyes glued to her monitoring screen. "I can see them. Two of the five hidden channels originate from this device. One routes through direct memory to the Metadata Attic's bottom layer—that's the channel injecting foundational architecture type definitions. The other routes through the Old Generation back to this device—that's the maintain-references feedback loop."

"Feedback loop?"

"Right. The device sends reference-maintenance instructions, the leaked objects in the Old Generation receive them and send confirmation back. The confirmation signal travels through this loop back to the device, triggering the next round of instructions."

"Closed-loop control." Cole murmured.

"If I could cut the feedback loop—" Nova started.

"Can't cut it." Cole said. "A sudden break in the feedback loop would be detected by the device. It would switch to a backup channel within milliseconds."

"Then what?"

"Modify it." Cole said. "Don't cut—change. Replace the confirmation signal in the feedback loop with 'references broken.' Make the device think references have already snapped—it'll automatically reduce instruction frequency, or stop sending entirely."

"But the leaked objects' references are actually still there." Jace said.

"Right. But the device won't know that. It thinks references are broken, so it stops maintaining them. Once maintenance stops, the reference relationships will gradually decay naturally—and the cleaners can reclaim them."

"This modification—is that also a CAS?"

"Has to be CAS." Cole said. "The confirmation signal in the feedback loop changes continuously during transmission—communication between the device and the leaked objects is continuous. To replace the confirmation signal, you have to complete compare-and-swap in a single instant of signal transmission. Only CAS can do that."

Jace took a deep breath. "Let me see the feedback loop's data structure."

Nova projected the feedback loop's data stream from her monitoring screen onto the device's surface. Jace crouched and scanned the flowing data like reading sheet music.

"The confirmation signal format is simple—a hex value, fixed at 0xAA." Jace said. "Every feedback round is 0xAA. I need to change it to 0x00—references broken."

"How often does the signal transmit?"

"Every five seconds."

"You have a five-second window."

"Not five seconds." Jace shook his head. "The confirmation signal only exists in transmission for about two hundred milliseconds. I have to complete the CAS within two hundred milliseconds—read the current value (should be 0xAA), compare (confirm it's 0xAA), replace with 0x00."

"Two hundred milliseconds enough?"

"For me, yes." Jace flexed his fingers. "But the issue isn't time—it's position. The feedback signal isn't at a fixed address; it's flowing through the data cable. I have to precisely catch it at the node it passes through and complete the CAS at that node."

"Nova can help you locate the node."

Nova nodded. "I can track the feedback signal's real-time position in the data cable. When the signal reaches the nearest node, I alert Jace."

"Notification delay?"

"I can keep it under ten milliseconds."

"Plus CAS operation time—"

"Total under fifty milliseconds." Jace said. "Well within the two-hundred-millisecond window."

Cole looked at the two of them. One for positioning, one for execution. A team.

"There's one problem." Cole said. "The device might have a verification mechanism for feedback signal modifications. If I change one confirmation signal and the device notices it's wrong—"

"It might immediately switch to a backup channel." Nova said. "Or worse—enter self-preservation mode and accelerate loading all remaining types."

"So we can't just change it once." Jace said. "We have to change it continuously. Replace every feedback round's 0xAA with 0x00. Make the device receive 'references broken' feedback consistently. After sustained periods, it'll conclude all references have failed and stop maintaining automatically."

"How many rounds would that take?"

"Based on the feedback loop's design—about thirty rounds. Every five seconds per round. Thirty rounds is—"

"Two and a half minutes."

"Two and a half minutes of continuous CAS. Thirty times. Each in a two-hundred-millisecond window."

Cole looked at Jace.

"Can you do it?"

Jace grinned. "I've done harder."

"When?"

"Never." His grin widened. "But there's always a first time."

Cole didn't smile. He turned to Nova.

"Tomorrow morning, starting the moment Wyatt releases the write lock. You handle positioning, Jace handles CAS. I handle—"

"You handle what?"

"I handle keeping Donovan occupied."

Nova and Jace looked at him simultaneously.

"Donovan will come?" Nova asked.

"Definitely." Cole said. "Tomorrow morning when Wyatt releases the write lock, the anomalous write window reopens. Donovan has been waiting for this window all day. He won't miss it."

"You're taking him on alone?"

"I'm enough alone."

Jace and Nova exchanged a glance. They knew Cole's lock expertise—biased locks, lightweight locks, heavyweight locks, he'd mastered them all. But Donovan wasn't an ordinary person. He managed a commercial empire of sixteen segments; his cunning and calculation were beyond what most people could fathom.

"Be careful." Jace said.

"You too."

The three withdrew from Segment Three. Jace and Nova returned to their respective positions for final preparations. Cole walked alone toward Stack Alley.

Dawn was approaching.

Tomorrow morning—no, this morning—was the decisive moment.

Cole walked across the empty Heap District commercial strip. He glanced up at the Old Generation.

More cracks. Dark red light seeped through the fissures, like blood.

He quickened his pace.

Behind him, Segment Three's entrance closed silently in the morning light.

The "Under Renovation" plaque still hung on the door.

But after tonight, that plaque wouldn't hang anymore.

Either Segment Three would return to normal.

Or—the entire city would go under renovation.
