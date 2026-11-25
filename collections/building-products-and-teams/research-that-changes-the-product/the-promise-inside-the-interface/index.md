Title: The promise inside the interface

[Read HTML](https://getharsh.in/collections/building-products-and-teams/research-that-changes-the-product/the-promise-inside-the-interface/)

Author: Harsh Joshi

<a id="the-promise-inside-the-interface"></a>

# The promise inside the interface

There is a satisfying moment in technical research when a mechanism finally becomes intelligible. A diagram that seemed ornamental becomes a working explanation; the strange term turns out to name a problem you already understand. It is tempting to take that moment as the end of the investigation. In product work, it is often the beginning. The next question is what this understanding changes for somebody trying to do something.

I care about that crossing because product decisions often contain technical assumptions before anybody calls them technical. “Let people bring their own model” sounds like a welcoming promise. It also assumes a way to load the model, enough memory to run it, compatible operations, an acceptable response time and a useful account of what happens when one of those conditions fails. The promise has already made an architectural commitment. Research gives us a chance to notice it before a customer discovers it for us.

<a id="the-same-machine-two-different-products"></a>

## The same machine, two different products

Consider a hypothetical team offering model inference. One prospective user wants an interactive assistant whose response begins quickly. Another wants to process a large archive overnight. Both ask for access to the same kind of accelerator. A hardware catalogue makes their requests look similar; the work makes them different. The assistant cares about waiting and interruption as experienced by a person. The archive job can tolerate more delay between individual items if the whole batch finishes within its window. A design that improves aggregate throughput can help the second and frustrate the first.

Now imagine the team reading the [PagedAttention paper](https://arxiv.org/abs/2309.06180). Kwon and colleagues describe how allocating attention-cache state in blocks can reduce wasted memory and allow more requests to be served together. The interesting product consequence is not merely that an engine became faster. Memory management changes how many requests can coexist, while scheduling and the workload still shape the response people experience. A reported improvement belongs to the paper's tested setting. It supplies a mechanism to investigate in our setting, not an automatic multiplier for the service we want to offer.

The two users give the team different questions to test:

| Product use | What the user needs | Comparison the team should make |
| --- | --- | --- |
| Interactive assistant | A useful response beginning promptly under arriving demand | First-response delay and completion behaviour at declared input/output lengths and loads |
| Overnight archive | The declared batch completed within its window | Completed work, elapsed time and recovery across that batch |

This changes the next conversation. Input lengths, response lengths and arrival patterns matter alongside the accelerator. A model upload needs a selected execution path, not just a place to store its weights. Interactive and batch demand may require different admission and scheduling choices. The mechanism has given the product team a concrete comparison to ask for before promising one pool for both.

The commercial comparison changes too. A low rate for hardware that takes longer, interrupts more often or requires substantial adaptation may produce a costly result. The relevant purchase becomes [the completed job](https://rawthoughts.in/collections/useful-compute/a-gpu-price-is-not-a-job-cost/) (on RawThoughts), with the time and conditions that make it useful. Technical research and pricing research meet at that object. Neither can settle the comparison alone.

<a id="far-enough-into-the-mechanism"></a>

## Far enough into the mechanism

A product person does not need to become the best kernel engineer in the room to recognise that kernel performance and service performance are different questions. They do need enough understanding to hear when an answer belongs to the wrong question. That middle ground is demanding. It asks for more than collecting explanations and less than pretending to own every technical specialty.

I find a mechanism most useful when I can follow it into a failure. If memory is the constraint, what happens as the requests become longer? If communication is the constraint, what happens when work spreads across machines? If a benchmark looks excellent, what was actually completed, and which requests never reached the result? Those questions turn a literature survey into possible experiments. They also let an engineer disagree precisely: perhaps the workload is different, the assumption is wrong or the proposed measurement would conceal the bottleneck.

The disagreement can alter the scope. A service might begin with a narrow, well-understood model and workload rather than a universal compatibility claim. It might expose a capability check before accepting a job. It might make export and recovery part of the first user journey rather than leave them as later infrastructure work. The smallest useful product is not necessarily the one with the fewest screens. It is the one whose promise has become specific enough to carry.

There is a counterpressure worth keeping. Research can also become a way to postpone choosing anything. Every paper opens another literature, every limitation another architecture, every promising idea another future product. A practical investigation needs a live decision: something that would change if one explanation were right and another were wrong. The decision gives the reading a direction without requiring every interesting question to become a roadmap item.

In this case, understanding the mechanism has made the decision more definite. Two people asking for the same machine may need different products. We can now test the distinction, rather than let the hardware name settle it for us.


Reading path: [Building products and teams](https://getharsh.in/collections/building-products-and-teams/) > [When research changes the product](https://getharsh.in/collections/building-products-and-teams/research-that-changes-the-product/) > [The promise inside the interface](https://getharsh.in/collections/building-products-and-teams/research-that-changes-the-product/the-promise-inside-the-interface/)

Next in journey: [What the measure leaves out](https://getharsh.in/collections/building-products-and-teams/research-that-changes-the-product/what-the-measure-leaves-out/)
