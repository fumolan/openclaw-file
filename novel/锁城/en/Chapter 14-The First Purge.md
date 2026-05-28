# Chapter 14: The First Purge

Warden launched a deep sweep in the Old Generation.

It wasn't planned—he'd been forced into it. Old Generation capacity was approaching ninety-five percent, and New Generation objects kept getting promoted. Without a deep sweep, the Old Generation would fill completely within hours.

Vera guided Cole to Warden. The head of the cleaners stood in the Old Generation's central plaza, twenty-odd cleaners in gray uniforms lined up behind him. Their gear was specialized—marking wands in hand, reclamation satchels slung over their shoulders.

"Cole." Warden spotted him and gave a nod. Sixty years old, his face deeply furrowed, but his spine was ramrod straight. His eyes were gray—like the Old Generation's sky.

"Warden, I need to talk to you."

"About what?"

"Do you know why the Old Generation filled this fast?"

Warden paused. "I know."

"Do you know someone's deliberately creating leaked objects?"

"I know." Warden's voice didn't waver. "But I don't have time to deal with causes right now. I can only deal with consequences."

He waved his hand, and the twenty-odd cleaners simultaneously raised their marking wands and fanned out in four directions.

"Marking begins." Warden ordered.

Mark-and-sweep. One of the oldest cleaning methods. First, mark all reclaimable objects—those not pointed to by any reference. Then sweep them away, freeing space.

But this situation was unusual. Most objects in the Old Generation were maintained by artificial references—their reference chains, though closed-loop, genuinely existed. When the marking wands passed over them, they didn't light up—meaning "reachable," not reclaimable.

Only a handful of genuine garbage objects—those with truly broken reference chains—were marked as reclaimable by the wands.

"Marking complete." A cleaner returned to report ten minutes later.

"Sweep." Warden ordered.

The sweep was quiet. Marked objects turned transparent one by one and vanished. Space was indeed freed.

But not much.

Warden looked at the post-sweep space report, his brow tightening.

"Three percent freed." He said. "Old Generation dropped from ninety-five to ninety-two percent."

"Is three percent enough?" Cole asked.

"No." Warden shook his head. "At the current expansion rate, it'll fill back up in a few hours."

"What about fragmentation after the sweep?"

Warden glanced at the Old Generation's interior. The cleared regions were scattered—chunks here and there, like cheese gnawed by mice. The freed space was fragmented, each piece too small to accommodate large objects.

"Severe fragmentation." Warden admitted. "Mark-and-sweep only handles reclamation, not compaction. The freed space is scattered. If a newly promoted object is large, it won't fit anywhere."

"So what do we do?"

"Compact." Warden said. "After mark-and-sweep, we run a mark-and-compact—move all surviving objects to one end and carve out contiguous free space."

"But compaction means moving objects. Moving objects means modifying reference relationships. Modifying reference relationships requires—"

"A city-wide pause." Warden finished for him.

Cole said nothing.

"Mark-and-compact must freeze all thread person activity." Warden said. "Because while objects are being moved, if a thread person is still accessing an object through its old reference address—they'll land at the wrong location. So we must pause."

"Another pause."

"Yes. And longer than a normal pause." Warden looked into the Old Generation's depths. "A normal pause only marks and sweeps—most objects don't need to move. But mark-and-compact moves nearly every surviving object—that takes significant time."

"How long?"

"Based on current Old Generation object counts and fragmentation levels—" Warden calculated silently. "At least fifteen minutes."

Fifteen minutes. City-wide pause for fifteen minutes. The last three-minute pause had cost eleven lives. How many would a fifteen-minute pause claim?

"Is there another way?" Cole asked.

"Yes." Warden said. "Regional sweeping."

"Regional?"

"Divide the Old Generation into small regions and sweep one at a time." Warden said. "No need for a city-wide pause—just suspend activity in that particular region. Everything else keeps running."

"Have you used this method before?"

"I have." Warden said. "It's the newest cleaning approach—divide the entire Heap District into equally sized regions and sweep them one by one. Each time, only a small region pauses. Downtime is much shorter."

"Then why not use it?"

"Because it's limited." Warden sighed. "Regional sweeping works for gradual cleanup, but the Old Generation is expanding too fast. Regional sweeping can't keep up."

He turned to face Cole.

"Cole, you're a smart man. You should see it by now—cleaning isn't the solution. No matter what method I use, as long as those leaked objects remain and their reference chains hold, I'm just bailing water from a leaking bucket."

"So what's your recommendation?"

"Plug the leak." Warden met Cole's gaze. "Find the source. Shut down that class-loading device."

"Can't shut it down. Forcible shutdown triggers cascading collapse."

"I know." Warden's voice dropped. "But if we don't—Full GC is only a matter of time. When it hits, the city-wide pause won't be fifteen minutes. It could be thirty minutes, an hour, maybe longer. In a pause like that—"

He didn't finish.

But Cole knew what he meant.

In a one-hour pause, what vanished might not be just thread people. It could be the entire city.

"Warden," Cole said, "I have a plan."

"Go ahead."

"Tomorrow morning, you launch a sweep targeting the direct memory region."

Warden blinked. "Direct memory? That's outside my jurisdiction."

"I know. But inside direct memory there's a channel—a data line extending from the Old Generation to the Metadata Attic's bottom layer. That channel is transmitting 'maintain references' instructions. If you can cut that channel during the sweep—"

"I can't. Cleaner authority is limited to the Heap District. Direct memory isn't part of the Heap."

"But the cleaners' marking ripples pass beneath direct memory." Cole said. "The ripples can't directly clear data in direct memory, but they can interfere with data transmission—like a strong magnetic field disrupting radio signals. If you concentrate the ripples directly below the direct memory region and sustain them for a few seconds—"

"You want me to use marking ripples to interfere with data transmission?" Warden's eyes narrowed. "That's not what marking ripples are designed for."

"I know. But right now it's the only way to cut that channel without entering direct memory."

Warden was silent for a long time.

"Ripple interference can't be guaranteed." He said. "It might cut the channel, or it might only cause brief disruption—the channel would automatically recover once the interference stops."

"Brief disruption is enough." Cole said. "I only need a window of a few seconds. During those seconds, the reference-maintenance instructions would be interrupted. While they're down, the reference chains would be momentarily exposed—that's when the cleaners can reclaim leaked objects."

"A few seconds—how many objects can I reclaim at most?"

"Not all of them. Just the critical batch—the core objects directly referenced by the class-loading device. Once those core objects are reclaimed, the entire reference network begins to collapse."

Warden thought it over. "This requires precise timing. The ripple interference window—when do you need it?"

"Tomorrow morning. The moment Wyatt releases the write lock."

"Why that moment?"

"Because after Wyatt releases the write lock, the window for anomalous writes reopens. The class-loading device will accelerate—it'll do two things simultaneously: transmit 'maintain references' instructions and distribute new tasks. While doing both, its resistance to ripple interference will be at its weakest."

Warden nodded slowly.

"I can try." He said. "But Cole—if it fails. If the ripples don't cut the channel, or the interference doesn't last long enough—"

"There won't be a second chance." Cole said. "Because the ripple interference will reveal your intentions. Donovan—or the class-loading device—will realize the cleaners are no longer neutral. At that point, it'll go all out."

"All out—"

"The Old Generation fills within hours. Full GC becomes unavoidable."

Warden took a deep breath. His gray eyes studied Cole, weighing the young man's resolve.

"Are you sure your plan will work?"

"No." Cole said. "But it's the best plan we have."

"The best plan—how confident are you?"

Cole thought for a moment.

"Thirty percent."

Warden laughed—a weathered, helpless sort of laugh.

"Thirty percent." He repeated. "All right. Thirty percent is better than zero."

He turned to face his cleaners.

"Tomorrow morning. Everyone goes on standby."

The cleaners nodded in silence.

Cole turned to leave the Old Generation. Behind him, Warden's voice echoed.

"Cole."

"Yeah?"

"If this works—remember one thing for me."

"What?"

"Cleaners aren't killers." Something complex lived in Warden's voice—regret, maybe, or expectation. "We only do what the city needs us to do. But if the city itself is broken—cleaning shouldn't be the only answer."

Cole didn't look back.

He knew Warden was right.

But he also knew that in the next few hours, cleaning—and possibly the enormous pause that followed—was the answer everyone was facing.

In the distance, the Old Generation's sky darkened another shade.
