# Chapter 23: Not Enough Workers

Slater's thread pool took a hit the moment the device was destroyed.

Not a physical hit—a task hit.

When the device went dark, the three hundred forty-seven unregistered thread people it had created lost their task source. Their task queues went suddenly empty—no new marking tasks, no new reference-maintenance instructions, no new type-loading requests.

But the people were still there.

Three hundred forty-seven thread people were still alive—they still had stack space, reference relationships, and execution capability. They just had nothing to do.

Under normal circumstances, thread people without tasks should exit automatically—execution complete, resources released, natural death. But these three hundred forty-seven hadn't been created through normal procedures. Their lifecycle management was bound to the class-loading device. The device was gone; they had no exit mechanism.

They would live forever.

Forever holding references to leaked objects in the Old Generation.

"Problem's not solved." Slater said through the comm, voice urgent. "Device is gone, but those three hundred forty-seven are still out there. They're wandering the Old Generation like ghosts—still gripping reference lines. The cleaners still can't reclaim those objects."

Cole stopped on his way to the Metadata Attic.

"They have no exit mechanism?"

"None. While the device existed, it managed their lifecycles—assigning new tasks after completion, marking them reclaimable when no tasks remained. Device gone, marking mechanism gone. They're permanently stuck in 'executing' status."

"Can we manually assign them exit tasks?"

"Tried. They don't accept externally assigned tasks. Their task source is hard-coded to the device—only the device can assign tasks to them."

"The device is destroyed."

"Right. So they'll never receive new tasks. And never exit."

Cole closed his eyes and thought for three seconds.

"Then don't make them exit." He said. "Make them complete."

"How do they complete without tasks?"

"Their previous tasks—marking operations, reference maintenance—what status are those in?"

Slater checked. "Mostly 'executing'—tasks were assigned but not completed. After the device was destroyed, the completion signals can't come back, so they're stuck at 'executing.'"

"What if I change those task statuses to 'completed'?"

Slater paused. "The thread people would think their task is done—then wait for new task assignment. But new tasks can't be assigned—because there's no task source. They'd enter a 'waiting for assignment' state."

"In the waiting state—do they still hold references?"

"Shouldn't. After task completion, thread people release all resources held during the task—including references. In waiting state, they hold nothing."

"Can the cleaners reclaim them then?"

"Thread people with no references—the cleaners may not be able to directly reclaim them. But once they enter waiting state with no task source, their survival timer starts counting down. Default is sixty seconds. After sixty seconds, they exit automatically."

"Three hundred forty-seven people, all exiting within sixty seconds." Cole said. "Once they exit, all references released. References gone—"

"The leaked objects lose references—the cleaners can reclaim them!"

"Exactly. But I need you to do one thing."

"Name it."

"Those three hundred forty-seven people's task statuses are scattered across the entire Old Generation. I need your thread pool workers to change them all to 'completed.'"

Slater was silent for a second. "I still have twenty core workers. How many do you need?"

"All of them."

"All? What about my own tasks—"

"Suspend all routine tasks." Cole said. "The only thing that matters right now is making those three hundred forty-seven release their references. Once references break, the cleaners can reclaim the leaked objects. Once space is freed, Full GC becomes unnecessary."

"Understood." Slater said. "But I have twenty workers and three hundred forty-seven tasks. Each worker can only change one task status at a time. At least seventeen rounds. Delay between rounds—"

"How long?"

"If using CAS to change task status—about three seconds per round. Seventeen rounds is roughly one minute. Plus the sixty seconds for thread people to exit—total two minutes."

Two minutes. Not much.

"Start immediately." Cole said.

"Roger." Slater's voice turned decisive. "All workers switching to emergency task—modify leaked thread people's task status to 'completed.' All core workers deploying."

Cole continued toward the Metadata Attic. Behind him, Slater's twenty core workers received their new orders simultaneously. They dropped their routine tasks and surged toward the Old Generation.

Twenty workers, like twenty arrows, shot into the forest of luminous spheres.

The first worker reached his target—a faceless thread person. He crouched and pressed his hand against the target's chest-mounted task status panel.

CAS operation: read "executing," compare "executing," swap "completed."

One second. Status changed.

The faceless thread person's body trembled slightly—his task was done. He released the reference line he'd been gripping. The line slipped from his fingers and hung suspended in the air, like a kite whose string had been cut.

Then he began to wait. For a new task.

No new task came.

The timer started counting down.

Sixty, fifty-nine, fifty-eight...

The second worker finished his target. The third, the fourth...

Twenty workers operating simultaneously, highly efficient. Across the Old Generation, faceless thread people released their reference lines one after another and entered waiting state.

Reference lines sloughed off in droves, like leaves falling in autumn.

The leaked objects that had been maintained for three days lost their artificial reference protection for the first time. Their reference chains began to decay naturally—without external maintenance, reference relationships would gradually weaken over time.

The cleaners wouldn't reclaim immediately. The reference chains hadn't fully broken—decay took time.

But the direction was right.

Cole watched it all as he kept walking. He still had his own task—use Donovan's token to enter the Metadata Attic's bottom layer and revoke the remaining incremental updates.

The token in his hand was growing warm—Donovan's residual identity information was dissipating.

He had to reach Meta before the token became completely invalid.

He quickened his pace.

Behind him, in the Old Generation, the first wave of exiting thread people began to turn transparent.

Sixty seconds were up.

One, two, three...

They vanished silently.

They didn't know why they existed. Didn't know what they'd been maintaining. Didn't even know they were disappearing.

They were just—tools.

And tools, once used up, were put away.

That was Lockhaven's rule.

But Cole knew these rules came with costs. Every tool that vanished had once been alive.

He quickened his pace and didn't look back again.
