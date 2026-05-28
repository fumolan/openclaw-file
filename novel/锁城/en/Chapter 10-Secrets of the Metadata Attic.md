# Chapter 10: Secrets of the Metadata Attic

The Metadata Attic sat at Lockhaven's highest point.

Looking up from the Heap District's commercial strip, it resembled a tower suspended in the gray canopy—cold, silent, cut off from the world. The Attic's base was supported by countless data cables, dense as a spiderweb, connecting to every corner of the city.

These cables didn't carry ordinary commercial data. They transmitted type information—the most fundamental, most core data in all of Lockhaven. Every thread person's capability definition, every object's construction blueprint, every rule's implementation logic—all of it was stored in the Metadata Attic.

Cole had never been here before. Not because he hadn't wanted to—but because he couldn't.

The Metadata Attic had only one entrance, and the door bore no lock. In its place was a transparent barrier—only those approved by Meta could pass through.

Cole stood before the barrier and waited three minutes.

Nothing happened.

"Meta." He spoke toward the barrier.

No response.

"My name is Cole. I'm here about the class-loading channel."

Still no response.

Cole was about to speak a third time when the barrier suddenly turned translucent. Through it he could see a spiraling staircase ascending into a warm glow.

"Come up." A voice drifted from within the barrier. Cool, composed, like wind gliding across ice.

Cole stepped through the barrier.

The spiral staircase was far longer than it appeared from outside. With every step, text or images materialized on the walls alongside him—fragments of type definitions. Some of the text he recognized; some he'd never seen. They were like pages of an open book, each one a piece of Lockhaven's infrastructure.

After about five minutes of climbing, the staircase ended.

Meta sat behind a floating worktable. She looked to be around thirty, features refined but remote, draped in a silver-gray robe. Before her stretched an enormous semi-transparent screen displaying countless parallel data streams.

"Sit." She gestured at the chair opposite.

Cole sat. He noticed a heavy tome resting at the edge of the worktable—its cover bore a symbol he recognized: Parents Delegate.

"You knew I was coming." Cole said.

"You found the class-loading device in Segment Three." Meta wasn't asking—she was confirming.

"You already knew about it?"

"I knew someone was building a custom class-loading channel." Meta's voice was flat. "Three months ago I detected the first non-standard class-loading request. It hadn't gone through my review, and it hadn't followed the Parents Delegate inheritance path."

"Three months ago? Everything was normal then."

"It wasn't normal. You just hadn't noticed yet." Meta pulled up a data set on her screen. "Look—three months ago, type registration volume in the Metadata Attic suddenly jumped seventeen percent. All the new types were valid—correctly formatted, structurally sound, passing verification. But their origins weren't in my records."

"And you didn't investigate?"

"I did." Meta said. "But the Parents Delegate rules limit my authority."

That made Cole frown.

Parents Delegate—when loading types, ask the parent first. If the parent can handle it, the parent takes over. Only if the parent can't does it fall to the child. This was Lockhaven's fundamental type-loading inheritance rule.

"You're the guardian of the Metadata Attic. Don't you have the highest authority?"

"No." Meta shook her head. "I'm the application-level guardian. Above me are the platform-level guardians—and above them, the bootstrap-level guardians. The Parents Delegate rule is: every class-loading request goes to the bootstrap-level guardian first. If the bootstrap level can handle it, no need to pass it down. If it can't, it goes to the platform level. And only if the platform level can't handle it does it reach me."

"So Donovan's class-loading channel—"

"Donovan's custom class loader bypassed all three of our levels." A trace of emotion crept into Meta's voice—not anger, but resignation. "He created an independent class loader from the outside. It doesn't belong to any of the three levels, so it never comes through my review."

"How is that possible? A class loader has to be mounted under one of the levels to function."

"Normally, yes. But if someone—" Meta paused. "If someone modified the definition of the class loader itself, so it doesn't need to be mounted under the three-tier architecture—"

"Modified the class loader's definition?" Cole's heart sank. "Who has the authority to modify the class loader's definition?"

Meta looked at him.

"The definition is stored in the Metadata Attic." She said. "But not in a region I can access."

"What do you mean?"

"The Metadata Attic has many layers. I guard the application layer—which stores the type definitions thread people use daily. But the Attic's deepest layer—which stores the foundational architecture type definitions—is outside my jurisdiction."

"Who manages that layer?"

"No one." Meta said. "Or rather, no one has touched it since Lockhaven was founded. It's read-only. The foundational architecture type definitions—including the class loader's own definition—were hard-coded when Lockhaven was established. Theoretically impossible to modify."

"But Donovan did."

"Yes." Meta's voice dropped even lower. "Which means Donovan didn't do this alone. Modifying foundational architecture type definitions requires extremely high privileges—far beyond his authority as a commercial zone segment manager. He must have had help."

"What level of help?"

"At least platform level or above." Meta said. "Possibly even—bootstrap level."

Bootstrap level. The topmost tier of Lockhaven's class-loading architecture. It governed the most core, most fundamental type definitions.

"Who's the bootstrap-level guardian?"

Meta was silent for a few seconds.

"There isn't one." She said. "The bootstrap level runs automatically. It's been self-operating since Lockhaven was founded—no human management required."

"An automated system doesn't make mistakes."

"It doesn't. But it can be guided." Meta's gaze shifted to the screen. "If someone knows the bootstrap level's operating parameters—knows when it loads, what it loads, how it responds to requests—they can craft inputs that guide the bootstrap level toward specific behaviors. No need to modify it directly—just make it believe certain operations are normal."

Cole understood. Like not picking a lock, but using the right key—except the key was forged.

"Do you know who has that kind of capability?"

"No more than five people in the entire city." Meta said. "I'm one of them."

Cole looked at her. "Would you do something like this?"

"No." Her answer was crisp. "But I can't guarantee the other four wouldn't."

"Who are the other four?"

"Quincy, for one. He manages the underlying queuing mechanism—he knows the system parameters inside out."

"He wouldn't. He cares about fairness more than anyone. Tampering with the underlying rules is the last thing he'd tolerate."

"That leaves three. Slater, Donovan—"

"Donovan's already exposed. The fourth?"

Meta's silence stretched a long time.

"Warden."

Cole's breath caught.

Warden. Head of the cleaners. The only entity in the entire city that remained active during pauses.

"You're saying—Warden might have guided the bootstrap level?"

"I said I'm listing people with the capability." Meta said. "I have no evidence against anyone. But Cole—have you considered something?"

"What?"

"The shadows moving during pauses." Meta held his gaze. "You've been looking for people active during pauses. You assumed they were Donovan's people. But the cleaners are the only ones legally active during pauses. If the cleaners themselves are doing things they shouldn't—who would notice?"

Cole stood.

"Thank you for telling me this."

"Cole." Meta called after him. "There's something you must know."

"What?"

"Donovan's class-loading device can't be forcibly shut down." Meta said. "I've scanned its structure. It's already loaded over two thousand new types. Instances of those types are distributed across every corner of the Heap District—New Generation, Old Generation, even direct memory areas. If the class loader crashes, those type definitions will enter an incomplete state. Every object created from them—"

"Will have problems."

"Not just problems. Unpredictable behavior." Meta's voice carried a gravity rarely heard from her. "Some objects might suffer reference breaks, worsening the memory leak. Others might generate incorrect references, pointing to data they shouldn't access. Worst case—cascading collapse. One object's abnormal behavior triggers another's, layer after layer, until the entire city's data structure collapses."

"Then how do we fix it?"

"The correct approach: first purge all objects created from the malicious types, let the cleaners reclaim them normally. Then unload the malicious types themselves."

"But you said the reference chains were engineered to be unbreakable—the cleaners can't reclaim them."

"Which is why you need to find the origin of the reference chains—the custom class loader itself." Meta said. "The class loader is the starting point of all malicious types and objects. If you can stop it from loading new types while gradually severing the existing objects' references to the class loader—the cleaners can reclaim them step by step."

"Step by step? How long?"

"Depends on the reference chains' complexity." Meta said. "Optimistically—three days. Pessimistically—"

"How long?"

"Not enough time."

Cole looked into Meta's cold eyes. She wasn't exaggerating.

"The Old Generation will fill faster than three days." Meta said. "At the current expansion rate, it'll hit one hundred percent within forty hours. When that happens—"

"Full GC."

"City-wide pause. Not minutes. Possibly up to half an hour."

Cole turned toward the staircase.

"Cole." Meta's voice came from behind him.

He stopped.

"If you need my help—" She paused. "You'll need to follow proper procedure. Submit a request through Quincy's queue. My Attic doesn't accept private commissions."

"I know."

"And—watch out for Warden."

Cole didn't look back. He hurried down the spiral staircase, through the transparent barrier, and back into the Heap District's commercial strip.

The night wind hit him, cold enough to bite.

He looked up toward the Attic—the suspended tower glowed like a lone star in the darkness, its light cold and unwavering.

Forty hours.

He had to stop the Full GC within forty hours.

Otherwise Lockhaven would face the longest pause in its history. The people who vanished during that pause wouldn't number eleven.

It would be everyone.

In the distance, the cracks in the Old Generation flickered with a dull red light in the darkness.

The floor was trembling.
