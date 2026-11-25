Title: What does the line item mean?

[Read HTML](https://getharsh.in/collections/building-products-and-teams/from-document-to-domain/)

Author: Harsh Joshi

<a id="what-does-the-line-item-mean"></a>

# What does the line item mean?

At [Accacia](https://accacia.com/#), I worked on converting bills of quantities into bills of materials. Reading the rows was one part of the job. A quantity needed a unit, and a description needed enough context to identify the material. Extracting the right characters could still leave us with the wrong interpretation.

Take the number twelve. It might mean twelve boxes ordered, twelve pieces received or twelve units left after an earlier delivery. Put twelve in a neatly labelled field and it looks ready to calculate with. But which calculation? The unit and the event decide that. This is where a document-processing product has to understand more than the document’s layout.

<a id="twelve-packs-of-what"></a>

## Twelve packs of what?

Take a constructed example. A small workshop orders twelve packs of fasteners. Its planning sheet assumes a hundred pieces per pack, so it derives a total of 1,200 pieces. The supplier's document also says twelve packs, but a product revision has changed the pack size to eighty. The order count still matches. The derived quantity is now 960. A system comparing only the two quantity cells reports agreement while missing the change that matters to the workshop.

| Interpretation | Pack count | Pieces per pack | Derived piece count |
| --- | --: | --: | --: |
| Planning assumption | 12 | 100 | 1,200 |
| Revised supplier definition | 12 | 80 | 960 |

The arithmetic is easy once the meaning is settled. The difference is 240 pieces, despite perfect agreement about the twelve packs. Identifying which packaging definition applies, whether it was current for this order, and whether the document describes a request or a delivery determines which calculation belongs in the work. More fluent extraction cannot supply those relationships merely by producing a convincing sentence.

Suppose the workshop later receives a partial delivery. The planning sheet still needs the full quantity, purchasing tracks what was ordered, and the person preparing the work needs to know what is physically available. These views can contain different numbers without any of them being a bad transcription. A domain model gives those numbers different jobs. Flattening them into a universal quantity field makes the disagreement disappear from the representation while leaving it alive in the work.

The example is deliberately small. The same difficulty grows when a line item combines material, dimensions, installation and a service obligation. A description useful to the buyer may not be the description useful to a manufacturing estimate. Translation between them is a substantive interpretation, not a prettier copy of the original row.

<a id="a-neat-table-can-conceal-the-missing-relationship"></a>

## A neat table can conceal the missing relationship

Structured output is valuable because it makes information easier to inspect, compare and calculate. Its usefulness can also make it persuasive. Once a sentence has become a named field, it begins to look as though the naming question has been settled. A model may select a plausible unit, infer a missing category or expand an abbreviation. Each choice can be reasonable; some choices will matter enough that they should remain inspectable.

For the workshop, an unknown pack size should not silently become a hundred because that is the common case. The system can preserve the extracted count, show the missing conversion and ask for the particular product definition. That lets useful work continue without confusing a partly understood record with a completed estimate. It is a better product experience than either making the user distrust every field or presenting all fields with equal confidence.

The distinctions also change evaluation. Reading the right characters, assigning the right field, interpreting the unit and deriving the useful total are separate points at which work can succeed or fail. An overall accuracy number can conceal a small family of errors that reverses a downstream decision. A practical evaluation includes those cases, because the question is whether the system helped the work rather than whether most cells looked correct.

[The application around the model](https://getharsh.in/blog/an-ai-product-is-more-than-a-model/) has a large role here. It decides which context is available, how an interpretation is displayed, when a missing relation interrupts the calculation and how a person's correction changes the rest of the result. A more capable model may reduce the difficulty. It does not remove the need to design that interaction.

<a id="a-correction-has-consequences-beyond-one-cell"></a>

## A correction has consequences beyond one cell

If a person corrects the pack size from a hundred to eighty, the product can treat it as a local text edit. The visible total then changes, but a cached estimate elsewhere may remain at 1,200. Alternatively, it can understand that the total depends on the packaging definition and make the affected results visible. The second response makes the correction consequential rather than cosmetic.

The human contribution is more informative still when the reason survives. Perhaps the supplier changed the product. Perhaps the order used an old definition. Perhaps the person corrected an extraction error rather than a domain assumption. Those are different problems to repair. Training on the corrected value alone can lose the distinction, especially if the number eighty becomes a pattern detached from the product and version to which it belongs.

Provenance supplies part of that structure. The [W3C PROV overview](https://www.w3.org/TR/prov-overview/) describes information about the entities, activities and people involved in producing a result. In this example, the source document, the selected product definition, the transformation and the correction are all relevant to understanding the total. Recording their relationship gives someone a way to investigate the result. It does not make the interpretation correct by itself.

Nor does retaining everything automatically produce a useful account. The reviewer needs to see what changed this result, not wade through every unrelated event in the system. That is why [useful context](https://rawthoughts.in/collections/systems/context-that-helps-the-work/when-context-helps/) (on RawThoughts) is a harder target than stored context. The package definition is quiet information until the count needs to become a different quantity. Then it can be indispensable.

<a id="the-domain-expert-changes-the-product-s-question"></a>

## The domain expert changes the product's question

An expert may not correct the number at all. They may reject the proposed comparison. Perhaps the fasteners are an incompatible grade, or a different task requires another material even though the dimensions match. The expert is supplying a relationship the current model did not know to ask about. Capturing only whether they accepted the output would make the feedback much less useful than the judgment itself.

This is where product work and domain work become closely coupled. The software should make recurring interpretation cheaper without making the expert repeat their whole discipline for every document. The expert should be able to identify a particular ambiguity, qualify a mapping or explain why a seemingly reasonable substitution fails. Over time those contributions can improve definitions, examples, evaluation cases and the model's assistance. Their usefulness comes from preserving what the correction was about.

The product also needs a readable result for someone who did not watch that process happen. A downstream person may need a usable materials total, while a reviewer needs the source and derivation. These are complementary views of the same calculation. A clean report should not acquire a different meaning simply because the detailed view was inconvenient to render.

<a id="information-becomes-usable-in-a-relationship"></a>

## Information becomes usable in a relationship

The workshop still ordered twelve packs. What changed was our understanding of what those packs contained, which definition applied and what had actually arrived. Now the planner can calculate a materials total, purchasing can follow the order and the person doing the work can see what is available. Their different answers have become useful rather than contradictory.

That is the opportunity I see in document systems: help people arrive at an account they can use and correct together. The extracted row is a beginning. The product earns its place when a specialist can explain why eighty applies here, the correction reaches the estimates that depended on a hundred, and the next person can understand the result without repeating the investigation.


Reading path: [Building products and teams](https://getharsh.in/collections/building-products-and-teams/) > [What does the line item mean?](https://getharsh.in/collections/building-products-and-teams/from-document-to-domain/)
