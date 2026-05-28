# Chapter 19: Ambush in Stack Alley

When Cole emerged from the Metadata Attic, he almost didn't make it out of Stack Alley alive.

The time was seven in the morning. He'd been working for nearly twenty hours straight. His body was running on fumes, but his mind was still spinning at full tilt. Vera's intelligence, Meta's modification approval, Quincy's unfair queue, Jace's CAS preparation—all the gears were turning; he just needed to make sure they meshed at the same moment.

Stack Alley's entrance lay twenty steps ahead. Cole's gait was unsteady, but his pace hadn't slowed.

On the fifth step, he felt it.

The air in Stack Alley had changed. Not the temperature—the density. The air grew viscous, as though something invisible was pressing against his body.

Cole reacted instantly—he sidestepped and reached for the lock tools at his belt.

But his hand was half a beat too slow.

A force surged from the depths of the alley on his left, like an invisible hand pressing down on Cole's shoulder. Not a physical attack—something deeper. Cole felt his thinking slow, his movements grow sluggish.

Recursion.

Someone was applying recursive pressure on him.

A recursion attack was one of the most insidious weapons in Lockhaven. It exploited the nature of thread stacks—every time a thread person executed a task, a new "stack frame" was created on the stack. Recursive calls kept creating new stack frames, layer upon layer, until the stack space filled up.

Normal recursion had an exit condition—once a condition was met, stack frames began unwinding one by one, and the thread person recovered. But if the recursion had no exit condition—

Stack overflow.

Cole felt the pressure building on his stack. One layer, two layers, three... his vision blurred, his limbs grew heavy. The attacker had somehow pushed massive numbers of useless stack frames onto his stack, like water being poured into a glass without stopping.

The glass was nearly full.

Cole forced himself to stay calm. The key to a recursion attack was the exit condition—without one, the stack would keep growing until overflow. He needed to find the attack's source and interrupt the recursion before his stack overflowed.

But his reaction speed was severely degraded. Even processing a simple logical thought took several seconds now.

Eighth stack frame. Ninth. Tenth.

Cole's hand was still in his pocket. His biased lock sat at his fingertips—but he couldn't muster the strength to pull it out.

"Cole!"

A voice from the distance. Sharp, urgent.

Then a rush of air—someone barreled in from the side, knocking aside the invisible pressing force.

Jace.

Cole felt the pressure on his stack drop sharply. Not because the recursion stopped—because someone was helping him release stack frames. Jace's fingers pressed against Cole's temple, cold as ice—he was using CAS operations to directly modify the control variables on Cole's stack.

"Don't move!" Jace shouted. "I'm modifying your stack frame counter—lowering the recursion depth limit. The frames he pushed in will pop off automatically."

Cole felt layers of pressure dissolving one by one. Ninth frame—popped. Eighth—popped. Seventh...

"Found the recursion's trigger condition." Jace said. "He planted a dead loop on your stack—every call creates a new frame and then calls itself again. No exit condition."

"Change it." Cole's voice was hoarse.

"Working on it." Jace's fingers flew across Cole's temple. "I'm replacing the call instruction with a no-op—when it gets called, it does nothing and returns immediately. The dead loop breaks."

Cole felt the last layer of pressure dissolve. His thinking sharpened, his body light again.

He straightened and turned toward the direction of the attack.

In Stack Alley's depths, a black silhouette was retreating rapidly.

"After him!" Cole shouted.

He and Jace surged forward simultaneously. But the attacker was fast—he clearly knew Stack Alley's terrain intimately, exploiting every corner, every crevice to the fullest.

Three alleys later, the attacker vanished at a T-junction.

Cole stopped, bent over, gasping.

"Lost him." Jace was breathing hard too. "But I don't care about that—how's your stack?"

Cole assessed his condition. Thinking clear, movements normal. Jace's CAS repair had been excellent—all anomalous stack frames had been purged.

"I'm fine." He said. "But that attack—not something an ordinary person could pull off."

"A recursion attack?" Jace's expression was grave. "Creating infinite recursion on a stack requires precise control of stack frame structure—not just anyone can do it. The attacker had to know your stack size, frame format, and calling conventions."

"Who knows my stack size?"

"Theoretically only you." Jace said. "But in practice—the cleaners record stack sizes when they scan thread people during pauses. If someone got hold of the cleaners' scan data—"

"Warden."

"Not Warden himself." Jace shook his head. "But his data—if someone copied his scan data without his knowledge—"

Cole remembered. Warden had said the cleaners' marking ripples covered the entire city during pauses. The ripples didn't just mark reclaimable objects—they scanned every thread person's status, including stack size.

If someone during a pause—someone other than the cleaners—had intercepted the marking ripple's data—

"Activity during pauses again." Cole murmured.

"But this time it's different." Jace said. "This attacker wasn't acting during a pause—he was operating during normal runtime. He could leave Segment Three, enter Stack Alley, and attack you."

"That means those thread people created by the class-loading device aren't just sitting in the Old Generation maintaining references. Some of them—have gained mobility."

The two locked eyes.

"They've evolved." Jace said. "Those thread people created by the class-loading device are no longer just tools. They've started attacking proactively."

Cole straightened.

"The plan doesn't change." He said. "But the timeline is tighter. If those thread people are attacking proactively, we're no longer fighting a machine. We're fighting an army."

He headed for Stack Alley's exit.

"To Segment Three." He said. "Before you finish prepping the CAS, I need to make sure there are no more ambushers inside."

Jace nodded once, and the two walked side by side toward the Heap District commercial strip.

Behind them, Stack Alley went quiet again.

But the air still carried the lingering aftertaste of the recursion attack—that viscous, oppressive sensation.

Like an invisible hand that had just relaxed its claws.
