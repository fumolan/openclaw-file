# Chapter 17: The Rules of the Queue Changed

On the eve of the decisive moment, Quincy made a decision that caught everyone off guard.

He turned off fair mode.

When the news spread, Cole was in Stack Alley making final preparations. His communicator crackled with Quincy's voice—no explanation, just one sentence: "Tomorrow morning, my queue no longer guarantees first-come, first-served."

Cole set down the lock tools in his hands and called back.

"Quincy, what are you doing?"

"Buying you time." Quincy's voice was unusually calm. "That window you need—the few seconds between Wyatt releasing the write lock and the flood of anomalous writes—I can stretch it."

"How?"

"With unfair mode." Quincy said. "Under fair mode, my queue allocates resources in strict first-come, first-served order. Under unfair mode—no queuing. Whoever gets there first takes it. Miss out, wait for the next round."

"What does that have to do with me?"

"After Wyatt releases the write lock, anomalous write requests will flood my queue. If my queue is fair, these requests line up in order—from first to last, processed one by one. That means the anomalous writes flow in at an even, predictable pace, and your window will be very narrow."

"And if it's unfair?"

"Under unfair mode, new requests can cut in line—seizing resources before queued requests are processed. That means anomalous write requests get scattered—some execute immediately, some get pushed back by newer arrivals. Writes no longer follow an even rhythm; they come in waves. There are gaps between peaks."

"The gaps are my window."

"Exactly." Quincy said. "Gaps between peaks could last several hundred milliseconds, even a full second. Much wider than the window you originally estimated."

Cole took a deep breath. Quincy wasn't just helping him—Quincy was joining the fight in his own way. Turning off fair mode meant abandoning the core philosophy of his queuing mechanism. For an old man who'd built his life on fairness, it was a painful choice.

"Are you sure?"

"Not sure." Quincy said. "But unfair mode has another advantage—higher throughput. Under heavy contention, fair mode has overhead from maintaining queue order. Unfair mode eliminates that—processing is faster."

"But it'll make the people in your queue—"

"Uncomfortable." Quincy finished for him. "I know. People who've waited a long time might get their spots stolen by newcomers. But it's temporary. After tomorrow morning, I'll restore fair mode."

"What if people are unhappy?"

"Let them come to me." A long-dormant sharpness entered Quincy's voice. "I've been a fair man for fifty years. I can afford one unfair day."

The comm went silent.

Cole stood at the Stack Alley window, looking out at the Heap District commercial strip's lights. Five in the morning—the city was still sleeping, or rather, gathering strength for the storm to come.

He thought about the people in Quincy's queues. Some had been waiting two days. They queued properly, no cutting, no complaints, because they believed in fairness. They believed first-come, first-served was the city's iron law.

Tomorrow, that iron law would be suspended.

Some of them would be bumped by newer requests. They'd be angry, confused, betrayed.

But Cole knew—if today failed, queuing itself would cease to matter. Fairness presupposed a functioning city. If the city paused—paused completely—not even the right to queue would remain.

He gathered his gear and stepped out of Stack Alley.

On his way to Segment Three, he passed through Quincy's plaza. In the predawn hours, dozens of queuers remained—waiting in their sleep.

Cole didn't wake them.

He simply crossed the plaza and headed toward Segment Three.

Behind him, Quincy sat in the heart of the tree's crown, watching the data on his crystal screen.

On the screen, the "Fair Mode" toggle had been switched to "Off."

The old man stared at that switch for a long time, silent.

Then he sighed softly.

"One day." He said to himself. "Just borrowing one day."

The brass tags on the tree's roots swayed gently in the night breeze. Each tag represented someone waiting.

Tomorrow, some would get their turn.

Some wouldn't.

But at least—after tomorrow, there would still be a tomorrow.
