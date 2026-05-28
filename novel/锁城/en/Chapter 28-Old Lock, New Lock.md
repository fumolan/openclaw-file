# Chapter 28: Old Lock, New Lock

When Cole returned to his quarters in Stack Alley, the biased lock was still on the door.

But its state was wrong.

After the events of the past few days—probing, attacks, recursion—the biased lock had undergone multiple upgrades and downgrades. It was now in lightweight lock state, no longer the original biased lock.

Cole stood at the door, looking at the revolving gate pattern on the lock face.

He could revert it to a biased lock. Biased locks were the lightest—so long as only one person used the door, it was the fastest way through. No extra operations needed for daily entry and exit.

But he could also leave it.

The past few days had taught him something: a biased lock's assumption was "only one user." Most of the time, that assumption held. But when it failed—when someone came probing, attacking—the upgrade process itself leaked information.

The prober had confirmed Cole's door was accessible precisely by triggering the biased lock's upgrade.

What if he kept it as a lightweight lock?

A lightweight lock had slightly more daily overhead than a biased lock—every door opening required a CAS operation. But a lightweight lock didn't depend on the "only one user" assumption. Even if someone probed, a lightweight lock wouldn't go through the dramatic escalation that a biased lock would.

Cole thought about it.

Then he made a decision—don't revert to biased lock.

He reached out and performed a CAS on the lightweight lock. The lock face recognized his mark, and the door opened.

Inside, he found something unexpected—a package on the table.

No sender information. Just one line: "For Cole."

He opened it.

Inside was a lock. Not a biased lock, not a lightweight lock, not a heavyweight lock.

It was a lock he'd never seen before.

The lock face bore a complex pattern—not a revolving gate, not a sealed checkpoint. More like a—ticket. The pattern had a serial number field, a timestamp field, and a checksum field.

Cole turned the lock over in his hands for a long time.

Then he understood.

It was a StampedLock—the newest lock design in Lockhaven. It worked completely differently from traditional locks.

Traditional locks—biased, lightweight, heavyweight—were all based on a "lock-release" model. You lock the resource, use it, then release it. While locked, no one else can touch it.

This new lock didn't follow that model. It issued a "ticket" for each operation—each ticket carried a timestamp. When you picked up the ticket, you didn't lock anything—you just went and read the data. After reading, you brought the ticket back to the lock for validation: had anyone modified the data while you were reading?

If no one had—your read was valid. No locks involved at all.

If someone had—your ticket was invalidated, and you had to start over. But this time, you'd need to actually acquire a lock and read again.

Cole considered the advantages of this design.

Most of the time—no one was modifying data. So most of the time, read operations needed no locks at all. No CAS, no mutual exclusion, no waiting. Read, validate, done.

More efficient than a read-write lock. Because even though a read-write lock allowed concurrent reads without mutual exclusion, the read lock itself still had overhead—you had to acquire and release it. This new lock didn't even need a read lock.

"Optimistic read." Cole murmured.

Optimistic—assuming most of the time there would be no conflicts. Only locking when a conflict actually occurred.

This was a different philosophy from biased locks. Biased locks assumed "only one user"—when the assumption failed, they escalated to heavier locks. This new lock assumed "no conflicts"—when the assumption failed, it fell back to traditional locking.

Optimistic was more—practical.

Cole held the new lock and thought about the whole incident. If he'd been using this lock from the start—when someone came probing, he wouldn't have needed to trigger any lock escalation at all. The prober would get a ticket, read the data, validate—and find the data had changed, so they'd start over. Cole wouldn't even need to know the prober existed. The lock handled it.

No biased-to-lightweight escalation. No lightweight-to-heavyweight escalation.

The entire process was smooth.

Cole set the new lock on the table. There was a note inside the package.

"Your old lock is too heavy. Try something lighter.—A friend."

No signature. But Cole had a pretty good idea who.

Not many people in Lockhaven could design a new lock mechanism. Grant was one—he'd been optimizing container locks. But this lock's design style wasn't Grant's.

It was more like—Quincy.

Quincy managed the underlying AQS mechanisms. All locks ultimately relied on his queuing rules. If anyone could design a lock that didn't need a queue—

That was what Quincy had always pursued.

Fairness was good. But fairness meant queuing. Queuing meant waiting.

If there were a way to skip the queue—not through unfair cutting, but through optimistic assumptions—

Most people, most of the time, didn't need to queue.

Cole put the new lock away.

He wouldn't install it yet—the lightweight lock on his Stack Alley door, upgraded from biased, was sufficient. New things needed time.

But he'd remember this lock.

Remember the concept of "optimistic."

Remember—that most of the time, rules didn't need to be so strict. Be optimistic, verify occasionally. Lighter than locking everything, safer than releasing everything.

Outside the window, the Heap District's commercial lights flickered in the night.

Cole closed the door. The lightweight lock clicked shut behind him.

Not a biased lock. Not a heavyweight lock.

Just enough.

That was another thing he'd learned: just enough was better than both over-fortification and over-openness.

The measure of a lock wasn't how heavy it was—but how right it was.
