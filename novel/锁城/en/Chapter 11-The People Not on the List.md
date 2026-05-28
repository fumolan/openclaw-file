# Chapter 11: The People Not on the List

Jace spent the entire afternoon on a single task—precisely tallying the total number of living thread people in Lockhaven.

It wasn't a simple headcount. Thread people numbers fluctuated constantly—some vanished during pauses, some crashed mid-task, some sat in queues waiting for assignment. But Jace's CAS skills gave him a natural advantage for counting: he could rapidly scan the citywide thread registry without disturbing anyone, checking each entry's living status.

The result made him inhale sharply.

"Three hundred forty-seven extra." In Cole's Stack Alley quarters, Jace spread his statistical report across the table. "The thread registry lists a total of one hundred twenty-six thousand thread people. But the actually living—meaning those with active reference relationships in the Heap District—comes to one hundred twenty-six thousand three hundred forty-seven. Those extra three hundred forty-seven aren't on the registry."

Cole looked at the numbers, his frown deepening.

"Not on the registry, but they have active references?"

"They do. They're not ghosts—they have complete reference chains, allocated stack space, tasks they're actively executing. From the system's perspective, they're normal thread people. They're just not registered."

"That's impossible. Thread people must be registered upon creation."

"Normally, yes." Jace flipped to the report's second page. "But I traced the creation records for several of them—their creation requests bypassed the standard registration process. Not through Slater's thread pool, not through Quincy's queuing mechanism, not even through Meta's class-loading channel. They came from—"

"The class-loading device in Segment Three directly."

"How did you know?"

"Because I saw the device today." Cole gave Jace a brief account of his discovery in Segment Three. Jace's face grew paler with every detail.

"Custom class loader..." Jace murmured. "He didn't just create new types—he used those types to create new thread people. These thread people—"

"Are the extra three hundred forty-seven."

"What are they doing?"

Cole walked to the window and looked out at Stack Alley's gray sky.

"They're holding references." He said. "Every unregistered thread person holds one or more strong references to objects in the Old Generation. As long as they're alive, those objects won't be reclaimed."

"Three hundred forty-seven people, each holding a few references—"

"Thousands of objects become unreclaimable."

"And they're still creating more—the class-loading device is still running—"

"Right. Every cycle produces more types, more objects, more thread people." Cole's voice was level, but Jace heard the undertow beneath it.

"The reference counter." Jace said suddenly. "That CAS counter you found in Segment Three—what's it counting for?"

"For the leaked objects' reference counts." Cole said. "Every increment means a new reference was established. If the thread people creating those references are the three hundred forty-seven unregistered ones—"

"Then the references will never break." Jace finished his thought. "Because the people creating them were themselves created by the class-loading device. The device doesn't shut down, they don't die. They don't die, the references don't break. The references don't break, the objects don't get reclaimed. It's a closed loop."

Cole nodded.

"How do we break it?"

"Through the class-loading device." Cole said. "But Meta said it can't be forcibly shut down. Forcible shutdown triggers a cascading collapse."

"So what, ask Donovan to shut it down himself? He'd have to be insane to agree."

"Not asking Donovan. We make those three hundred forty-seven people disappear first."

Jace blinked. "How? They have complete reference relationships—the cleaners won't touch them."

"The cleaners won't. But what if their reference relationships get reassigned?"

"Reassigned?"

"A thread person's reference relationships aren't carved in stone." Cole said. "When a thread person finishes a task, their references get cleaned up—reclaimed by the thread pool or the task scheduler in one sweep. Since those three hundred forty-seven were created illegally, their references were never folded into the normal management system."

"You mean—we manually bring their references into the management system, then recycle them through normal procedures?"

"Not recycle them. Make them complete their tasks and exit execution." Cole turned to face Jace. "A thread person who's completed a task no longer holds any object references. No references means—"

"The cleaners can reclaim them."

"No. A thread person with no references doesn't need the cleaners to reclaim them—they exit on their own. A thread person's lifecycle is finite: execute task, return result, exit. If their task gets marked as complete, they naturally terminate and release all held resources."

Jace's eyes brightened. "So the key is—assign those three hundred forty-seven a completable task, let them finish it and exit?"

"But we don't assign it. They won't accept externally assigned tasks because their task source is the class-loading device. We need to change the task content the class-loading device distributes to them."

"Change the task content? How do we modify the task distribution logic in Segment Three's class-loading device?"

"Through CAS." Cole looked at Jace. "That CAS counter you found in Segment Three—I changed its operation interval to eight seconds. That counter doesn't just control the reference count—it's the class-loading device's task distribution metronome. Every tick distributes a new batch of tasks."

"You slowed the metronome—"

"Task distribution slowed down, but the task content is still the same. If I can CAS my way in and change the task content to a 'null task'—one that can be completed without holding any references—"

"Then the thread people who receive null tasks will complete immediately, exit immediately, and release their references!"

Cole nodded once.

"But there's a catch." He said. "CAS operations must be atomic—compare and swap must complete in the same instant. If the class-loading device detects someone modifying the task content, it'll trigger a self-preservation mechanism—accelerate and load all remaining types at once."

"So we get exactly one CAS shot."

"One." Cole said. "Compare, swap. One instant. Get it right, and the three hundred forty-seven gradually exit. Get it wrong—"

"Cascading collapse."

Silence fell between them.

Outside the window, Stack Alley's lights flickered on and off. In the distance, the Heap District commercial strip's lights were dimmer than last night—the Old Generation's space shortage was already affecting the commercial strip's power supply.

"Cole." Jace's voice was uncharacteristically grave. "One CAS. Do you trust me?"

"Why are you asking?"

"Because I'm the one who has to make that CAS." Jace said. "Your expertise is locks—biased locks, lightweight locks, heavyweight locks, that's your domain. CAS is mine. You can't match my precision."

Cole didn't argue. It was a fact.

"How long do you need to prepare?"

"I need to go back and study the counter's full structure first." Jace said. "CAS isn't something you do with your eyes closed—I have to know exactly where the target data sits, its format, its possible values. Give me twelve hours."

"You have eight." Cole said. "Wyatt's write lock can only be held for one day. He pulled it this morning; it has to be released tomorrow morning. The moment Wyatt releases that lock, the window for anomalous writes reopens. That window will almost certainly be exploited by the class-loading device—it's waiting for a write window to accelerate task distribution."

"Eight hours." Jace took a deep breath. "Enough."

He stood and headed for the door.

"Jace." Cole called after him.

"Yeah?"

"Don't miss."

Jace grinned. "Relax. CAS is my life."

He pushed the door and walked out.

In Stack Alley, the sound of his footsteps quickly faded.

Cole sat back down and looked at the statistical report on the table. Three hundred forty-seven people not on any list. They didn't know they were abnormal—they thought they were residents of Lockhaven, thought they were executing legitimate tasks, thought their reference relationships were valid.

They were simply carrying out assigned tasks. Like the packages waiting in Gordon's queue to be dequeued—not knowing what their existence meant.

In the distance, the sky above the Heap District's Old Generation trembled.

Eight hours.

Cole closed his eyes. Somewhere deep in his mind, a countdown had begun—a countdown that would determine Lockhaven's fate.
