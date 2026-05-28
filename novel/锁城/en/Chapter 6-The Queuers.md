# Chapter 6: The Queuers

Quincy's turf sat at the very bottom of the Heap District, near the exit to Stack Alley. There, a massive circular plaza opened up, and in its center grew an inverted tree—roots reaching skyward, crown pointing at the ground. It was Quincy's trademark and his desk.

Every root represented a wait queue. Small brass tags dangled from each root, every tag engraved with a thread person's ID and the resource they were waiting for.

When Cole arrived, the plaza was packed.

Not a dozen or twenty people—hundreds. They'd split into dozens of queues, each aligned with a root. The lines stretched from the center of the plaza all the way to the walls at the perimeter, winding around corners before vanishing into shadow.

"More people than usual," Cole murmured.

Jace hadn't come along—he was still staking out the Segment Three entrance. Cole had made this trip alone.

He threaded through the crowd toward the center. Most of the queuers looked haggard; some had been waiting a long time. A young thread person dozed against a wall, clutching a numbered brass tag. Cole glanced at it—the timestamp was two days old.

Two days waiting, still not served.

Cole picked up his pace.

Quincy sat in the heart of the tree's crown, leaning back against a thick root. Before him stretched an enormous crystal screen displaying real-time data for every queue: length, wait time, resource allocation.

Quincy was fifty, but he looked a decade older. His hair had gone entirely white, and the creases on his face might have been carved with a knife. Yet his eyes were the sharpest in all of Lockhaven—eyes that had witnessed countless queues, countless competitions, countless waits.

"Cole." Quincy didn't look up. "I knew you'd come."

"You did?"

"Your ID showed up in my queue yesterday." Quincy pointed to a line of small text on the screen. "Cole. Request type: information query. Priority: high. Estimated wait time—" He paused. "Never mind. You're here, so we'll skip the line."

Cole didn't stand on ceremony. He sat across from Quincy.

"I want to look up someone," Cole said. "No—not someone. A group. They've been accessing the Metadata Attic frequently, and they may be using a custom class-loading channel."

Quincy's fingers glided across the crystal screen. A stream of data cascaded into view.

"In the past week, total requests to access the Metadata Attic: three thousand seven hundred twenty-one." Quincy said. "Of those, about twenty-eight hundred came through normal channels. The remaining nine hundred-plus—" His fingers stopped. "Source unknown."

"What does 'source unknown' mean?"

"Exactly what it says." Quincy's tone didn't waver. "These requests passed authentication, entered the Attic, executed operations, and left. But their source identifiers are blank. Like someone walked in wearing a mask, did their business, and walked out."

"Doesn't your queue record the source of every request?"

"Under normal circumstances, yes." Quincy said. "But my queue only logs requests that pass through it. If someone skips my queue and goes straight into the Attic—"

"Then your queue has no record of them."

"Correct." Quincy looked at Cole. "But there is one loophole."

"What loophole?"

"Skipping my queue doesn't mean leaving no trace at all." Quincy's finger traced an arc across the screen. "My queuing mechanism isn't a wall—it's a net. Every request has to pass through a net node before entering the Attic. Normal requests get their node assigned through my queue. Abnormal requests may not queue up, but they still have to go through some node—and the nodes themselves keep logs."

Cole's eyes lit up. "You can find which nodes those abnormal requests passed through?"

"Yes." Quincy opened another page of data. "These are the abnormal request records matched from node logs. Look—" He pointed to a string of addresses on the screen.

Cole leaned in. Every abnormal request's address pointed to the same region.

"Segment Three." Cole said.

"Right." Quincy said. "Every single abnormal request entered the network through a Segment Three node."

Cole was silent for a few seconds.

"There's one more thing." Quincy's voice dropped even lower. "Some unfamiliar faces have started appearing in my queues."

"Unfamiliar?"

"People who've never shown up in my queues before. They appear out of nowhere and cut straight to the front—skipping everyone who's been waiting."

"Unfair insertion."

"You could call it that." A flicker of emotion crossed Quincy's face—not anger, but worry. "My queues have always run on a first-come, first-served basis. Fairness is the foundation of that system. But now someone's bypassing the rules and cutting in line."

"Those line-cutters came from Segment Three too?"

"I don't have proof." Quincy said. "But the timing lines up. The insertions started at almost exactly the same time as the abnormal requests from Segment Three."

Cole stood.

"Quincy, I need you to do something."

"Name it."

"If those line-cutters show up again—don't stop them. Let them cut. But I need you to track where they go after. What resources they take, where they head, what they do."

Quincy held Cole's gaze. "Aren't you worried they'll take something they shouldn't?"

"I am. But if I stop them from taking it, they'll never show up again." Cole said. "I need them to expose more of themselves."

Quincy was quiet for a moment, then nodded slowly.

"Cole," he called out as Cole turned to leave. "There's something you should know."

"What?"

"My queuing mechanism—it wasn't my own design." Quincy said. "Before me, there was a more fundamental set of coordination rules. Those rules don't belong to any individual; they're part of Lockhaven's infrastructure."

"You're talking about AQS?"

A flicker in Quincy's gaze. "You know about it?"

"Heard of it. Never seen it."

"The core of those rules is a state variable and a wait queue." Quincy said. "Every lock, every barrier, every semaphore—they all rely on the same underlying rules at their base. My queue is just one application of that system."

"What's your point?"

"My point is—if someone can bypass my queue, they've either found a vulnerability in my implementation, or they're manipulating those underlying rules directly."

"Manipulating the underlying rules? Who could do that?"

Quincy didn't answer. He simply glanced in the direction of the Metadata Attic.

Cole understood.

The only ones who could manipulate the underlying rules were those lowest-level type definitions—stored in the Metadata Attic, they were the blueprints of Lockhaven's infrastructure. If someone had tampered with those blueprints, they'd effectively tampered with Lockhaven's foundational rules.

"I'm going to see Donovan." Cole said.

"Careful." Quincy said. "Donovan is a shrewd man. Shrewd men don't reveal their hand easily."

"I don't need him to reveal his hand." Cole said. "I just need him rattled. Once rattled, he'll make mistakes."

He turned and merged into the crowd. Hundreds of queuers stood silently in their respective lines; occasionally someone murmured to a neighbor, but mostly there was only silence.

Cole crossed the plaza toward the exit.

Behind him, Quincy studied the data on his crystal screen. Those nine hundred-odd requests with no source, moving like ghosts between his queues and the network, coming and going as they pleased.

He turned his head to look at the inverted tree.

Brass tags covered every root, each tag representing someone waiting.

Today, there were dozens more tags than yesterday.

Quincy sighed.

More people queuing all the time, but the resources remained fixed. If the underlying rules had been tampered with, did queuing even mean anything anymore?

He had no answer.

But he knew Cole would go find one.

In the distance, in the direction of the commercial zone's west end, Donovan's sixteen segments operated like sixteen independent city-states, quietly ticking along.

Segment Three was the quietest of all.

But the quieter the place, the more likely it was hiding something.
