# Chapter 20: Double-Checked Locking

Eight o'clock sharp. Two hours until Wyatt released the write lock.

Cole met Slater at the Segment Three entrance. The thread pool manager had come without advance notice, looking terrible.

"New problem." Slater cut straight to the chase. "One of my core workers went abnormal."

"What happened?"

"He was executing a routine task and hit a facility entrance that required double-checked locking. The normal flow is—do a quick first check; if the entrance hasn't been initialized, skip it. If it has been initialized, lock and check again."

"And?"

"On his first check, the entrance was uninitialized. He was about to skip it. But in the instant after he checked—the entrance's state changed. To initialized. On his second check, he saw initialized, so he locked and went in."

"What's the problem with that?"

"The problem is—what he saw inside after locking didn't match what he saw on the first check." Slater said. "First check: uninitialized. After locking: initialized. The state change happened between the two checks—in those few milliseconds when he had no lock protection."

Cole's brow furrowed.

"Someone exploited the double-check timing gap." He said.

"Yes." Slater said. "During those few milliseconds, someone changed the entrance's state. My worker walked into a tampered entrance—he thought he was validating the correct state, but what he checked the first time and what he checked the second time weren't the same object anymore."

"And your worker—"

"He triggered the entrance's protection mechanism. Now his execution is suspended—not crashed, suspended. He's inside the entrance waiting for someone to confirm the state."

Cole thought for a moment. "Whose task was your worker executing?"

"Unknown. Just like those marking tasks before—source scrubbed."

"Another trap." Cole said. "They didn't just exploit the double-check timing gap—they used your worker to trigger it."

"What kind of trap?"

"Double-checked locking failure—a DCL vulnerability—has caused serious security incidents in Lockhaven's history." Cole said. "Someone exploited instruction reordering—changing the execution order of operations—to make the state between two checks unpredictable. This kind of vulnerability once broke double-checked locking entirely, exposing incompletely initialized objects to other threads."

"So my worker—"

"Your worker is now hanging inside a tampered entrance. If nobody rescues him, he'll hang forever. But rescuing him means entering that entrance—and the entrance has been booby-trapped."

"So what do we do?"

"Don't go through the entrance." Cole said. "Sever his reference relationship with the entrance from outside. His task is suspended—not because of references, but because he's waiting for confirmation. If I send him a confirmation signal—make him think the entrance state is normal—he'll complete the task and exit."

"How do you send a confirmation signal?"

"CAS." Cole said. "The confirmation signal is a simple boolean—true or false. I CAS in, change the waiting-for-confirmation state to confirmed. He can exit."

"CAS again." Slater sighed. "Do you solve everything with CAS?"

"Not everything with CAS. Problems CAS can solve don't need locks." Cole said. "Locks are for keeping people out. But this scenario doesn't require keeping anyone out—I just need to change a value."

He located the suspended worker's position—deep in a corridor in the Heap District commercial strip. The worker's body was motionless, like he'd been encased in amber.

Cole crouched and placed his hand on the control panel on the worker's chest. It displayed the waiting-for-confirmation state—a question mark blinking endlessly.

He felt out the panel's data structure. The confirmation signal lived in a simple boolean field—currently false, needed to be changed to true.

Simple CAS. Read false, compare false, swap true.

One second.

The worker's body stirred. The question mark on his chest became a check mark, and then the entire panel went dark.

The worker opened his eyes.

"I—" He looked around, bewildered. "Where am I?"

"You got suspended." Cole said. "You're fine now. Go back to Slater."

The worker shook his head, stood up, and walked off. His steps were unsteady, but no worse for wear.

Cole straightened and watched the worker's retreating back.

"The double-check timing gap." He muttered. "This attack style isn't random. It requires precise knowledge of the check's timing window, the state's data structure, and the confirmation signal's format."

Not many people could do that.

And among those who could, one was Donovan.

Donovan managed sixteen segments of commercial zone. Every segment entrance used double-checked locking—quick check once, locked check once. Donovan understood double-checked locking deeper than anyone.

"Donovan's counterattacking." Cole said to Slater. "He knows we're preparing. He's stalling us."

"How?"

"Every suspended worker needs a CAS operation to rescue. If he has ten, twenty traps like this—all my time goes to rescuing workers."

Slater's face darkened further. "I'll monitor all tasks from now on. Any task involving a double-checked entrance gets intercepted."

"No. Don't intercept." Cole said. "Let him keep setting traps. But I need you to do one thing—give me each trapped worker's location and confirmation signal format in advance. I'll prep the CAS operations ahead of time—worker gets suspended, I free him within one second."

"You can prepare the antidote before the trap even triggers?"

"As long as I know the trap's location and format." Cole said. "The essence of CAS is—be ready before you act."

Slater hesitated, then nodded.

"Fine. I'll give you real-time status monitoring access for all workers."

Cole turned and left.

Nine o'clock. One hour left.

In the distance, the "Under Renovation" plaque still hung on Segment Three's entrance.

In one hour, that plaque would come down.

Not because the renovation was complete.

Because Segment Three was about to become a battlefield.
