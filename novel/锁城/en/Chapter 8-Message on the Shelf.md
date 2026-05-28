# Chapter 8: Message on the Shelf

By the time Cole emerged from Segment Three, it was already dark.

He didn't go straight to Vera to report. Not because he didn't want to—he needed to deal with something more urgent first. Slater's communicator had buzzed three times while Cole was inside Segment Three. He'd ignored all three. On the fourth, he picked up.

"Cole!" Slater's voice was nearly a shout. "We've got a problem! My queue is blocked!"

"What do you mean?"

"The supply queue—the one Gordon runs—it's completely jammed! Since this afternoon, every dequeue operation is stuck. My workers can't pull supplies; they're all piled up at the queue exit waiting."

"What's Gordon saying?"

"He won't skip the blocked task! He insists on strict first-in, first-out!"

Cole hung up and hurried toward Gordon's supply queue.

The supply queue was in the Heap District's commercial strip, North Zone—a massive, elongated warehouse. One side was the enqueue port, where tasks and supplies entered the queue. The opposite side was the dequeue port, where workers collected their tasks and supplies.

Under normal circumstances, both ports operated simultaneously, supplies flowing smoothly through the queue. But when Cole arrived, over a hundred anxious workers had gathered at the dequeue end.

"Gordon!" Cole found the queue's keeper in the crowd.

Gordon stood at the dequeue control station, his face dark as iron. He was a middle-aged man, stocky and deliberate in speech—famous for his even temper. But today his brow was tied in knots.

"Cole, perfect timing." Gordon's words came twice as fast as usual. "Dequeue is stuck at the fifth position. First four tasks in the queue checked out fine. The fifth—"

"What about the fifth?"

"It won't complete." Gordon pointed at the status panel on the control station. "Task five's status reads 'executing,' but the thread person assigned to it—has vanished."

Cole looked at the panel. The queue status was clear:

- Task 1: Completed ✓
- Task 2: Completed ✓
- Task 3: Completed ✓
- Task 4: Completed ✓
- Task 5: Executing (Thread ID: 87-F, Status: Non-existent) ✗
- Task 6: Waiting
- Task 7: Waiting
- …… (Subsequent waiting tasks: 217)

"The thread person executing Task 5 doesn't exist anymore?"

"He disappeared during the pause early this morning." Gordon said through gritted teeth. "The task was assigned to him, he started executing, and then the pause hit. When the pause ended, he was gone—but the task's status never changed back. It's stuck on 'executing.'"

"Why not just manually reset the status?"

"Can't." Gordon shook his head, his tone stubborn. "The queue's rule is first-in, first-out. If Task 5 hasn't properly completed or failed out, I can't skip it. Every task behind it has to wait until it's resolved before it can dequeue in order."

"Gordon," Cole kept his anger in check, "there are over two hundred tasks backed up behind it. Some are food rations for Slater's workers. You can't hold up everyone for one dead task."

"Rules are rules." Gordon looked up, meeting Cole's eyes. "If I skip Task 5, I violate the first-in, first-out principle. Skip one today, skip two tomorrow. Before long, why would anyone queue? They'll just cut in line."

"So what's your plan? Wait for the vanished thread person to come back?"

"I plan to find Task 5's original definition and see what operation it's actually executing. If I can understand its logic, maybe I can manually trigger a completion or failure."

Cole took a deep breath. Gordon wasn't being unreasonable—he was just rigid. But that rigidity was a virtue under normal circumstances: it was precisely his strict adherence to FIFO that kept the supply queue running reliably.

"Show me Task 5's contents." Cole said.

Gordon pulled up the detailed definition. Cole scanned it, and his face changed.

Task 5's operation: Enter the Heap District's Old Generation, locate the object at the specified address, increment its reference count.

"Reference count again." Cole murmured.

"What?"

"This task—it's connected to that CAS counter in Segment Three." Cole pointed at the address in the task definition. "The object it's targeting is right in the heart of the leaked objects in the Old Generation."

"You're saying—the task itself is part of the problem?"

"Yes." Cole said. "Someone submitted a flood of marked tasks through Slater's thread pool. Those tasks were designed to add references to the leaked objects in the Old Generation. Task 5 was one of them. The thread person executing it disappeared during the pause, but the operation was already partially executed—the reference count was already incremented, but the task never sent back a completion signal."

"So it's stuck in an intermediate state."

"Exactly. And your queue won't skip it—"

"Because the rules don't allow it."

Cole looked at Gordon's obstinate face. Under normal circumstances, he'd respect Gordon's rules. But these weren't normal circumstances.

"Gordon," Cole shifted tactics, "what if I don't ask you to skip Task 5, but to properly complete it instead?"

"How? The thread person executing it is gone."

"Task 5 is supposed to increment a specific object's reference count. If that operation has already been carried out—the count has already gone up—then Task 5 has essentially succeeded. All it's missing is a completion signal."

Gordon thought about it. "You mean—I manually send it a completion signal?"

"Not you. The task's original submitter." Cole said. "If I find whoever submitted Task 5 and they confirm the operation is done, you can let Task 5 exit normally."

"But I don't know who submitted this task."

"I do." Cole said.

He didn't explain further. He turned to face the anxious workers gathered outside the dequeue port.

"Everyone, give me one hour." Cole raised his voice. "Within an hour, the queue will be moving again."

The workers dispersed, skeptical but willing. Gordon watched Cole's retreating back.

"Where are you going?"

"Segment Three." Cole said. "Donovan's there. Task 5 was submitted through the thread pool by him. I'll get him to confirm completion—or make him watch what his operation has caused."

He strode away from the supply queue.

Behind him, Gordon stared at the stuck "Executing" status on his control station. He placed his hand on the panel, his finger tracing the edge of Task 5's ID number.

"First in, first out." He said softly. "The old rule doesn't change."

But he knew that if Cole didn't come back with a completion signal within the hour, he'd be facing two hundred angry workers and a completely broken queue.

First-in, first-out was the rule.

But whether the rule could hold depended on the people.
