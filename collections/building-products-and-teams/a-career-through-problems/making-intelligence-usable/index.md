Title: Making intelligence usable

[Read HTML](https://getharsh.in/collections/building-products-and-teams/a-career-through-problems/making-intelligence-usable/)

Author: Harsh Joshi

<a id="making-intelligence-usable"></a>

# Making intelligence usable

A language model makes an unusual first impression: the component seems able to explain the whole system. It can interpret a request, supply an answer and sound as though it knows what should happen next. Building applications around that capability returned me to questions I had met in plants and customer workflows. Which information matters here? What actually happened? What would let somebody inspect an error or continue the work?

I co-founded [DAO Studio](https://daostudio.in/about/) with Shashwat Pandey in October 2022 and led its product, technology and company work through September 2024. Alongside those responsibilities, I built [YojnAI](https://daostudio.in/yojnai/) as an individual contributor. Composition, tracing and feedback were ways to give the application more structure than one impressive answer.

The studio began with an ambition inspired by Amul and Lijjat Papad: help people create decentralised autonomous organisations. As we explored what that would require, AI became part of the means. The mission I wrote down was to democratise AI and commoditise intelligence. YOJN, from a Sanskrit word for a unit of distance, became the name through which that idea developed. The destination was bigger than a language-model tool; the tool was a concrete place to work on explainability, controllability, decomposability and interoperability.

The individual-contributor and founder perspectives did not take turns neatly. Building the platform meant deciding what a unit of work should expose, then confronting what the application needed that the abstraction had left out. Leading the company meant asking whether someone else could use, maintain and pay for that arrangement. A mechanism elegant enough to explain on a whiteboard still had to survive those questions. I wanted to make the tool and understand the business it might make possible, rather than delegate one side and talk only about the other.

We raised ₹0.6 crore, brought in three entrepreneurs in residence and built an advisory board of five. The company reached ₹5 lakh in monthly recurring revenue and cash-flow neutrality during the pilot period. We also made three IP filings; filings are steps in protecting work, not granted patents. A community of more than a thousand people and more than five open-source projects gave the work other routes into use and discussion.

<a id="following-the-work-between-model-calls"></a>

## Following the work between model calls

One design choice was to expose work before the final response. An application might have already extracted a useful term while still waiting for a clarification elsewhere. Keeping that intermediate state and giving another component a callback into the work could let a person inspect the term without rerunning the whole request. I wanted the application to be somewhere people and software could contribute, rather than an answer everybody had to wait for.

That ambition led into [the composition model](https://daostudio.in/collections/composing-ai-work/from-composition-to-a-deliberate-change/agent-playbook-and-application/): models and tools inside agents, agents and checks inside playbooks, and an application connecting them to a particular customer's records and workflow. The abstraction had to preserve the useful differences. A missing value, a completed extraction and an action already performed could not all become indistinguishable prompt context.

The platform went into three pilots, in investment banking, operations and the CFO office: one application read invoices and agreements, and another worked through financial research calculations. Those were partner-owned products built with the platform, not products whose ownership followed from our having supplied the technology. That gave the application work a setting beyond a disconnected demonstration. The product question was no longer just whether a model could produce useful text. It was whether a person could work with the result: find the part that needed attention, supply a correction and choose what to use next. Tracing and feedback brought that interaction into the design. They also kept returning me to the same tension: how much structure could make the application easier to work with, before maintaining the structure became another job for the user?

I had to move between the platform and the particular application. A useful abstraction lets different work share a mechanism without making the differences disappear. An invoice and a research question can both pass through a model, but they ask for different sources, interpretations and results. The version of an application, the path through its tools and the point where somebody intervenes give that otherwise fluid process something concrete to examine. [Understanding a trace](https://daostudio.in/collections/composing-ai-work/from-composition-to-a-deliberate-change/reading-the-work-behind-an-answer/) then becomes work in its own right, rather than something the log performs for us.

The earlier experiences were useful without supplying a ready-made answer. A plant's independent physical state is different from a language-model application's generated result. A support workflow has different dependencies from a finance task. But following the work beyond the apparent success of a component remained a productive habit. The [product around the model](https://getharsh.in/blog/an-ai-product-is-more-than-a-model/) needed its own attention.

<a id="the-run-that-made-a-year-of-building-feel-worthwhile"></a>

## The run that made a year of building feel worthwhile

When asked for a “hell yeah” moment in my career, I returned to a finance-model run through YOJN. We had spent a year building the tool. I was working with finance data for the first time, adapting a Mistral 7B model quantised to four bits through reinforcement learning from human feedback. The application had to do useful work with financial material, where a fluent response could still get the numerical reasoning wrong.

The figures I reported from that pilot were MMLU performance comparable to GPT-3.5, a BigBench score above 70% and self-hosting at about $1.75 an hour. They describe my reported pilot result, not a benchmark comparison. The satisfaction was more immediate. The system we had spent that year building had carried the model work into an actual application. It was a litmus test of YOJN, and it remains one of my favourite moments of something first working.

The model's score was only part of the product question. A person still needed to inspect an answer, trace it to the financial material and correct a mistake. That was why composition, tracing and feedback belonged together in the tool. Improving a model and making its contribution usable in an application were connected jobs, with different results to examine.

<a id="taking-that-habit-into-another-setting"></a>

## Taking that habit into another setting

Company leadership required a different view of the same work. A promising application needed people who could build, review and sustain it, and an arrangement in which that effort could continue. I could not stay solely inside the mechanism, but I did not want to become so far removed from it that the product was only a promise I could explain. Moving between those perspectives was part of the founder's job.

What I carry into consulting is that combination. I want to understand the problem where it happens, make the important dependencies intelligible, and stay close enough to implementation to learn what the design missed. Sometimes the next useful intervention is technical. Sometimes it is a smaller promise, a clearer decision or a different division of work. The architecture is stronger when those possibilities remain available.

<a id="the-questions-that-came-home-with-me"></a>

## The questions that came home with me

[RawThoughts](https://rawthoughts.in/) began as writing and exploration during my transition out of [Smart Joules](https://smartjoules.co.in/) and developed into the applied practice I work through now. Some questions from those years have become more concrete there: [which context helps](https://rawthoughts.in/collections/systems/context-that-helps-the-work/when-context-helps/), how [a responsibility survives a conversation](https://rawthoughts.in/collections/practice/turning-conversation-into-work/), and what a system needs to retain when someone returns to it. Consulting keeps those questions in contact with work whose value is judged by the people relying on the result.

The application question also leaves me curious about [the capacities being composed](https://causality.in/collections/composition-and-learning/from-unit-to-swarm/three-tests-for-a-reasoning-unit/). Connecting useful model calls and studying how learning units might organise are different problems, but the difference makes the crossing productive. A working application shows me where a deeper question begins; it cannot answer that question merely by working.

Teaching and participation in the [UPAI](https://upailabs.org/) community continue the other side of the practice: helping people enter work, and letting their questions expose what my own account takes for granted. A shared context is valuable because somebody else can contribute through it, not simply because it represents my thoughts more neatly.

I had come to language models with the habits of someone who wanted to follow a system's path. Their fluency made that habit more important, while their possibilities made the path less familiar. Building around them drew product, engineering and company responsibility together. It also left me wanting to understand more of the systems on which that work depended.


Reading path: [Building products and teams](https://getharsh.in/collections/building-products-and-teams/) > [A career through problems](https://getharsh.in/collections/building-products-and-teams/a-career-through-problems/) > [Making intelligence usable](https://getharsh.in/collections/building-products-and-teams/a-career-through-problems/making-intelligence-usable/)

Previous in journey: [The customer changes the system](https://getharsh.in/collections/building-products-and-teams/a-career-through-problems/the-customer-changes-the-system/)

Next in journey: [Research and the working system](https://getharsh.in/collections/building-products-and-teams/a-career-through-problems/research-and-the-working-system/)
