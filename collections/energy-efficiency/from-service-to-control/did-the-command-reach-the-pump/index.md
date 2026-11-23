Title: Did the command reach the pump?

[Read HTML](https://getharsh.in/collections/energy-efficiency/from-service-to-control/did-the-command-reach-the-pump/)

Author: Harsh Joshi

<a id="did-the-command-reach-the-pump"></a>

# Did the command reach the pump?

Press a button. The application says the command succeeded. What, exactly, have we learned about the pump?

One button makes the request feel like one event. Behind it, the application accepts an instruction, a controller receives it and equipment may respond. The success message may belong to any one of those steps. Meanwhile, the operator needs to know what happened in the plant. Reading equipment and plotting its behaviour was part of my work on energy products; talking to operators made the other half unavoidable. They needed somewhere to act, not a lesson in our packet network.

Following the command through that gap changes how I think about the interface. It has to make the next useful check visible. A plant keeps running outside our description of it, and the software has to find out what that independent world did.

<a id="one-rule-several-places-to-fail"></a>

## One rule, several places to fail

Imagine a recipe that changes a pump setting when a measured condition is met. One plant, one rule, one action looks like a local operation. Its observation, evaluation and output may nevertheless live in different places. A reading can come from another controller; the rule can run locally while its command crosses the network; or observations can travel to a server before a decision returns.

Those arrangements fail differently. With local evaluation and output but a remote observation, the controller can remain healthy while the rule loses the information it needs. With local observation and evaluation but remote output, the condition can be recognised while the action remains unconfirmed. Moving evaluation closer to the equipment can remove an internet dependency without removing the local-network dependency or making a missing reading valid.

Locality is therefore a property of a particular path, not a reassuring adjective for the whole system. During an outage, “the controller is running” helps only after we know which parts of this control still depend on something else.

<a id="the-zero-that-fills-a-gap"></a>

## The zero that fills a gap

A value arrives with an interpretation already attached. Which device produced it? Which parameter does it represent? What unit, scaling and age apply? Chiller performance can depend on power, flow and temperature obtained through different paths. One current input cannot make the others current, and receiving a packet cannot establish that the mapping to a physical component is correct.

The distinction between an off asset, an unavailable reading and an invalid calculation matters here. A zero can be a real observation. Substituting zero for a missing input changes the meaning of the calculation while making the chart look complete. The graph should express the state of the evidence rather than reward the interface for having something to draw.

The same plant can need several representations. Its geographical layout helps locate an asset. Its physical connections explain where flow or power travels. A logical group identifies the observations needed to understand a process. Collapsing these into one hierarchy makes the display simpler at the cost of hiding the dependencies that explain a failure.

![Chiller power passes through controller A, while flow and temperature readings pass through controller B before meeting in the performance calculation.](https://getharsh.in/collections/energy-efficiency/from-service-to-control/did-the-command-reach-the-pump/plant-light.svg)

The dashed paths carry readings from the plant to the performance calculation.

<a id="how-far-did-the-request-get"></a>

## How far did the request get?

The command can be followed as a sequence of observations.

1. The application accepts the request. It has entered the software; did the controller receive it?
2. The controller acknowledges receipt. It received the instruction; did the equipment act on it?
3. The equipment reports a state that matches the request. Is that report current, in the expected unit and mapped to the right component?
4. Physical feedback changes. Something in the plant changed; did it deliver the intended service?
5. The service is examined. We can compare the output with what is needed; is it adequate for the current load?

Each stage gives the operator somewhere to stand. The next check is narrower than “did it work?”, and the path can remain partly known without being called either a complete success or a complete failure.

A requested speed and a reported speed can agree while a distant part of the building still receives [inadequate service](https://getharsh.in/collections/energy-efficiency/from-service-to-control/the-service-behind-the-saving/). Conversely, equipment can respond while feedback is delayed or interpreted incorrectly. “Failed” can be as misleading as “successful” when either label compresses the entire path into one status.

This changes the meaning of recovery. Repeating a command because its confirmation is absent can duplicate an action already taken. Accepting a successful request as the physical result can leave a real failure unnoticed. The installation, the action and its observations must inform the response; the interface cannot invent that knowledge through a generic retry rule. A statement such as “request sent, equipment state unconfirmed” gives the operator a useful location in the process, from which the product can help identify the missing check instead of offering only an optimistic green indicator or an unexplained error.

<a id="the-plant-can-change-without-us"></a>

## The plant can change without us

Manual mode can override a network request. Somebody can change the plant during an outage while the application's last observation remains unchanged. A retained reading helps reconstruct the earlier state, but reconnecting requires finding out what is there now, not automatically restoring the old setting. That is a product problem as much as an engineering one: the operator needs the distinctions that affect a decision, not every implementation detail.

A recipe also has a life beyond its creation. Date eligibility, enabled state, current evaluation, command transmission and physical effect can diverge. The calendar can permit execution while the recipe is paused. Evaluation can begin without a valid input. A command can be sent while its output path is unavailable. Deployment gives the rule a place to operate; commissioning and continuing observation establish how it is operating.

Alerts extend the path to another person. A locally detected condition may still rely on a server and a communication channel to reach them. Delivery, reading, taking responsibility and resolving the problem then become separate achievements. The person and the manual route belong to the operation, not outside it as an afterthought. Whether the path ends at equipment or reaches another operator, showing where it has reached and which check would let the work continue is more useful than making an entire physical operation look finished because the software successfully sent a message.


Reading path: [Energy efficiency](https://getharsh.in/collections/energy-efficiency/) > [From service to control](https://getharsh.in/collections/energy-efficiency/from-service-to-control/) > [Did the command reach the pump?](https://getharsh.in/collections/energy-efficiency/from-service-to-control/did-the-command-reach-the-pump/)

Previous in journey: [The service behind the saving](https://getharsh.in/collections/energy-efficiency/from-service-to-control/the-service-behind-the-saving/)

Next in journey: [Advice that meets the operator](https://getharsh.in/collections/energy-efficiency/from-service-to-control/advice-that-meets-the-operator/)
