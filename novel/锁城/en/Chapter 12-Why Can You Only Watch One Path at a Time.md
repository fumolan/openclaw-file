# Chapter 12: Why Can You Only Watch One Path at a Time?

Nova was no ordinary thread person in Lockhaven.

That much was obvious from the way she worked—other thread people handled one thing at a time, guarding one channel, processing one connection. Not Nova. She could track dozens, even hundreds of channels simultaneously, leaping to whichever one showed activity.

Her workspace was the communications tower in the Heap District's commercial strip—a metal lattice over thirty meters tall, topped by an observation deck open on all four sides. Inside the deck sat a semicircular console bristling with over a hundred small screens. Each screen corresponded to a communication channel.

When Cole found Nova at three in the morning, she was sitting cross-legged before the console, both hands flying across the touch panel. Data cascaded down the hundred-plus screens like waterfalls, and her eyes tracked every single one simultaneously.

"Nova." Cole stood beside the console for half a minute before she noticed someone was there.

"Oh, Cole!" Nova's face broke into a brilliant smile. She was twenty-two, round-faced, short-haired, with wide bright eyes—looked like a college student endlessly curious about the world.

"What are you doing?" Cole asked.

"Monitoring." Nova drew a circle with her finger, encompassing every screen before her. "One hundred twenty channels, all monitored at once. Impressive, right?"

Cole glanced at the screens. Indeed, one hundred twenty—each channel showing a different status: some transmitting data, some waiting for connections, some idle. Nova's monitoring method was distinctive: she didn't check channels one by one in rotation. Instead, she used a centralized dispatch console that received readiness signals from all channels simultaneously. Whichever channel was ready—incoming data, new connection, disconnect request—the dispatch console lit up, and she handled it instantly.

"Your dispatch console—" Cole pointed at the main screen in the center of the console. "It manages one hundred twenty channels at the same time?"

"Yep. That's my gift." Nova patted the console proudly. "Everyone else can only watch one path at a time. I can watch one hundred twenty simultaneously. No matter which path stirs, I know first."

"There's a problem with your approach." Cole said.

"What problem?"

"Ordering."

Nova's smile dimmed. "What about ordering?"

"You monitor one hundred twenty channels at once, but you process them in readiness order. Whichever's ready first gets handled first—you don't know which channel will be ready before the others."

"Right, so what?"

"If two channels become ready at the same time, which one do you handle first?"

Nova thought for a moment. "Whichever screen lights up first."

"What if both screens light up at the same time?"

"Uh—whichever one's closer to my hand."

Cole didn't smile. He stepped up to the console and looked at the one hundred twenty small screens.

"Nova, I have a task for you."

"What task?"

"I need you to monitor a set of special channels. Not communication channels—data transmission channels between the Heap District's Old Generation and the Metadata Attic."

Nova's eyes lit up immediately. "Special channels? Interesting. How many?"

"I'm not sure. Could be dozens, could be over a hundred. They're hidden—not routed through the public communication network. You'll need to scan and discover them yourself."

"Hidden channels? This is going to be fun!" Nova rubbed her hands with excitement. "You want me to find them?"

"Find them and monitor their data throughput." Cole said. "I need to know, at every moment, how much data is flowing between the Old Generation and the Metadata Attic, what type of data it is, and which direction it's flowing."

"How much time do I have?"

"Between now and tomorrow morning."

Nova paused. "That urgent?"

"Extremely urgent."

Nova dropped her playful demeanor. She fished a pair of earphones from beneath the console and put them on, shrinking the one hundred twenty screens into a virtual overlay on her left eye—her method was always keeping part of her attention on the regular channels while using the rest to scan new targets.

"What frequency range should I scan?"

"Full spectrum. Start from the bottom—the foundational architecture type definition band. That's the deepest layer of the Metadata Attic."

"The deepest layer? Isn't that restricted?"

"I know. But you're not an ordinary thread person." Cole said. "Your multiplexing ability lets you listen in on multiple channels without being detected. As long as you don't intervene—listen only, never transmit—you won't trigger any alarms."

Nova took a deep breath. "Listen only, no transmitting. Got it."

She closed her eyes and spread her hands across the console. The one hundred twenty small screens flickered in unison, then quickly reset. On the main screen, a brand-new scan interface opened—the frequency band range stretched from lowest to highest, like a fan unfolding.

"Starting scan." Nova said.

Her fingers danced across the touch panel. Every second, the scan covered dozens of frequency bands. Most were empty—no active data transmission in those regions. But occasionally, a faint glimmer flickered across a band—like a fish shadow gliding through deep water.

"Something's there." Nova's voice sharpened with focus. "Bottom of the band—foundational architecture type definition zone—there are a few weak signals. Not regular data transmissions, more like... heartbeats."

"Heartbeats?"

"Periodic pulse signals. Very regular interval—about every eight seconds."

Eight seconds. Cole immediately thought of the CAS counter he'd adjusted in Segment Three—the operation interval was also eight seconds.

"Track that signal."

Nova adjusted the scan parameters and locked onto the pulse signals. Thin lines appeared on the main screen—originating from the Old Generation's uppermost layer, threading through the Heap District commercial strip, and extending all the way to the Metadata Attic's base.

"Five channels." Nova said. "All starting from the Old Generation, terminating at the Metadata Attic's bottom layer. Low data volume, but continuous."

"What's the data content?"

"Incremental updates to type definitions." Nova's face changed. "Cole—these channels are injecting new foundational architecture type definitions into the Metadata Attic's bottom layer."

Cole's pulse quickened. Meta had said foundational architecture type definitions were read-only, untouched since the city's founding. But if someone was injecting incremental updates—

"Specifically what types?"

"Can't read them." Nova shook her head. "The format of these type definitions is unlike anything I've seen. Their naming doesn't follow Lockhaven's standard conventions—it looks like an external encoding scheme."

"External encoding scheme?" Cole's frown deepened. That meant these types weren't generated by Lockhaven's internal rules—they were imported from the outside—beyond the city.

"There's something else." Nova's voice dropped. "The data flow direction on these five channels isn't only Old Generation to Metadata Attic. One channel is bidirectional."

"Bidirectional?"

"Data flowing from the Metadata Attic to the Old Generation." Nova pointed to a thin red line on the screen. "The Attic is sending some kind of instruction to the Old Generation."

"What instruction?"

Nova traced the red line's endpoint. The data stream converged at a specific location in the Old Generation—its center, the densest cluster of leaked objects.

"The instruction content is—" Nova's finger slid across the screen, decoding the data—"Maintain references."

Two words froze the air in the communications tower.

Maintain references.

The Metadata Attic—or rather, some compromised part of it—was sending "maintain references" instructions to the leaked objects in the Old Generation. That was why their reference chains never broke: it wasn't that the reference relationships themselves were unbreakable, but that an external instruction was continuously sustaining them.

"Cole." Nova looked up, the usual humor gone from her eyes. "This isn't normal. The Metadata Attic shouldn't send instructions to any objects. It's only supposed to store type definitions."

"But it's been modified." Cole said. "Someone planted new type definitions in the Attic's deepest layer—definitions that gave the Attic new capabilities. It's no longer just a storage center. It's become—"

"A controller."

Cole nodded.

"Nova, keep monitoring these five channels. Log everything—data volume, transmission frequency, content changes. Especially the red channel—the 'maintain references' instruction—I need its frequency and pattern."

"You want me to find its rhythm?"

"I need to know what happens if I cut that red channel."

Nova thought for a moment. "If you cut the 'maintain references' instruction—those objects might lose their external maintenance, and the reference chains would revert to normal behavior. Then the cleaners could reclaim them."

"But it's also possible—"

"The reference chains could snap abruptly, causing a cascading collapse." Nova finished his thought.

They locked eyes.

"So we can't just cut it." Cole said. "We need a safe way to sever the connection."

"That means I need to analyze the red channel's instruction pattern—find its cycle and critical nodes. If we can cut it between two instructions—"

"Like surgery. Making the incision between two heartbeats."

Nova nodded firmly. "Give me time. I'm analyzing."

Cole tapped the edge of the console and turned to leave.

"Cole." Nova called after him.

"Yeah?"

"That path you mentioned—the problem of only watching one path at a time." Nova looked at him earnestly. "I can watch one hundred twenty paths at once. But you're right—I don't know which comes first. If you need me to watch a specific path at a specific moment—you have to tell me in advance."

"I will."

"And—Cole." Nova's voice grew smaller. "Those three hundred forty-seven people not on the list—are they on this path too?"

Cole looked at her young face.

"They are." He said. "They're on every path."

Nova lowered her head and returned to her console. The light of one hundred twenty small screens reflected on her face like one hundred twenty unblinking stars.

She was back in her world—a world where she could see one hundred twenty paths at once.

But for the first time, she was beginning to fear that not all paths could show their endings at the same time.
