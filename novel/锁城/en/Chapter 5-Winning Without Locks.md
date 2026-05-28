# Chapter 5: Winning Without Locks

Cole hadn't made it to Donovan's commercial zone before his communicator buzzed.

It was Jace.

"Cole, don't come to Segment Three. Something's up."

Cole's stride faltered for a beat. "What?"

"While I was staking out the Segment Three entrance, I found an unregistered passage. Not a normal one—looked freshly dug. I crawled in and took a look. The structure inside is weird."

"Weird how?"

"There's a counter inside the passage." Jace's voice carried an unusual excitement. "A shared counter, constantly climbing. Ticks up every few seconds. But there's no lock on it at all. No biased lock, no lightweight lock, nothing."

"No lock? How does it maintain data consistency?"

"That's the interesting part." Jace said, "It's using CAS."

By the time Cole reached the Segment Three entrance, Jace was crouched beside a concealed fissure tucked into the corner where two walls met. You'd never spot it unless you were looking hard. Inside was a narrow passage—just wide enough for a person to edge through sideways.

"You're sure this passage isn't on any map?"

"Checked three times." Jace said, "It's not on the commercial zone's public maps. It was dug later."

Cole ducked through the fissure. The passage wasn't long—about twenty steps to the end, where it opened into a slightly wider space, like a small room carved out in haste.

In the center of the room stood a metal pillar. A panel at its top displayed a number that kept changing.

1247.

1248.

1249.

Every few seconds the number incremented. Cole watched for a minute; by then it had climbed to 1255.

"See?" Jace stood beside him. "No lock. Absolutely none. But it's never gone wrong."

Cole leaned closer. At the bottom of the panel was a line of small text—an operation log. He scanned a few entries and immediately spotted the pattern.

Each increment was logged as a three-step operation: read current value, add one, write back. No lock protected the three steps. Under normal circumstances, two people operating at the same time should have caused errors. But the log showed every operation had produced a correct result.

"CAS." Jace pointed at the log. "Look at this line—compare and swap. The operator reads the current value—say, 1255—calculates the new value, 1256, and then performs a comparison: is the value still 1255 right now? If yes, it swaps in 1256. If not—meaning someone else changed it in the meantime—it starts over."

"Has it ever had to retry?" Cole asked.

"It has." Jace flipped through the log. "But rarely. Most of the time it succeeds on the first comparison. That means very few people are touching this counter simultaneously—low contention."

Cole studied the ever-climbing number, doing rapid mental arithmetic. What was this counter tracking? If it was an object's reference count, every increment meant a new reference had been established. If references kept growing—

"This is a reference counter," Cole said.

"What?"

"It's not an ordinary counter." Cole pointed at the jumping digits. "It's adding references to some object. Every tick creates a new reference. The more references, the less likely the cleaners can reclaim that object."

Jace's face changed. "So this is a memory leak tool?"

"Yes. But more elegant than I expected." Cole crouched to examine the base of the pillar. "It uses no locks, so it won't be detected during pauses—when the cleaners scan, locks themselves are scan targets. No locks means an extra layer of stealth."

"But who's executing these CAS operations?"

Cole circled the pillar. On its back, a thin data cable ran into the passage wall and vanished.

"Remote operation." Cole said. "The operator isn't here. They're sending CAS commands through this cable."

"Can we trace it?"

"Yes. But not now." Cole straightened up. "If we yank that cable, the operator will know instantly that we've found the counter. They might relocate or destroy evidence. We need them to keep operating without suspecting anything."

"So what do we do?"

"Something I'm better at than they are." Cole pulled a biased lock from his pocket but didn't attach it to the pillar. "CAS isn't just their weapon."

He pocketed the lock and placed his right hand on the panel, fingers pressing lightly.

"What are you doing?" Jace leaned in.

"Reverse CAS." Cole said. "They use CAS to increment the counter. I can use CAS to do something else—like, without changing the counter's value, change its operation frequency."

His fingers glided across the panel. Cole wasn't a natural CAS prodigy like Jace, but his understanding of low-level mechanisms far exceeded most. He knew the core of CAS wasn't speed—it was precision. You didn't need to be faster than your opponent; you just needed to be more accurate.

His fingers stopped. A new parameter appeared on the panel: operation interval. The CAS operations, which had been firing every three seconds, were now quietly reset to every eight seconds.

"I've reduced the frequency," Cole said. "The counter's still climbing, but slower. From the outside, it might look like a network hiccup causing the slowdown. They won't suspect a thing."

"And then?"

"Then we exploit the time gap." Cole said. "Slower counter means slower reference growth. That gives the cleaners breathing room—maybe an extra day or two. In that time, we have to find the remote operator."

He turned to face Jace. "Can you trace the data cable now? Don't pull it—just determine its direction."

Jace crouched, pressed his palm against the wall, and slowly tracked the cable's path.

"Northwest," he said. "Through Segment Three's wall, heading into—" His finger stopped.

"Into where?"

"The direction of the Metadata Attic."

Cole closed his eyes.

The Metadata Attic again.

Every lead converged on the same place: anomalous objects injected from the outside, injection via custom class loader, the class loader's control endpoint pointing at the Metadata Attic.

"Cole." Jace stood, his expression grimmer than before. "If the control endpoint is really in the Metadata Attic, that means Meta—"

"Not necessarily." Cole cut him off. "The Metadata Attic is the city's largest type information repository. Anyone with access rights can store or retrieve data inside. Meta is the guardian, but she's not the only one with a key."

"Who else has a key?"

"I don't know. But I know who might know."

"Who?"

"Quincy." Cole said. "Quincy maintains the city's queuing mechanism. Every request, every resource allocation passes through his queues. If someone's been frequently accessing the Metadata Attic, Quincy's queues will have the records."

"Then let's go see Quincy."

"No." Cole shook his head. "Donovan first."

"Changing your mind again?"

"We've got enough leads." Cole said. "That counter in Segment Three is hidden in Donovan's commercial zone. Whether Donovan knows about it or not, he owes me an explanation."

He took one last look at the still-ticking number—now jumping only every eight seconds. 1256… 1257…

Slow, but not stopped.

Cole edged out of the passage and back to the Segment Three entrance. Jace followed, glancing back at the fissure.

"You said you can win without locks," Jace said. "But he didn't use locks either, and he's been winning for a long time."

"He didn't win on locks." Cole said. "He won on stealth."

"And your reverse CAS? Does that count as winning?"

"No." Cole's face was calm. "It counts as buying time."

He walked toward the west end of the commercial zone—Donovan's territory.

Behind him, in the fissure, the counter's panel ticked again. 1258.

Slow, but not stopped.
