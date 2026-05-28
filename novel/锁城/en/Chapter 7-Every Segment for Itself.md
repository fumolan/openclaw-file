# Chapter 7: Every Segment for Itself

Donovan's commercial zone was divided into sixteen segments—the most distinctive architectural complex in Lockhaven.

From the outside, it looked like a chocolate bar snapped into sixteen pieces. Each piece was an independent area with its own passageways, its own security, its own operating rules. Thick partition walls separated the segments, pierced only by narrow interconnecting doors at specific points. Each door bore a lock whose grade depended on the segment's traffic volume.

Segments One through Five formed the commercial strip's core, fitted with the heaviest locks—heavyweight locks. Those corridors saw constant queuing and fierce contention; nothing short of heavyweight locks could keep order.

Segments Six through Twelve were moderately busy, equipped with lightweight locks. The lock faces flickered occasionally, signaling competition, but most of the time a single CAS got you through.

Segments Thirteen through Sixteen formed the outermost ring, fitted with biased locks. Few people visited these segments normally; the biased locks were essentially ceremonial.

Segment Three was part of the core zone. Heavyweight lock.

But when Cole reached the Segment Three entrance, he noticed something off.

The passage leading into Segment Three was empty.

Not sparse—deserted. Not a soul in sight.

A passage guarded by a heavyweight lock should have had thread people queued up waiting to get through. But the entrance to Segment Three was completely barren, not even a loiterer in sight.

"Nobody?" Jace stepped out of the shadows. "I've been staking this out all morning. At least twenty groups came to the Segment Three entrance, but not one of them went in. They took one look and left."

"Why?"

"Check the lock at the entrance."

Cole walked to the Segment Three entrance and studied the heavyweight lock carefully. The lock face was normal—no signs of tampering. But above it, a small metal plaque had been mounted. Four characters were engraved on it:

"Under Renovation."

Cole blinked.

"Under Renovation" was Lockhaven's official designation, meaning the area was temporarily closed and off-limits. But Donovan's sixteen segments had never posted a renovation notice—Donovan's segments were the most stable, most punctually run commercial zone in the city. He wouldn't shut one down without good reason.

"When did this plaque go up?" Cole asked.

"Three days ago." Jace said. "I asked the merchants nearby. They said it appeared suddenly. No advance notice to anyone."

Three days ago. The moment everything started going wrong.

Cole reached out and touched the plaque. Metal, finely crafted, with Donovan's family crest along the edge—an interlocking chain motif. Not a forgery.

But the message was wrong.

"Donovan wouldn't close Segment Three." Cole said. "It's one of his core zones, highest profit margins. He'd have to be out of his mind."

"So the plaque—"

"Is real. But Donovan didn't put it up." Cole's finger traced the edge of the plaque. "Or Donovan put it up, but not of his own free will."

He pulled his hand back and stared at the sealed passage door. The heavyweight lock held the entrance firm; without a key or lock-cracking expertise, nobody was getting in.

"Did you try?" Cole asked Jace.

"Tried CAS. No good." Jace shook his head. "Heavyweight locks don't go through the CAS channel—they go straight through the operating system's mutex mechanism. My CAS can't outrun a kernel-level lock."

"Then we go around."

"Go around? Segment Three is walled on all four sides. This is the only entrance."

"Cut through an adjacent segment." Cole said. "Segments Two and Four both share partition walls with Segment Three. If there are interconnecting narrow doors in those walls—"

"There are." Jace said. "But those doors have locks too."

"What grade?"

"Lightweight."

Cole looked at Jace. Jace immediately caught his meaning and grinned.

"You want me to CAS my way through?"

"Not break through. Pass through normally." Cole said. "Lightweight locks use the CAS channel. You're the fastest CAS operator in the city."

"Depends on contention." Jace flexed his fingers. "If the narrow door's unused, one CAS does it. If someone's using it—"

"Segment Three is under renovation. Nobody should be coming or going during renovation. If the CAS fails on the other side—it means someone's in there."

Jace's eyes lit up.

The two circled around Segment Three's exterior wall and entered Segment Four. Segment Four was moderately busy, with a steady trickle of people. Cole noticed that the thread people in Segment Four walked with deliberate care to avoid the partition wall shared with Segment Three, as though something unclean clung to it.

The narrow door in the partition wall did indeed bear a lightweight lock. The lock face was clean, no signs of contention—nobody had used this door in a long time.

Jace took a deep breath and pressed his palm to the lock face.

The CAS operation began.

Cole watched from the side. He could read Jace's progress from the micro-movements of his hands—every CAS consisted of three steps: read current state, prepare replacement data, execute compare-and-swap. Jace's read was blisteringly fast, almost instantaneous the moment his skin touched the lock.

First CAS—the lock face trembled slightly.

Failed.

"Someone's here." Jace whispered, brow tight. "The lock face's state changed between my read and my swap. Something inside is operating this lock."

"Again."

Second CAS.

Failed again.

"It's looping." Jace's speech sped up. "It's modifying the lock face every few seconds. My CAS keeps hitting its modification window."

"Can you dodge it?"

"Need precise timing." Jace closed his eyes, hand still pressed to the lock face. He was feeling the opponent's rhythm—the interval between modifications, the duration of each change.

Five seconds.

The operation interval was roughly five seconds.

Jace opened his eyes. "Next five-second window. I'll count to three. Together."

Cole nodded.

Jace's fingers drifted lightly across the lock face, feeling the opponent's cadence. One, two, three—

Third CAS.

A soft click from the lock face.

Open.

The narrow door slid inward, revealing a gap barely wide enough for one person. Beyond it: pitch black.

Cole squeezed through first.

Inside, Segment Three was a different world. From the outside, it was a "renovation" zone—sealed and dormant. But stepping in, Cole beheld something else entirely.

The passage walls on both sides were embedded with glowing data cables, densely intertwined like blood vessels. Through them flowed a fast-moving light—not the normal glow of data transmission, but something darker, denser.

"This isn't renovation." Cole said softly. "It's construction. Someone is building a new system inside Segment Three."

Jace squeezed in behind him and froze at the sight.

"These data cables—" He reached out to touch the nearest one and yanked his hand back immediately. "They're transmitting class definitions."

"What?"

"Class definitions. The raw blueprints of type information." Jace's face went pale. "Someone is using these cables to inject new types into Lockhaven. Massive, continuous injection."

Cole followed the cables' path with his eyes. They all converged at Segment Three's center—where a door stood. No lock on it, but a symbol was carved into the doorframe.

Cole recognized it.

It represented "class loading"—the gateway through which type information entered Lockhaven from the outside.

The door was open.

Light spilled from within, making Cole squint instinctively. Through the glare, he made out a massive machine—or rather, a device. It hummed steadily, and with each pulse, a new batch of data was sucked in from the outside, translated into type information Lockhaven could understand, and dispatched through the data cables to every corner of the city.

"Custom class loader." Cole's voice came through clenched teeth.

In the heart of Segment Three, deep inside Donovan's commercial zone, someone had built a complete custom class-loading channel. It bypassed Meta's review, bypassed the Parents Delegate inheritance rules, and directly injected new types into Lockhaven from the outside.

Those types spawned hordes of objects holding strong references, stuffing the Old Generation full.

This was the root of everything.

Cole stood before the door, watching the class-loading device churn inside the light. He didn't rush in—because next to the device stood a figure.

The silhouette was familiar. Broad shoulders, gray-white hair, ramrod-straight posture.

Donovan.

"I should have known it was you." Cole said.

Donovan turned. His expression wasn't that of a criminal caught red-handed—it was that of a host who'd been waiting a long time.

"Cole." Donovan smiled. "You got here a day earlier than I expected."

"You've been injecting malicious types into Lockhaven." Cole's voice was level, but his hand had already drifted to the lock tools at his belt.

"Malicious?" Donovan's smile deepened. "Cole, how do you define malicious? The types I inject are all valid type definitions. They've gone through the complete loading, linking, and initialization process. The objects they create all have normal reference relationships. The cleaners don't reclaim them not because they're unreachable—because they're still alive."

"You fill the Old Generation with objects that serve no one, then claim they're alive?"

"To a system, having references means being alive." Donovan's tone was as matter-of-fact as if he were reciting a law. "Haven't you always preached the importance of references? Objects with references shouldn't be reclaimed. I'm simply ensuring they all have them."

"By tampering with reference counters."

"By creating references for them." Donovan corrected. "The counter is just a tool. The real key is the types themselves—I designed perfect reference chains for them. From GC Roots to every object, the reference relationships are complete, closed loops, unbreakable."

Cole finally understood why the cleaners couldn't reclaim those objects. The cleaners weren't malfunctioning—the objects' reference chains had been artificially engineered into structures that would never break.

"Why?" Cole asked.

Donovan's smile vanished. A complex expression took its place—anger, resentment, and something else Cole hadn't seen before.

"Because Lockhaven is running out of room." Donovan said. "The Heap District has limited capacity. Thread people keep increasing, object creation keeps accelerating. One day, the Old Generation will fill up. And when that happens—"

"When that happens, what?"

Donovan met Cole's eyes.

"When that happens, the cleaners will trigger a Full GC. City-wide pause. Not minutes—maybe tens of minutes. The people who vanish during a pause like that won't number eleven. It'll be hundreds. Thousands."

"So your solution is to—fill up the Old Generation yourself?"

"My solution is to prove that this system can't hold." Donovan's voice went low. "If I don't accelerate the process, everyone will sleepwalk toward that ending. By making the Old Generation fill up early, by showing everyone the horror of a Full GC—they'll finally take change seriously."

Cole was silent for a long time.

"You made eleven thread people disappear to prove a point."

Donovan said nothing.

"You nearly brought the entire city to its knees to prove a point."

Donovan still said nothing.

Cole looked away from him and back at the still-running class-loading device. Its hum reverberated through Segment Three's sealed space like the heartbeat of a bomb about to detonate.

"Shut it down." Cole said.

"Can't." Donovan shook his head. "Once this device is activated, it runs continuously until all type definitions are fully loaded. Forcibly interrupting it would crash the class loader—and a class loader crash would cascade to every type that's already been loaded."

"You mean if I shut it down, all the types that were injected would—"

"Not would—would crash. The type information would be incomplete. Objects created from those types would exhibit unpredictable behavior." Donovan said. "Including broken reference chains, memory access exceptions, even—"

"Even what?"

Donovan's gaze slid away.

"Even a cascading collapse. The Heap District's structure would be destroyed. The entire city—"

He didn't finish.

Cole stared at Donovan's back. Donovan was gambling. He'd wagered the entire city's safety to bet that the crisis he manufactured would force everyone to change.

"Donovan." Cole's voice went cold. "You've lost your mind."

In the corridor, the class-loading device's hum grew louder.

The floor of Segment Three began to tremble.
