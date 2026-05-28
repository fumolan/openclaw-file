# Chapter 3 — Twenty Permanent Workers

Slater's thread pool sat in the transition zone between the Heap District commercial belt and Stack Alley — a square compound enclosed by high walls. From the outside, it looked like a giant labor market, with people constantly coming and going.

But Cole knew the inside was far more complex than any market.

The core of the thread pool was twenty permanent workers. They were stationed in the pool around the clock, always on standby. No matter what happened outside, these twenty were never let go — that was Slater's bottom line. His reasoning: "Twenty core workers are my lifeline. Sure, they idle when things are slow, but I don't care. When things pick up, you'll see why I keep them."

When Cole and Jace arrived at the thread pool, Slater was standing in front of a large blackboard at the entrance, scribbling with chalk. The board was covered in grids, each containing a worker's number and current status.

"Busy, busy, busy, busy —" Slater muttered as he ticked boxes. "All busy."

Cole scanned the blackboard. All twenty core workers' grids were marked "executing." The bottom half of the board was the temps' section — crammed with numbers, many followed by "released" tags.

"You're here." Slater didn't look up. "Figured you'd show up. I heard about the pause."

"All your workers are busy?" Cole asked.

"Are you blind?" Slater finally turned. His shrewd face was etched with exhaustion, dark circles heavy under his eyes. "Twenty core workers, all on duty. Hired thirty-plus temps last night, twelve still working. The rest were released after finishing."

"What's causing so many tasks?"

Slater hesitated. He fished a crumpled list from his pocket and handed it to Cole.

Cole took one look and his brow tightened.

The list showed all tasks from the past three days. The volume was clearly abnormal — normally the thread pool handled fifty or sixty tasks a day at most, but the list showed over two hundred tasks yesterday alone.

"Who submitted these tasks?" Cole asked.

"Don't know." Slater shook his head. "Tasks came in through the standard interface, but the source information was scrubbed. I can only see the task content."

"What's the content?"

"Repetitive tasks." Slater said. "Lots of them. Same pattern — enter the old generation area, execute a marking operation, return."

Marking operations. Cole's heart skipped a beat.

Marking was the Sweepers' job. But the Sweepers had their own team — they didn't need Slater's thread pool for marking tasks. If external tasks were also performing marking operations —

"What were these marking operations marking?" Jace asked.

"Unclear." Slater said. "My workers just execute, they don't ask questions. But I noticed one detail — when these marking tasks execute, the object reference counts in the old generation change."

"What kind of change?"

"Increase." Slater said. "Every time a marking task completes, the reference count of certain old generation objects goes up by one. As if something is constantly adding new references to those objects."

Cole and Jace fell silent simultaneously.

An object being referenced meant it wouldn't be collected. If an object's references kept increasing, the Sweepers would never touch it — even if the object had no practical use whatsoever.

This was the essence of a memory leak.

"You said these tasks started three days ago?" Cole asked.

"That's right. Suddenly flooded in three days ago. Never happened before."

Three days ago. The first pause had been three days ago.

"Slater," Cole lowered his voice, "during today's three-seventeen pause, what were your workers doing?"

"During the pause?" Slater blinked. "Frozen. Everyone was frozen."

"All twenty core workers were frozen?"

"Of course. Nobody can escape a pause." Slater stopped mid-sentence, looking into Cole's eyes. "Wait — what are you getting at?"

"Could your workers have been temporarily commandeered during the pause?"

"Impossible." Slater was emphatic. "I'm the only one who controls my workers. Nobody touches them during a pause. Unless —"

He didn't finish.

"Unless what?"

Slater's expression turned subtle. "Unless someone bypassed me and operated my task queue directly."

The task queue. The thread pool's task queue was a capacity-limited buffer. Normally, external tasks had to be submitted through Slater's interface, and Slater decided which worker got what. But if someone could stuff tasks directly into the queue —

"Can you check your task queue?" Cole asked.

Slater walked to the queue console and pulled up the operation logs.

The log was long. Cole and Slater scanned the timestamps together. Before three-seventeen, everything was normal. At three-seventeen, the pause began, all operations frozen. The six minutes between three-seventeen and three-twenty-three were blank — no operation records.

"Nothing at all during those six minutes?" Jace asked.

"During a pause, of course there's nothing." Slater said.

"Wrong." Cole pointed to the end of the log. "Look at the first record after the pause ended."

Three-twenty-three, pause recovery. The first record wasn't a task execution result — it was an enqueue record. A new task had been pushed into the queue the instant the pause ended.

"That's not normal." Slater's face changed. "Right after recovery, no new task should come in that fast. It takes at least a few seconds for a task to go from submission to enqueue."

"Unless this task wasn't submitted through the normal interface." Cole said. "It was prepared during the pause, waiting at the queue entrance, and auto-enqueued the moment the pause lifted."

Beads of sweat formed on Slater's forehead.

"Someone stuffed something into my queue during the pause." His voice trembled slightly. "That means someone was active during the pause. They touched my queue. They touched my workers."

"Not just your queue." Jace said coldly from the side. "They touched Cole's lock during the pause, and they touched your queue. Their range of activity is much larger than we thought."

Slater sat down. He stared at the blackboard with its twenty "executing" tags.

"Cole," he looked up, "what do you need me to do?"

"Two things." Cole said. "First, from now on, monitor the source of every new task. No matter which interface it comes through, I want to know who submitted it."

"And second?"

"Cut your worker count to the minimum. Keep only the twenty core workers. No temps."

Slater's eyes went wide. "With this kind of workload, you want me to cut staff?"

"Precisely because the workload is abnormal." Cole said. "If someone is using your thread pool for something shady, more tasks means more cover for them. Reducing workers forces them to surface — when tasks pile up until the queue overflows, they'll have to switch to another method. That's when we can trace their real path."

Slater gritted his teeth. "Fine. But I have a condition."

"Name it."

"After we find out who did this, I want to handle them personally." A dangerous glint flashed in Slater's eyes. "Nobody messes with my thread pool without paying the price."

Cole nodded once.

He turned and left the thread pool, Jace following behind.

"You think Slater's right?" Jace asked. "Someone bypassed him and hit the queue directly?"

"Possibly." Cole said. "But there's another possibility — Slater is lying."

Jace whistled.

"You think Slater himself is the inside man?"

"I didn't say that." Cole's pace didn't slow. "But all the clues point to his thread pool. The ability to act during a pause requires execution resources, and his pool is the only place in the city that can provide that much horsepower. Whether he knows it or not, his pool has been compromised."

"And you still had him monitor task sources?"

"Having him monitor is also monitoring him." Cole said. "If he's innocent, the monitoring data will help us find the real culprit. If he's guilty, contradictions will show up in the data."

Jace grinned. "Cole, you're more devious than I thought."

Cole didn't respond. His gaze was fixed on the depths of the Heap District commercial belt — Donovan's territory was in the western section, five major passages away.

"Where to next?" Jace asked.

"Donovan can wait." Cole said. "I want to see Vera first."

"Vera? You just talked to her."

"She said she saw shadows in the Heap. I want to know more."

"What about me?"

"Go stake out the entrance to Segment 3." Cole said. "Donovan's commercial zone is divided into sixteen segments. Segment 3 is the quietest one. If something's wrong with it, it won't stay quiet forever."

Jace shrugged. "Fine. But Cole —"

"Yeah?"

"If I see something I shouldn't in Segment 3, can I act?"

Cole looked at him. "Yes. But don't kill. I need them alive."

Jace laughed and walked away.

Cole headed toward the Heap District commercial belt alone. Behind him, in the thread pool, Slater was rearranging worker numbers on his blackboard. Twenty grids, twenty names.

His thread pool was everything to him. No one knew every worker's status better than he did.

But if even he couldn't control his own workers — then the pool was no longer his.

In the distance, Donovan's commercial zone sat unnervingly quiet under the Heap's gray sky.

Too quiet.
