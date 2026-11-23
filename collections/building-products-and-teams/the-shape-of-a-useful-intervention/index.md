Title: The shape of a useful intervention

[Read HTML](https://getharsh.in/collections/building-products-and-teams/the-shape-of-a-useful-intervention/)

Author: Harsh Joshi

<a id="the-shape-of-a-useful-intervention"></a>

# The shape of a useful intervention

Imagine a small organisation struggling with appointments. Its team wants to rebuild the booking system. They have a plausible proposal: separate services for availability, reservations, notifications and payment. The diagram is attractive and each component has a clear technical role. Yet the complaint that started the discussion is that people arrive expecting appointments the organisation cannot honour.

Several different difficulties could produce that experience. Perhaps availability updates too slowly. Perhaps a notification describes a request as a confirmed appointment. Perhaps the organisation accepts reservations faster than staff can complete them. Perhaps people deliberately overbook because the existing cancellation pattern makes an empty slot costly. A new architecture can address some of these conditions. It can also preserve them behind better interfaces.

A useful review begins by following one booking into the disagreement. Suppose the system has recorded a request, while the visitor believes a place has been confirmed. The organisation has not yet assigned the required person or resource. In this constructed case, the first intervention may be to make the commitment explicit: when does a request become something the visitor can rely on, and who or what can make that transition? The answer affects the message, the data model, the cancellation path and the workload the organisation accepts. It is a product decision with architectural consequences.

That is where I would want the review to land. A notification and the allocation of a resource are concrete enough to inspect together. If the mismatch is elsewhere, following them should expose it. The team can investigate the problem without first accepting my account of the whole architecture.

I have worked as a builder, a team leader and an adviser. Each position changes what I can contribute and what I can carry through myself. My exploratory years included conversations and possible collaborations that did not become enduring ventures. A useful review still matters on its own terms: it can change the next experiment, expose an uncertainty or help a team stop promising something it cannot deliver. The people continuing after the conversation need to know what to do with it.

<a id="a-recommendation-meets-somebody-s-capacity"></a>

## A recommendation meets somebody's capacity

Advice can become unhelpful by being correct at the wrong scale. A proposal may assume specialist staff the organisation does not have, a budget it cannot sustain or a maintenance obligation nobody has accepted. It is not enough that the design would work under those conditions. The conditions have to become part of the conversation.

For the appointment team, a sophisticated real-time scheduler might be appropriate later. A first intervention could instead make the confirmation rule intelligible, reduce the unsupported promise and expose a small set of exceptional cases to a person. That choice does not celebrate permanent manual work. It gives the team a tractable way to discover what deserves automation and what depends on a judgment it has not yet made explicit.

In this example, the person covering booking requests checks both the available slot and the person or resource needed for it. Until those are assigned, the reply says, “We have your request; the appointment is not confirmed yet.” Confirmation records what has been reserved and gives the visitor the agreed details. The next shift sees requests still awaiting a decision alongside confirmed appointments, rather than an undifferentiated list of messages marked read. The wording, responsibility and handoff can be tried together before any new scheduler is built.

The ordinary rule also needs somewhere to stop. If a resource becomes unavailable, the booking goes to the person able to offer an alternative; it does not silently become confirmed because its preferred time is near. If a visitor asks for something the team cannot yet support, staff explain what must be checked and retain the unanswered question. A cancellation releases the actual allocation as well as changing the message. Trying those cases exposes whether the operation makes sense. Automation can then carry the recurring steps without being asked to invent how the organisation handles the exceptions.

The smallest intervention is therefore not necessarily the cheapest visible change. It is the smallest change that can answer the relevant question without moving an unmanageable burden elsewhere. A new confirmation button is not small if a person must spend every day reconstructing the missing context behind it. A larger change can be proportionate if it removes a recurring coordination failure. [Product simplification](https://getharsh.in/blog/making-a-product-smaller/) becomes interesting at that point: the reduction is in the difficulty people have to carry, not merely in the number of features.

The organisation also has legitimate reasons to choose differently. It might value continuity over a cleaner design, or be unable to interrupt a current service while investigating its future. A reviewer should make those trade-offs clearer rather than interpret every refusal as a failure to understand. The recommendation belongs to a decision, and the decision belongs to the people who will live with it.

<a id="the-advice-should-survive-the-adviser-leaving"></a>

## The advice should survive the adviser leaving

A conversation can feel productive because one person temporarily supplies all the missing context. They know what the diagram means, remember the exception and can explain why a suggestion was made. If the next team member cannot reconstruct that reasoning, the organisation has borrowed the person's presence rather than gained a useful account of the problem.

For our hypothetical booking case, I would want the review to leave four things people can use without me: the mismatch that prompted it, the competing explanations, the proposed confirmation rule and a booking that tests the rule. The next owner can then challenge the diagnosis. Perhaps confirmation wording was only a symptom and capacity is the real constraint. Finding that should improve the work, not become a defence of the reviewer's first answer.

This also changes the review's tone. “Your system is wrong” collapses the existing work and the particular concern into one verdict. “This message promises a confirmed place before the necessary resource is assigned” identifies a condition the team can examine. Precision makes the criticism less personal and more actionable without making it less serious. [Holding an idea without becoming it](https://getharsh.in/blog/holding-an-idea-without-becoming-it/) matters on both sides: the builder needs room to revise the design, and the adviser needs room to revise the diagnosis.

<a id="after-the-conversation"></a>

## After the conversation

An advisory contribution might be accepted and never implemented. A useful recommendation might become unnecessary because the organisation changes direction. A rejected suggestion might still reveal a constraint that helps the team choose another path. None of these possibilities makes advice inconsequential, but they make its consequence more particular than the success of the whole company or product.

The distinction matters for learning as well as credit. If the appointment change is made and the complaints remain, the right response is to investigate the result, not preserve the recommendation's elegance. Maybe the message was only one part of the problem. Maybe capacity is scarce in a way the booking model still conceals. The intervention has earned another question, and possibly a different scale of work.

Sometimes I should stay and help implement the choice. Sometimes another person is better placed to continue. Sometimes the review has done its job by making the decision possible. Knowing when to stop is part of being useful: the team should leave with work it can carry, rather than a larger dependence on the person who came to help.

I would rather leave the booking team able to explain when an appointment is confirmed, test the exceptions and change the rule when it fails than leave them with a better diagram they need me to interpret.


Reading path: [Building products and teams](https://getharsh.in/collections/building-products-and-teams/) > [The shape of a useful intervention](https://getharsh.in/collections/building-products-and-teams/the-shape-of-a-useful-intervention/)
