# Chapter 29: The Types That Were Erased

Three days after the incident, Meta conducted a comprehensive type audit in the Metadata Attic.

Cole was invited to attend. It was his second time in the Attic—the first had been the bottom level to roll back incremental updates; this time, the upper level to review the audit results.

The audit results were better than expected.

Of the three hundred-plus malicious incremental updates, twenty base incrementals had been safely rolled back, one hundred eighty auto-deleted by the Attic, and the remaining hundred cleared through cascade deletion. The erased type definitions affected approximately fifteen percent of Segment Three's data structures, but other areas were virtually untouched.

"Damage assessment." Meta stood before the crystal screen, her voice as cool as ever. "Type definition integrity rate: ninety-seven percent globally. Segment Three, eighty-two percent. All other areas, above ninety-nine percent."

"That eighteen percent in Segment Three—"

"Already covered by Grant's segmented reconstruction." Meta said. "He filled the cleared areas with standard type definitions. Different functionality than before, but a safer structure."

"So—no permanent damage?"

"There is." Meta said. "A hundred force-deleted type definitions won't be coming back. All objects and data associated with them are gone."

"What kind of objects?"

"Primarily operational data from Donovan's commercial district—transaction records, customer information, inventory data from Segment Three." Meta said. "All of Donovan's business activity records from the past three years have been wiped."

Cole thought for a moment. "This data—"

"Gone." Meta said. "Force deletion is irreversible."

Cole was silent for a while.

Donovan's commercial empire had lost all its operational data overnight. The sixteen segments remained, but Segment Three's memory had been wiped clean.

Like a person losing three years of memory. The person was still there, but the past was gone.

"There's one more thing." Meta said.

"What?"

"Class unloading." Meta said. "The malicious types created by Donovan's class-loading device—their type definitions became orphan types after the incremental updates were cleared. Orphan types need to be unloaded—completely removed from the Attic."

"Is the unloading complete?"

"Mostly." Meta said. "But class unloading has a prerequisite—the class loader that loaded the type must be collected first."

"The class-loading device has been destroyed."

"Yes. The device is gone, but it wasn't a standard class loader—it was Donovan's custom one. Custom class loader collection requires specific conditions—no active instances, no references pointing to it, and the loader's definer—"

"Donovan is gone."

"Correct. With the definer gone, the loader becomes orphaned. Orphaned loaders can be collected, but it takes time."

"How long?"

"Already in progress." Meta said. "Warden's Cleaners check for unloadable orphan types during each marking pass. A few unloaded each time, gradually clearing them. Estimated—one week for full completion."

One week.

In one week, every trace Donovan had left—malicious types, leaked objects, custom class loaders—would be gone from Lockhaven completely.

As if they had never existed.

Cole stood in the Attic's upper level, looking out the window. From here he could see the entire Heap District—Stack Alley at the bottom, the commercial strip in the middle, the Old Generation above.

The Old Generation's sky had returned to its normal color—no longer gray, no longer dark red. A calm, cool blue.

The cracks remained, but they were healing slowly.

"Meta." Cole said.

"Hmm."

"Before Donovan disappeared—he said something. I didn't catch it."

Meta looked at him.

"You want to know what he said?"

"Can you find out?"

"A thread-person's last words before vanishing aren't recorded." Meta said. "That's private. It belongs to them."

Cole nodded.

"But if you want to guess—"

"I already have."

Meta didn't press further.

Cole turned toward the spiral staircase. On the way down, he passed the Attic's middle level—where all currently active type definitions were stored.

He stopped in front of one panel.

The panel bore a type definition—the standard type for thread-people. Every thread-person—including Cole himself—had been created from this type.

At the edge of the type definition, a line of small text: Creator—Boot Level. Immutable.

Immutable.

Lockhaven's foundational architecture—including thread-people themselves—had been set at the city's founding. Unchangeable.

Donovan had tried to change it. He'd failed.

But his failure raised a question: what if one day, the foundational architecture truly needed to change? What if the thread-people's type definition itself no longer served the city's needs?

Immutable—protection, or shackle?

Cole had no answer.

He continued down the stairs.

Behind him, the word "Immutable" on the panel glowed quietly in the Attic's light.

Like a closed door.

What lay behind it?

Cole didn't know.

Maybe one day he would.

Maybe he didn't need to.

Today was not that day.
