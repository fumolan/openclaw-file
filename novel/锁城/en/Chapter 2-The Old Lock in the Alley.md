# Chapter 2 — The Old Lock in the Alley

Stack Alley looked especially narrow in the dawn light.

Cole returned to his place just as the sky was growing light. He'd meant to rest a few hours before going to see Donovan, but his hand stopped the moment it touched the door latch.

The biased lock's state was wrong.

He stared at the lock for three seconds. A biased lock was the simplest kind — it recognized only one person. When Cole first hung this lock on the door, it automatically etched his signature onto the lock face. After that, every time he returned, the lock recognized him and opened without any additional verification. That was the nature of a biased lock: as long as there was no competition, it was the fastest way through.

But now, the signature on the lock face had been erased. In its place was a more complex structure — the pattern of a rotating turnstile.

A lightweight lock.

A chill ran down Cole's spine.

A biased lock didn't automatically become a lightweight lock. There was only one explanation: while he was away, someone had tried to open this lock. When another person touched a biased lock, it automatically revoked its biased state and upgraded to a lightweight lock — because now there was a competitor, and the lock needed a stricter verification mechanism.

"Someone's been here," Cole murmured.

He didn't rush inside. First he crouched down to check the door frame's seams — no pry marks, no signs of forced entry. The visitor knew how to pick locks, or at least how to trigger a lock upgrade.

He was intimately familiar with how lightweight locks worked: the visitor would have tried to acquire the lock with a CAS operation — first copying their own data to the lock face, then comparing, and if the lock face hadn't changed, replacing it with their own. This process didn't require a physical lock, just a few comparisons.

But revoking a biased lock wasn't something CAS could accomplish. That required a full lock upgrade.

Cole stood up and pushed the door open.

Everything inside was as he'd left it. Table and chairs undisturbed, files untouched, windows closed. The visitor hadn't come to search for anything.

Then what for?

Cole sat down and began to analyze. The biased lock had been upgraded to a lightweight lock, which meant the visitor had touched the lock but failed to enter. The lightweight lock's verification mechanism had kicked in — the visitor's CAS operation had failed, because while Cole's signature had been erased, the lock's state had already changed, and the visitor couldn't complete the replacement.

"So you were probing," Cole said to the empty air.

He didn't know this visitor. But the visitor clearly knew him.

Footsteps echoed in the alley outside. Cole's hand instinctively moved to the lock tools at his waist.

The figure at the door was Jace.

"You didn't sleep?" Jace saw him crouching at the door examining the lock. "What's wrong?"

"Someone's been here." Cole pointed at the lock face.

Jace leaned in for a closer look, frowning. "Biased lock revoked. Upgraded to lightweight."

"Yeah."

"When?"

"During the pause, or right after it ended." Cole said. "I left at three-seventeen. By the time I got back, the lock had already changed."

A strange expression flickered across Jace's face. "During the pause? Everyone was frozen during the pause. Who could have touched your lock?"

That was the question.

During a pause, all thread folk execution was suspended. No one could move. Unless —

"Unless this person wasn't subject to the pause's constraints," Cole said.

Jace fell silent.

"Or," Cole continued, "this person had the ability to maintain localized activity during the pause."

"That's impossible." Jace shook his head. "The pause is city-wide. The Sweepers' marking ripples cover every corner. No exceptions."

"Then explain this lock."

Jace looked at the lock face again. The lightweight lock's turnstile pattern reflected cold white light in the dawn. The lock face still held a trace of the visitor — not identity information, more like a tactile residue.

"Let me try." Jace reached out and touched the lock face lightly.

His fingers lingered for two seconds, then withdrew.

"I felt it." Jace's expression changed.

"What?"

"This lock was attacked with a CAS operation." Jace said. "I can feel the trace of a compare operation. The visitor read the lock's current state first, then tried to CAS-replace the lock face with their own data."

"Successfully?"

"No. The biased lock revocation triggered, but the lightweight lock's CAS verification failed." Jace's analysis sped up. "The visitor did one compare operation, but the lock face changed in the instant of comparison — probably because the biased lock revocation itself altered the lock face state. So the CAS failed."

"How good was the visitor's CAS ability?"

"Very good." Jace offered a rare, serious assessment. "The precision of this CAS operation was extremely high. With an ordinary person, after biased lock revocation, the lightweight lock would enter full contention and the lock face would become a chaotic mess. But this lock face is clean — the visitor did only one CAS and gave up."

Only one CAS and gave up.

That meant the visitor knew exactly what they were doing. They weren't here to force entry — just to probe. One CAS failure, and they immediately backed off, leaving no excess traces.

"Who do you think it was?" Cole asked.

"Don't know. But someone who can move during a pause —" Jace stopped mid-sentence, because the answer was too obvious.

The Sweepers.

The Sweepers were the only entities still active during a pause. They had to be — the pause was their creation. They needed that window to complete marking and reclamation.

"You think it's one of Warden's people?" Cole asked.

"Not sure." Jace shook his head. "But the pool of suspects just shrank. People who can do CAS operations aren't common. People who can move during a pause are even fewer. The overlap shouldn't be large."

Cole removed the lightweight lock from the door and pocketed it. From his spare locks, he took a fresh biased lock and hung it.

"You're not upgrading to something heavier?" Jace asked. "At least a heavyweight?"

"No need." Cole said. "The biased lock is enough. If they only came to probe, it means they weren't sure whether I was home. If they were sure I wasn't, they'd have broken in directly, not bothered with a CAS."

"But now they know — you discovered their probe."

"Let them know."

Cole went inside and dug out an old communicator from the back of a drawer. He hadn't used it in a long time — it was a dedicated channel for contacting Vera.

"You're calling Vera?" Jace leaned against the doorframe.

"I need Heap District intelligence." Cole adjusted the communicator. "If the visitor was active during the pause and they're a Sweeper, Vera might have leads."

"She might not want to help."

"She owes me a favor."

Jace raised an eyebrow but didn't press further.

The communicator crackled with static, then connected. A languid female voice came through: "This early in the morning, Cole. Something wrong with you?"

"Vera, I need you to look into something for me."

"What?"

"Today's pause at three-seventeen. Who maintained mobility during the pause?"

Silence for a beat on the other end.

"Why are you asking?"

"Someone touched my lock while I was frozen."

Another second of silence. Then Vera's tone shifted from languid to serious.

"The three-seventeen pause — theoretically, no one but the Sweepers could move. But I've received some strange reports. A few people claim they saw things during the pause they shouldn't have."

"What things?"

"Shadows." Vera said. "In the pause's gray ripples, people saw moving shadows. Not Sweeper shadows — human shadows."

Cole and Jace exchanged a look.

"I'll keep digging." Vera said. "But Cole — watch out for Donovan. A lot of things have been happening in his commercial zone lately. It's not coincidence."

The communicator went silent.

Cole put it back in the drawer and looked at Jace.

"Before we go to Donovan, there's somewhere else first."

"Where?"

"Slater's thread pool."

Jace blinked. "Why?"

"If someone can move during a pause, they need serious execution capability. That kind of power isn't something one person can have — they'd need an entire team behind them. And the only place in Lockhaven that can provide that kind of execution capability is Slater's thread pool."

"You suspect Slater?"

"No. I want to confirm whether Slater's workers were borrowed during the pause."

Cole pushed open the door and stepped into Stack Alley's morning mist.

The new biased lock clicked shut behind him. It didn't recognize the previous visitor's traces — it knew only Cole.

This time, Cole didn't look back.
