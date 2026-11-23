Title: Advice that meets the operator

[Read HTML](https://getharsh.in/collections/energy-efficiency/from-service-to-control/advice-that-meets-the-operator/)

Author: Harsh Joshi

<a id="advice-that-meets-the-operator"></a>

# Advice that meets the operator

The same deviation appears every morning. We can plot it, perhaps even predict it. Tomorrow, the operator will still have to work out what it means. Have we made the plant easier to run, or merely become very good at announcing its familiar difficulty?

At [Smart Joules](https://smartjoules.co.in/), the JouleMind and Nudges direction asked how infrastructure, process and user context could support better energy operations. The ambition went beyond another graph: measurements, command history, maintenance and schedules could help determine which suggestion mattered, and to whom. I am interested in that design problem because more information is only helpful when it changes the work of understanding or acting.

<a id="four-explanations-for-the-same-morning"></a>

## Four explanations for the same morning

Consider a constructed example. A cooling system uses more energy than expected during the first hour of operation. The pattern might follow an earlier start, a different load, changed equipment performance or an unreliable measurement. A schedule could explain a legitimate difference. A maintenance event could suggest somewhere to investigate. An incorrectly mapped sensor could make the apparent difference disappear when the measurement is repaired.

The repeated deviation selects a question; it does not choose between those explanations. A predictor that reproduces the pattern accurately has learned when it appears, not necessarily why. Recommending the same intervention for all four cases would turn a useful detection into an unhelpful certainty.

The next step becomes narrower when the explanation connects measurement quality to the operating period, service requirement and intended reference. Maintenance and command history can help distinguish the remaining possibilities, revealing which further observation would resolve a particular uncertainty. “Check whether this schedule still matches today's use” can be a better suggestion than “reduce energy” because it points to something a person can establish, rather than announcing a conclusion the pattern has not supplied.

The [US Department of Energy's measurement and verification guidance](https://www.energy.gov/cmei/femp/measurement-and-verification-activities-required-energy-savings-performance-contract) similarly treats equipment conditions, operating hours and varying loads as part of establishing a meaningful baseline. In this example, those conditions matter before the deviation becomes a diagnosis, not just afterwards when a saving is calculated.

<a id="who-can-answer-this-question"></a>

## Who can answer this question?

The person receiving the suggestion may know why the schedule changed but have no access to alter it. Another person may have access but lack the local context. Sending the same message to both does not solve the split. The application needs to distinguish a request for information, a recommendation to a decision-maker and work someone has agreed to carry.

This changes the shape of the suggestion. It can present the observed interval, the expected comparison and the reason a schedule check is relevant. The recipient can confirm a changed operating requirement, report missing information or pass the question to someone who can decide. A closed alert then has a meaning: was the difference explained, the measurement repaired, an intervention tried or only the notification dismissed?

The distinction also applies to priority. An unusual pattern may be less important than a smaller recurring loss, while a condition affecting service may deserve attention for reasons an energy score misses. NIST's [fault detection and diagnostics research](https://www.nist.gov/programs-projects/embedded-intelligence-buildings-program) includes interactive diagnosis and prioritisation by energy impact and occupant comfort. That is a useful external example of why detecting a fault and deciding what deserves attention require different information.

<a id="tomorrow-s-alert-should-remember-today-s-answer"></a>

## Tomorrow's alert should remember today's answer

Suppose the operator replies, “The building opened an hour earlier today.” That answer changes the comparison. The extra consumption belongs to an extra hour of required service, not necessarily to worse equipment performance. The application can retain the changed opening time and compare the operating interval on that basis. It has learned something about this morning without deciding that every future early start is harmless.

Tomorrow's question should depend on what changed. If the same opening requirement applies, repeating the original alert adds little. If the building returns to its ordinary hours but the plant still starts early, there is a new discrepancy worth examining. The operator's answer needs to remain attached to its schedule and period so it can reduce repetition without silencing a useful later question.

If an intervention is tried, its evaluation has to return to [the service behind the saving](https://getharsh.in/collections/energy-efficiency/from-service-to-control/the-service-behind-the-saving/). Did the useful work continue under comparable conditions? Was the result short-lived? Did the change merely move consumption elsewhere? A positive rating about a clear message cannot answer those questions, although it can tell us something about the interaction. The system needs both kinds of feedback without treating them as substitutes.

This is the learning loop I wanted the assistance to make possible: preserve a reason for the suggestion, connect it to an examined response, and use that result to make the next question more relevant. It does not require every proposal to become automatic control. Sometimes useful intelligence is knowing what to ask, retaining the answer in its proper context and not making the person reconstruct it again tomorrow.


Reading path: [Energy efficiency](https://getharsh.in/collections/energy-efficiency/) > [From service to control](https://getharsh.in/collections/energy-efficiency/from-service-to-control/) > [Advice that meets the operator](https://getharsh.in/collections/energy-efficiency/from-service-to-control/advice-that-meets-the-operator/)

Previous in journey: [Did the command reach the pump?](https://getharsh.in/collections/energy-efficiency/from-service-to-control/did-the-command-reach-the-pump/)
