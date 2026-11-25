Title: What the measure leaves out

[Read HTML](https://getharsh.in/collections/building-products-and-teams/research-that-changes-the-product/what-the-measure-leaves-out/)

Author: Harsh Joshi

<a id="what-the-measure-leaves-out"></a>

# What the measure leaves out

A team can improve the number it watches and make the product less useful. The uncomfortable part is that the improvement may be real. More answers arrive. More tokens are generated. Nothing in the measurement has to be fabricated for the conclusion to be wrong.

For the hypothetical interactive assistant, suppose the business objective is to help a person finish a task during the conversation. The team uses completed answers per minute as an early technical proxy. Batching more requests improves that number, so the new configuration looks like progress. But a person who has already abandoned the conversation cannot use the late answer. The proxy has stopped following the reason for improving it.

<a id="more-answers-less-useful-work"></a>

## More answers, less useful work

An invented comparison makes the divergence visible. Give both configurations the same hundred arriving requests and the same observation window. Set the response-time requirement before the test, and review whether each answer helps complete its task rather than counting any returned text as useful.

| Result from the same hundred requests | First configuration | More aggressive batching |
| --- | --: | --: |
| Answers completed within the observation window | 90 | 95 |
| Answers arriving within the response-time requirement | 80 | 60 |
| Answers both timely and useful for the task | 72 | 54 |

The second configuration completes more answers, yet delivers fewer useful answers while the person can still act on them. The comparison needs the whole arriving cohort, including unfinished requests, rather than only the responses that happen to succeed. The revised product measure is timely, useful task completion; throughput, queue time and answer quality help explain what moves it. None of those explanatory measures has to disappear, but none can stand in for the objective on its own.

The distinction also changes how a team investigates the result. If timely answers fall, the scheduling choice deserves attention. If timely answers arrive but do not help, the task or answer quality deserves attention. Collapsing those failures into one completion count makes two different product problems look like the same technical problem. Keeping the whole arriving cohort visible prevents the requests that failed to finish from quietly leaving the comparison.

For the archive user, the response-time requirement may be beside the point. A batch that finishes within its overnight window can benefit from the same scheduling choice. The discovery should change the offer or the configuration offered to each user, not become a verdict that batching is good or bad. This is the translation I want product research to accomplish: understand the business purpose, make a technical comparison, notice where the proxy diverges, and change the decision while there is still time to do so.

<a id="the-task-can-be-wrong-too"></a>

## The task can be wrong too

The task itself may need revision. In an annotation programme, a category can be applied consistently while failing to preserve the distinction the eventual model needs. The research question then concerns [what the label lets the next system learn](https://rawthoughts.in/blog/the-label-is-a-decision/) (on RawThoughts), rather than how rapidly more labels can be produced. That is another place where product judgment enters technical work early: defining the useful output changes the data, the contributor's task and the evaluation together.

An experiment that invalidates an attractive product assumption can be valuable even when it produces no launchable feature. If a new serving method helps only the overnight workload, the team has learned how to separate its users more honestly. If a category makes labelling easy while losing the distinction needed downstream, the team has learned that its definition of the work needs revision. More efficient execution of the original task would not resolve either problem.

That learning needs a way back into the product. Otherwise the team can preserve the report while continuing to sell the assumption it disproved. A changed acceptance condition, a narrower supported path, a different default or a revised commercial promise makes the investigation consequential. [Making a product smaller](https://getharsh.in/blog/making-a-product-smaller/) can then be the result of deeper understanding rather than reduced ambition.

I want the measure to remain close enough to the purpose that an unwelcome result can still change our minds. It should help us see where the work has become useful, not merely where the machinery has become busy.


Reading path: [Building products and teams](https://getharsh.in/collections/building-products-and-teams/) > [When research changes the product](https://getharsh.in/collections/building-products-and-teams/research-that-changes-the-product/) > [What the measure leaves out](https://getharsh.in/collections/building-products-and-teams/research-that-changes-the-product/what-the-measure-leaves-out/)

Previous in journey: [The promise inside the interface](https://getharsh.in/collections/building-products-and-teams/research-that-changes-the-product/the-promise-inside-the-interface/)

Next in journey: [Past the first successful call](https://getharsh.in/collections/building-products-and-teams/research-that-changes-the-product/past-the-first-successful-call/)
