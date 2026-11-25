Title: Research and the working system

[Read HTML](https://getharsh.in/collections/building-products-and-teams/a-career-through-problems/research-and-the-working-system/)

Author: Harsh Joshi

<a id="research-and-the-working-system"></a>

# Research and the working system

A role can widen the view without making the work less technical. Product responsibility asks what is worth building; engineering leadership asks how people can build and sustain it. Research can change the terms of both questions. Those perspectives meet in the same working system.

After DAO Studio, I moved through a short engagement with [Specmatic](https://specmatic.io/) in September 2024, VP Engineering at [Accacia](https://accacia.com/#) from October 2024 to February 2025, and Founding Product Manager at [AION](https://www.aion.xyz/) from March to November 2025. These were quite different problems. A developer wanted a dependable agreement with another service. A building-carbon workflow needed to understand what a document actually described. An AI team needed compute that could complete its work. Joining each organisation meant entering a history and vocabulary I had not chosen.

<a id="agreements-that-can-meet-the-code"></a>

## Agreements that can meet the code

At Specmatic, I explored how AI could help teams keep an API specification and its implementation together. Generating a plausible specification was the easy ambition to describe. The more useful question was where developers could agree on a change, discover what it would break and test the agreement before other teams depended on it.

My product work moved towards the pull request as that meeting place: a proposed code change, its corresponding specification and the checks that made their relationship examinable. That was a narrower entry than asking an agent to absorb every conversation around a project. It gave the ambition a recognisable place in a developer's day. AI could help developers keep that agreement as the code changed.

I also built a reflection agent for code and structured OpenAPI and gRPC specifications. That implementation and the broader workflow proposals are different parts of the account: building the agent did not by itself establish that every proposed collaboration path had been delivered.

<a id="the-document-had-another-job"></a>

## The document had another job

At Accacia, a bill of quantities sat between a building project and decisions about materials, carbon and procurement. Extracting the rows did not settle what they meant. A quantity needed a unit; a description needed enough context to identify the material; a proposed transformation needed someone able to recognise a wrong interpretation. [The line item](https://getharsh.in/collections/building-products-and-teams/from-document-to-domain/) was a domain object before it was a convenient piece of model input.

Leading engineering brought that problem together with the less glamorous work that lets a team change a system safely: explicit frontend/backend contracts, technical-debt decisions, tests and release responsibility. I also worked directly on role-based access control and audit logging. The hands-on work mattered to me. It kept the distance between a proposed engineering practice and the implementation carrying it short enough to examine.

The bill-of-quantities work covered more than 8,000 lines, with reported conversion accuracy above 90%. Alongside it, testing time fell by 70%, test coverage reached 60%, sprint velocity rose by 35%, and the beta arrived two quarters early. I built an LLM streamer library and led the engineering organisation through SOC 2 Type I and ISO/IEC 27001, issued in January 2025.

The domain also changed what a good engineering conversation sounded like. A row could be perfectly parsed and still be the wrong material; a test could confirm the transformation without confirming the interpretation. The team needed places where domain judgment and software behaviour could meet. That made contracts and tests more useful to me as shared working agreements than as a count to improve. The question was what another person could now change with confidence, and what still needed the specialist's eye.

<a id="infrastructure-has-readers-as-well-as-users"></a>

## Infrastructure has readers as well as users

The AION work brought two views closer together for me: the machine with its memory, communication and scheduling constraints, and the person waiting for an experiment to finish or an application to answer. Moving between product questions, technical research and developer experience made the distance between those views part of the work itself.

My cluster work reached 49.87% Model FLOPs Utilization on H100 and H200 systems: roughly half the hardware's theoretical arithmetic capacity was doing useful model computation. Communication between GPUs mattered too. The cluster reached 472–477 GB/s reported bus bandwidth in NCCL, the library coordinating that communication. A model spread across several GPUs depends on both the work each one can do and how well they work together.

The service also needed to keep a promise to the person using it. I delivered Guaranteed Start Windows and procedures for tearing down compute resources when their work ended, built a Go notification service, and defined service commitments and operations tracking. With Customer Success, I led GDPR and SOC 2 compliance work and delivered the terms of service and privacy policy.

I rebuilt the website twice, reaching about 0.05-second largest contentful paint, the time until the largest visible image or text block appears. I also built analytics connecting campaigns to GPU-hour use and an asynchronous product-management agent. That connected the work of bringing someone to the service with what they actually came there to do.

I led the research-led content programme, with fifteen article briefs and eight substantive drafts, and wrote the *Economics of AI* whitepaper.

In that programme, the same difficult subject had to become intelligible to a reader, useful to a product conversation and workable for another contributor. A faster isolated operation might still leave the developer's job unfinished. An accurate explanation might still leave a reader unable to choose. The explanation had to connect the mechanism to the decision facing its reader.

<a id="learning-enough-to-change-the-decision"></a>

## Learning enough to change the decision

Technical fluency matters to me because it changes what I can ask. A diagram can make two providers look interchangeable until the workload needs something only one can express. A document-processing pipeline can return neat fields while leaving the [meaning of the material](https://getharsh.in/collections/building-products-and-teams/from-document-to-domain/) unresolved. A simpler developer interface can still ask the user to reconstruct the difficult part of the workflow themselves.

I want to get far enough into the mechanism to recognise those differences. The aim is not to become the specialist in every part of a system. It is to understand the point at which a technical assumption changes the product, and to ask for the comparison that would make the decision clearer. [Research becomes product work](https://getharsh.in/collections/building-products-and-teams/research-that-changes-the-product/the-promise-inside-the-interface/) when it can change the boundary, the sequence or the promise, rather than simply decorate the proposal with more background.

Compute made that relationship especially interesting to me. A nominally faster device can leave a job waiting for memory, communication or available capacity. A system can process more work while offering a worse service to the person waiting. Following those differences took my own inquiry from hardware towards [the economic arrangement around it](https://getharsh.in/blog/from-compute-to-an-economic-question/). The larger question did not arrive separately from the engineering one; it appeared as I followed what the engineering could make possible.

The [content programme](https://getharsh.in/blog/research-becomes-a-reading-path/) brought another consequence into view: an explanation has to travel without its original author standing beside it. A writer needs enough of the mechanism to develop the argument; an engineer needs enough of the proposed comparison to challenge it. That connects explanation to leadership for me. A brief, a handover or a research collaboration becomes useful when another person can carry the work and judge what it needs next.

<a id="bringing-the-questions-into-my-own-construction"></a>

## Bringing the questions into my own construction

My present consulting practice is through [RawThoughts](https://rawthoughts.in/) (on RawThoughts). I stay interested in the whole path: the decision, the software, the people using it and the point at which the result can be examined. A model can be useful within that path without being the right method for every step. A deterministic calculation, a recoverable operation and a person's judgment may need to meet rather than be replaced by one fluent answer.

Alongside that work, I am [building an environment](https://getharsh.in/collections/building-products-and-teams/building-a-place-to-think/) in which context, responsibilities and capabilities can remain available across sessions. [Pale](https://rawthoughts.in/pale/) (on RawThoughts) gives my goals a path across applications; [Scope](https://rawthoughts.in/scope/) (on RawThoughts) brings an agent the context it needs from what Pale and Weave hold; [Weave](https://rawthoughts.in/weave/) (on RawThoughts) connects relationships with accountable work; [Gazette](https://rawthoughts.in/gazette/) (on RawThoughts) makes connected knowledge available to readers. Its purpose is to let work continue across those settings with less reconstruction, while leaving me attention for the decisions and inquiries I came to them for.

I want my practical work to keep meeting the questions that led me to it. Sometimes that means improving an implementation. Sometimes it means narrowing the problem or changing the representation. The inquiry continues because another setting can reveal a consequence I had not yet understood, not because every previous setting was secretly preparing me for the present one.


Reading path: [Building products and teams](https://getharsh.in/collections/building-products-and-teams/) > [A career through problems](https://getharsh.in/collections/building-products-and-teams/a-career-through-problems/) > [Research and the working system](https://getharsh.in/collections/building-products-and-teams/a-career-through-problems/research-and-the-working-system/)

Previous in journey: [Making intelligence usable](https://getharsh.in/collections/building-products-and-teams/a-career-through-problems/making-intelligence-usable/)
