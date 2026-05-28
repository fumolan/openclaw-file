# Chapter 25: The Cleaner's Choice

Warden had been waiting in the Old Generation for a long time.

He stood with over twenty Cleaners in the central plaza, waiting for Cole's signal. The marker ripples still pulsed beneath the direct memory area—disrupting the hidden channels effectively, but at a steep cost. The Cleaners had maintained enhanced ripples for over twenty minutes, and exhaustion was written across every face.

"Cole." Warden said into the comm. "What's the status?"

"Token spent. Incremental updates cleared. Three hundred forty-seven illegal thread-people are exiting." Cole's voice came from the Attic, tinged with fatigue. "Reference chains are detaching. The reference chains on the leaked objects are decaying."

"How long until full decay?"

"Per Vera's estimate—the fastest objects will lose all references within minutes. The slowest could take an hour or two."

"An hour or two." Warden repeated. "Can the Old Generation hold that long?"

"Old Generation current utilization—ninety-seven percent." Nova reported from the comm tower. "At the current expansion rate, we'll hit one hundred percent in—forty minutes."

Forty minutes. One hour of decay wouldn't be enough.

"Can the reference decay be accelerated?" Warden asked.

"Yes." Vera's voice joined in. "If the Cleaners can perform a mark operation—not collection, just marking—tag all dereferenced objects as 'reclaimable.' The marking itself accelerates reference decay, because the scan leaves traces on the objects' reference chains, and those traces weaken the reference strength."

"Mark without collection—that's safe."

"Correct. Marking only identifies reclaimable objects without actually reclaiming them. But the scanning during the mark process accelerates reference decay."

Warden looked at his Cleaners. They were exhausted. But this time, they didn't need to do a full collection—just marking.

"Everyone listen up." Warden's voice was loud and steady. "No collection. Marking only. Target—all leaked objects in the Old Generation that have lost their references. Report when finished."

The Cleaners raised their marking poles.

"Begin."

Over twenty poles emitted gray light simultaneously. The glow radiated outward from the plaza in every direction, covering every corner of the Old Generation. As the ripples swept past the spheres of light—the leaked objects—Cole could clearly see the change.

The fine red threads on the spheres' surfaces dimmed beneath the gray ripples. Some snapped outright—the ripple scan severed the threads that maintained the reference relationships. Others didn't break but grew thin, weak.

"Reference decay accelerating." Vera reported. "Estimated time to full decay—reduced from one hour to twenty minutes."

Twenty minutes. That would do.

Warden stood in the center of the plaza, watching the marker ripples spread. His gray eyes reflected the gray light.

"Cole." he said. "I made a choice."

"What choice?"

"This marking run—it's not a Full GC." Warden said. "I chose not to do a Full GC."

"You didn't need to do a Full GC in the first place."

"I did." Warden said. "The Old Generation utilization was at ninety-seven percent. By standard protocol, I should have triggered a Full GC—city-wide pause, full collection. But you said you could fix it. I believed you."

"You believed in a thirty-percent chance?"

"I believed in the person making the decision." Warden said. "A Cleaner's job isn't to judge right or wrong—it's to clean what needs cleaning. But when to clean, how to clean—that decision shouldn't come from a Cleaner."

He watched the red threads fading in the ripples.

"Three years ago—no, longer—since Lockhaven was founded, Cleaners have always been the passive side. The city produces garbage, and we sweep it up. Nobody asked where the garbage came from, nobody thought about reducing it. We just handled the last step—collection."

"Are you reflecting?"

"I'm thinking—if three years ago someone had noticed Donovan's anomalies, if someone had caught the first incremental update when it appeared—"

"We wouldn't be here today."

"Right." Warden said. "But nobody noticed. Because Cleaners only collect. We don't monitor. We only see the result—more and more garbage—but never the cause."

"That will change." Cole said.

"How?"

"Every time the Cleaners' marker ripples sweep across the city, they scan every object's status. That scan data includes more than which objects are reclaimable—it shows which objects have abnormal reference patterns, which objects have unknown creation sources, which objects are growing abnormally in size."

"You're saying—Cleaners should become the city's monitoring system?"

"Not a monitoring system. An early warning system." Cole said. "Marker ripples aren't just cleaning tools—they're diagnostic tools. If Cleaners record the distribution and changes of anomalous objects during each mark pass, they can catch warning signs before problems erupt."

Warden was silent for a long time.

"You mean—Cleaners shouldn't just be the cleanup crew at the end of the line."

"Right. Cleaners should be the city's eyes."

Warden looked at the marking pole in his hand. Gray light flickered at the tip, reflecting off his weathered face.

"I'll think about it." he said.

The marker ripples gradually faded across the Old Generation. Most of the red threads on the light spheres had snapped or decayed to near-nothing. The leaked objects' reference chains were collapsing at an accelerated pace.

"Old Generation utilization—ninety-four percent." Nova reported. "Leaked objects beginning to be naturally collected. Space is being freed."

Ninety-four percent. Down from ninety-seven. The trend was right.

"How long until we reach safe levels?" Cole asked.

"If references continue decaying at the current rate—about fifteen minutes. After that, the Cleaners can do a normal Minor GC to collect the leaked objects that have lost their references. Space reclamation will be fast."

"Then we wait fifteen minutes." Cole said.

He disconnected and walked from the Metadata Attic's bottom level toward the exit.

The spiral staircase stretched beneath his feet. Type definitions on the walls were slowly returning to their original state—the tampered panels had been wiped clean, restored to their founding condition.

Fifteen minutes.

In fifteen minutes, this three-day crisis would be over.

No Full GC. No city-wide pause. No hundreds of people vanishing.

Cole reached the Attic's exit and pushed through the transparent barrier.

The Heap District's commercial strip unfolded before him, its lights brighter than at dawn—the Old Generation's space reclamation was already restoring power to the commercial strip. The lights would only get brighter.

He descended the Attic's steps and stood in the commercial strip's corridor.

In the distance, the Old Generation's sky was still gray. But threading through the gray was a trace—faint, barely perceptible—of blue.

The cracks were healing.

Cole stood there, watching the sky change color.

He remembered the last thing Donovan said.

He hadn't heard it clearly.

But he could guess.

"I just wanted to prove this system couldn't hold."

Donovan had used the wrong method to prove something right.

Lockhaven's infrastructure was indeed aging. The type definition loading mechanism, memory management capacity planning, the way Cleaners worked—all of it needed to change.

But change didn't require gambling the entire city.

It could be done with a thirty-percent chance.

One step at a time.

In the distance, the Cleaners' marker ripples performed one final scan. After the ripples came a gentle, normal Minor GC.

Pause time—under three seconds.

No one vanished.

Cole closed his eyes.

It was over.
