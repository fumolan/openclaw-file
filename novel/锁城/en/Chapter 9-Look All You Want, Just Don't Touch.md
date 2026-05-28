# Chapter 9: Look All You Want, Just Don't Touch

Cole didn't go straight back to Segment Three.

He went to find Rhea and Wyatt first.

The Read-Write Lock family lived in the Heap District's commercial strip, South Zone, in a pair of twin towers. The buildings were identical, but their entrances faced opposite directions. The left tower's door bore an engraving of an eye—the read channel. The right tower's door bore a hand—the write channel.

When Cole arrived, Rhea was standing at the left tower's entrance, chatting with a group. Seven or eight thread people surrounded her, some flipping through data cards in her hands, others pulling up her public information streams on portable terminals.

"Look all you want, just don't touch." Rhea waved dismissively at the people around her when she saw Cole approaching. "Cole, you here to read too?"

"I need the Old Generation's recent read-write operation records."

"Read records, no problem." Rhea pulled a transparent crystal orb from her pocket. "Everything read-related in the Old Generation for the past week is in here. Take your time."

She handed Cole the orb. He cradled it and rotated it in his palm—strings of data materialized inside, each turn revealing a different time window.

"But for write records, you'll need to find Wyatt." Rhea added.

Cole nodded and was about to head for the right tower when Rhea called after him.

"Cole—Wyatt's in a foul mood today."

"When is he ever in a good mood?"

"Today's worse than usual." Rhea's expression turned delicate. "He says someone's been altering Old Generation data behind his back."

Cole stopped. "Someone's bypassing the write channel to modify data?"

"Not bypassing. Modifying when he's not operating—when the write channel is idle—using some other method. Not through his write channel at all."

That meant someone had established an alternative write path outside Wyatt's write channel. Under read-write lock rules, when the write channel wasn't held, the read channel allowed multiple people through simultaneously. But if someone bypassed both channels entirely and modified data directly—the read-write lock couldn't detect it at all.

"Does he know who?"

"No. But he's furious." Rhea lowered her voice. "Be careful. When he's angry—the entire right tower becomes a no-go zone."

Cole walked toward the right tower. The hand motif on the door cast a long shadow under the lights. He was about to knock when the door opened from inside.

Wyatt stood in the doorway. Half a head shorter than his sister, but carrying a heavier presence. Gloomy face, deep-set eyes, constantly darting gaze—like a cat perpetually on alert.

"Cole." His voice was low. "You're late."

"Late for what?"

"If you're here about the Old Generation's write operation anomalies—I've already looked into it." Wyatt stepped aside to let Cole in.

The right tower's interior was nothing like the left. The left was open-plan, dotted with reading seats and screens everywhere. The right was sealed—heavy walls, no windows, just one long corridor lined with tightly shut doors.

"The write channel shares the same lock with my sister's read channel." Wyatt walked as he talked. "When I'm operating—that is, when I hold the write lock—her read channel must close as well. No one can read and write at the same time. Period."

"But someone's bypassed that rule."

"Not bypassed. They never went through my door in the first place." Wyatt stopped at one of the doors and pushed it open.

Inside was a massive monitoring screen displaying a heat map of all write operations across the Old Generation. Under normal conditions, the bright spots should have been clustered only at the write channel positions Wyatt controlled. But right now, a dozen scattered hot spots dotted the map—not on the write channels, but distributed across various corners of the Old Generation.

"These bright spots are unauthorized write operations." Wyatt's voice trembled with suppressed fury. "In the past three days, huge numbers of new objects have been written into the Old Generation. None of these writes went through my write channel. I was never notified."

"How?"

"I don't know." Wyatt's fists clenched. "My write lock is exclusive. As long as I hold it, no write should occur. But these writes all happened while my write lock was released."

"You released the write lock?"

"Of course I released it. I don't hold it forever. After a write operation completes, I release the lock so the read channel can operate." Wyatt walked to the screen and pointed at several bright spots. "But the timestamps of these unauthorized writes—every single one falls within seconds after I released my write lock."

Cole studied the timestamps. It was true—every anomalous write occurred right after Wyatt released his lock. The interval was razor-thin, just a few seconds.

"Someone is exploiting your timing gap." Cole said.

"What do you mean?"

"Your write lock and Rhea's read lock are two faces of the same lock. When you hold the write lock, the read channel is closed. When you release it, the read channel opens. But in the gap between your release and the read channel reopening—there's a window of a few seconds."

"During those few seconds, the read channel is open." Wyatt frowned. "But the read channel is read-only. You can't write through it."

"Right—if you're using the read lock's official channel. But what if someone isn't going through the read lock at all? What if they're manipulating the underlying data directly?"

Wyatt's face changed.

"You mean someone is operating at a level below the read-write lock?"

"Not below it. Outside it." Cole said. "The read-write lock governs read and write operations through official channels. If someone built their own channel—say, a custom class-loading channel—they wouldn't need to go through your write lock at all."

Wyatt was silent for a long time. His hand rubbed the edge of the screen repeatedly, knuckles whitening.

"Cole," he finally spoke, "if someone really built their own channel outside the read-write lock—then my write lock, my sister's read lock, our entire twin tower—"

"Are all window dressing."

Wyatt took a deep breath. "Tell me who that person is."

"I'm working on it. But I need a favor."

"What?"

"From now on, don't release your write lock. Hold it. Permanently."

Wyatt stared. "Permanently? That shuts down the read channel completely. My sister—"

"I know. But if you hold the write lock continuously, the person exploiting the timing gap loses their window. They'll either have to switch to a different method—which leaves more traces—or stop operating entirely. Either outcome works in our favor."

"How long do you want my sister's read channel shut down?"

"One day. Maximum."

Wyatt looked at the scattered bright spots on the screen and slowly unclenched his fists.

"Fine." He said. "One day. You find that person. After that, I'm done."

He walked to the monitoring console and pulled the write-lock hold switch.

From the direction of the left tower came Rhea's startled cry—all the read channel lights had gone dark.

Wyatt didn't look back. "I'll explain it to her."

Cole stepped out of the right tower and stood in the open space between the twin buildings.

The left tower's door flew open with a bang. Rhea burst out. She spotted Cole and her eyes went wide.

"Cole! What did you say to my brother? Why is my read channel shut down?"

"Temporary measure." Cole said. "One day."

"One day?! I've got over thirty people reading data on my side!"

"Tell them to come back tomorrow."

Rhea took several deep breaths, visibly fighting to contain her anger. "You'd better have a damn good reason."

"I do." Cole said. "But now's not the time to explain."

He turned and walked away. Rhea shouted something after him, but he didn't catch it.

Closing the read channel would cause a chain reaction across the Old Generation—many operations that relied on real-time reads would be forced to suspend. But that was a necessary price.

If the window for anomalous writes was sealed, the hidden operator would have to switch methods. And a new method meant new traces.

Cole quickened his pace. He still had a lot to do.

The supply queue blockage needed resolving. Donovan's Segment Three needed handling. Vera's tracing results were pending.

And Meta.

The woman who knew all the secrets—he'd have to face her sooner or later.

In the distance, the sky above the Old Generation was darker than it had been during the day. Deep gray clouds pressed low, like a heavy ceiling.

A few more cracks had appeared in that ceiling.
