# Chapter 21: Only One Person Can Touch It at a Time

9:50 AM.

Ten minutes until Wyatt released the write lock.

Everyone was in position. Cole at the Segment Three entrance. Jace beside the class-loading device inside Segment Three. Nova at her monitoring console in the communications tower. Warden with his cleaners on standby in the Old Generation. Quincy at the central console in the plaza. Vera at her intelligence station in the commercial strip.

Only one person hadn't shown.

Donovan.

Cole stood before the Segment Three entrance, looking at the sealed passage door. The heavyweight lock held firm, an impenetrable wall.

But Cole had no intention of going through the front door.

He circled around to the partition wall between Segments Three and Four—the narrow door he and Jace had used last time. It still bore a lightweight lock. Cole reached out and performed a CAS—read state, compare, swap.

Passed on the first try.

He slipped through the narrow door, crossed the pitch-black corridor, and entered Segment Three's interior.

The data cables were denser than last night. The light flowed visibly faster—the class-loading device was ramping up, preparing for the imminent write window.

Cole didn't head for the device. He stopped at a crossroads in the corridor and reached for the lock tools at his belt.

Biased lock—the lightest lock. But today a biased lock wouldn't do. The crossroads was a shared junction with multiple paths converging. A biased lock only worked for single-person passage. This position required stronger control.

He pulled out a lightweight lock. A turnstile pattern flickered across the lock face. Lightweight locks were acquired through CAS—read the current state, and if unoccupied, swap in your own marker.

Cole executed a CAS. The lock face clicked and belonged to him.

But that wasn't enough.

He didn't need passage—he needed a blockade.

The crossroads was Segment Three's traffic hub. Every data cable, every task distribution channel, every reference-maintenance instruction passed through here. If Cole locked down this junction—

Segment Three's internal traffic would be severed.

But a lightweight lock only prevented others from acquiring the junction via CAS. If someone brought a heavier lock—say, a heavyweight lock—to forcibly seize it—

Cole needed to upgrade.

He pulled a heavyweight lock from his tools. This wasn't something he normally used—heavyweight locks were expensive, requiring operating system mutex support. But at a critical moment, they were the most reliable choice.

He removed the lightweight lock from the junction and replaced it with the heavyweight.

The lock face settled with a heavy thunk and emitted a low hum.

Now the crossroads was sealed by a heavyweight lock. No one could bypass it with CAS—heavyweight locks didn't use the CAS channel. To get through, you needed the lock's key, or you waited for Cole to release it voluntarily.

"Cole." Nova's voice came through his comm. "You've put a heavyweight lock on the Segment Three crossroads."

"Correct."

"You've cut Segment Three in half. The device is on the south side, the data cable exit on the north. The south-side device is still running, but the north-side exit is blocked. Instructions from the device can't get out."

"That's the point."

"But the device will detect transmission failure." Nova said. "It might enter self-preservation mode—accelerate loading all remaining types."

"Let it accelerate." Cole said. "The south-side device can run as fast as it wants—instructions that can't transmit means reference maintenance is spinning its wheels."

The comm went silent for a second.

"Cole—Donovan's coming."

Cole looked up.

From the direction of Segment Three's entrance, footsteps approached.

Donovan appeared at the far end of the corridor. He wore a dark gray robe, his face composed. But beneath the composure, Cole caught a trace of tension.

"Cole." Donovan stood at another crossroads—the south segment's entrance. "You've sealed off the north-side junction."

"I have."

"Why?"

"Only one person can touch it at a time." Cole said. "Segment Three's traffic has to stop."

Donovan looked him in the eye.

"Do you know what you're doing?" He said. "You've blocked the north side, but I'm standing on the south side. The device is on the south side too. I just need to reconnect a data cable, bypass your blockade—"

"You can try." Cole said. "But before you reconnect anything, there's something I need to tell you."

"What?"

"Your platform-level token is about to become invalid."

Donovan's expression didn't change. But his right hand—the one that had been hanging at his side—curled slightly into a fist.

"What do you mean?"

"Vera told me that three years ago she gave you the platform-level token. You used it to plant incremental updates in the Metadata Attic's bottom layer—modifying foundational architecture type definitions. That's how you were able to build a custom class loader."

Donovan was silent.

"But this morning, I submitted a modification request through Quincy's queue to Meta—to strip your platform-level guardian attribute. Meta has approved it. The token is being unbound from your identity as we speak."

"Impossible." Emotion finally crept into Donovan's voice. "Type definition modifications take time—"

"Quincy activated unfair mode. My request skipped the entire queue."

Donovan's face changed. He finally realized—Cole hadn't been fighting alone. The entire city was behind him.

"Even if the token is invalidated—" Donovan's speech quickened, "the incremental updates have been accumulating for three years. The Attic's bottom layer needs time to clean up increments—"

"Meta has already launched concurrent cleanup mode."

Donovan's body stiffened for an instant.

"You—how long did you spend preparing this?"

"Twenty hours." Cole said. "Enough."

9:58 AM.

Two minutes until Wyatt released the write lock.

Donovan stood at the south segment's entrance. Cole stood behind the blockade at the north-side junction. Between them lay Segment Three's complex data cable network and a crossroads sealed by a heavyweight lock.

"Cole." Donovan's voice was calm again, but beneath the calm was the ruthlessness of a cornered animal. "You think blockading one crossroads stops me? Segment Three is my territory. I know where every data cable lies better than you ever will."

He turned and walked toward the device.

"What are you doing?" Cole shouted.

"Accelerating." Donovan didn't look back. "Since the north side is blocked, I'll concentrate all south-side resources on one point—full-speed class loading. You堵 one path, I have another."

He reached the device.

Cole watched his back. If Donovan hit full acceleration, new type loading speed would double—even with the north side sealed, the south side was a complete system in itself. It could create types and instantiate objects internally, just unable to send reference-maintenance instructions to the Old Generation.

But Donovan didn't need to send instructions. He just needed to create more objects—stuff the Old Generation full. Once full, Full GC would be unavoidable.

"He's going to force a Full GC another way." Cole said into his comm.

"I know." Jace's voice came from a corner beside the device—he'd been hiding there the whole time. "But I'm already in position."

10:00 AM.

Wyatt released the write lock.

Cole didn't know the exact instant Wyatt pulled the switch, but he knew it had happened—because Nova shouted into the comm.

"The anomalous write window is open!"

In Quincy's queue, a full day's backlog of anomalous write requests flooded in. Under unfair mode, requests didn't queue first-come, first-served—they grabbed resources on arrival. Wave after wave, like surf pounding the shore.

"First wave—past." Quincy's voice was calm and fast. "Gap between peaks—six hundred milliseconds."

"Enough." Jace said.

His hand rested on the feedback loop's data cable beside the device.

"Signal incoming." Nova said. "Confirmation signal—0xAA—transmitting. Distance to nearest node: three, two, one—"

Jace's CAS completed within the two-hundred-millisecond window.

Read—0xAA. Compare—0xAA. Swap—0x00.

"Round one complete." Jace said. "Feedback signal replaced. The device received 'references broken.'"

The device's lens rotation slowed for an instant—it was processing the anomalous feedback.

"It's hesitating." Nova said. "By design, if thirty consecutive rounds of feedback come back 'references broken,' the device will conclude the reference chains have naturally failed and stop maintaining."

"Next round." Jace said.

Five seconds later—round two.

CAS. 0xAA→0x00.

The device's lens rotation continued to slow.

Round three. Round four. Round five.

Every CAS from Jace was flawless. Two-hundred-millisecond window, he needed less than fifty. Nova's positioning was pinpoint accurate every time.

"It's decelerating." Suppressed excitement crept into Nova's voice. "The device's reference-maintenance frequency is dropping."

Round ten. Round fifteen. Round twenty.

The device's lens spun slower and slower. Its hum dropped in pitch—from a high whine to a low rumble.

"Reference-maintenance instruction frequency—down from every five seconds to every fifteen." Nova reported.

Round twenty-five.

The device's lens stopped.

"Reference-maintenance instructions—transmission ceased." Nova said. "The Old Generation's leaked objects—their reference chains have lost external maintenance."

Cole closed his eyes for a moment.

He looked toward the south segment. Donovan stood beside the device, face pale.

The device no longer sent reference-maintenance instructions. But it was still running—Donovan was accelerating class loading. Even with maintenance stopped, new types kept loading.

"Warden." Cole said into the comm. "Reference maintenance is severed. You can begin."

In the Old Generation's direction, the cleaners' marking ripples flared to life.

Not ordinary marking ripples—the intensified ripples Warden had promised, concentrated directly below the direct memory region.

The ripples pierced through the Old Generation's ceiling and surged toward the direct memory region above.

Inside direct memory, the hidden channel that had been maintained for three years—the data line from the class-loading device to the Metadata Attic's bottom layer—shuddered violently under the ripple interference.

"Channel disrupted!" Nova shouted. "Data transmission interrupted—no, not interrupted—degraded. The channel's still there, but bandwidth has plummeted. Incremental update push speed—"

"How much did it drop?" Cole asked.

"Eighty percent." Nova said. "Meta's concurrent cleanup is outpacing the incremental push. She's winning."

Cole looked at Donovan.

Donovan had heard the comm traffic too. His face went from pale to ashen.

He'd lost.

But he hadn't given up.

Donovan's hand reached for the device's control panel. His fingers moved rapidly—he was activating the device's last line of defense.

"What's he doing?" Cole shouted.

"He's initiating full-volume loading!" Jace jumped up from beside the device. "He's going to load all remaining type definitions at once!"

Full-volume loading—the class-loading device's ultimate self-destruct mode. Injecting every unloaded type definition into Lockhaven in a single burst. Not incremental updates—a data flood.

If the flood surged in—the Old Generation would fill completely within minutes.

"Stop him!" Cole shouted.

Jace lunged toward Donovan. But Donovan reacted faster—he pulled a lock tool from his robe and hurled it at Jace.

A biased lock. Spinning through the air, straight at Jace.

Jace dodged sideways. The biased lock struck a data cable, sending sparks flying.

In that gap, Donovan pressed the final key on the panel.

The device's lens whirled to life—faster than ever before.

"Full-volume loading initiated!" Jace shouted.

Cole watched. The heavyweight lock at the crossroads still sealed the north side—but full-volume loading was routed through the south. The north-side blockade was useless against it.

He had to choose.

Stay behind the blockade—protect the north side's safety.

Or—rush the south side and shut down the device before full-volume loading completed.

Cole didn't hesitate.

He released the heavyweight lock.

The crossroads opened.

He charged through.
