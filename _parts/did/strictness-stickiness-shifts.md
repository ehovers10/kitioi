---
title: Strictness, stickiness, and shifts
chapter: Dispute in discourse
---

To get a sense of what it is for bare plurals to be *structurally universal*, let's start with a discussion of strict analyses in general, a class to which interpretations that appeal to universal quantification belong. Call a *strict analysis* any translation rules that assign an operator with universal force to a natural language expression. Operators that carry universal force generate true sentences just in case the set generated by the first operand is a subset of the set generated by the second one. It is natural to offer a strict analysis of sentences involving bare plural antecedents. To say that *Lawyers are liars* is just to say that anything that is a lawyer is also a liar. This amounts to nothing more than interpreting the sentence as involving a tacit universal quantifier. But this natural inclination is not quite right; it gets held up by a sticky situation. We can, I suggest, preserve the natural inclination while exctracting ourseleves from the sticky situation by interpreting bare plurals as subsumed by a tacit *structurally* universal quantifier.

The tack I take in motivating this suggestion is parallel to an argument offered by Thony Gillies {% cite gillies2007 | noname %} in favor of a strict analysis of *counterfactual conditionals*. This analysis is similarly natural; to say that *Jack would have forgiven him, if Lenny had told the truth* is just to say that all situations in which Lenny tells the truth are also situations in which Jack forgives him. But it, too, runs into a sticky situation. Gillies argues that strictness can be extracted from the sticky situation by developing an adequate story about the pragmatics of conditionals. He also argues that this extraction is worthwhile. I extend Gillies' ideas to provide what I take to be an equally worthwhile extraction of the universal quantifier analysis of bare plurals from their stickiness. My account depends on a pragmatic story told within the framework of collaborative update semantics.

### Counterfactual conditionals

Formally, the natural inclination involving English counterfactual conditional constructions is to give an analysis of them in terms of a strict conditional.

<!-- Strict definitions -->
{% def Strict conditional %}
  {{ "conditionals|strict conditional|translation" | formalize: "notitle" }}
  {{ "conditionals|strict conditional|definition" | formalize: "notitle" }}
{% enddef %}

But this natural inclination is held up by a sticky situation. The subset relation is *transitive*, and conjunction is *intersective* which means that strict conditionals verify *thinning*:

<!-- Thinning -->
{% def Thinning %}
  {{ "conditionals|thinning" | formalize: "notitle" }}
{% enddef %}

Unfortunately, counterfactual conditionals violate [Thinning](#thinning){: #thinning-show .tooled}. Consider:

<!-- Honey -->
{% ex Honey %}
  {{ "honey" | example: "sent" }}
{% endex %}

The antecedent of **B** in [Honey](#honey){: #honey-show .tooled} is a conjunction involving the antecedent of **A**, which means that if **A** is true, the strict analysis predicts **B**, whose consequent is the denial of **A**'s, to be false. But the sentences in [Honey](#honey){: #honey-show .tooled} can be interpreted as a perfectly consistent dialogue. This is a sticky situation. The standard response to examples such as these, developed originally by Robert Stalnaker {% cite stalnaker1968 | noname %} and David Lewis {% cite lewis1973 | noname %}, is to translate counterfactual conditionals with a *variably strict* operator. A variably strict operator works in two stages. First, it appeals to context to segregate the set determined by the first operand into preferred and dispreferred classes. It then demands for truth only that the preferred class of elements be a subset of the set determined by the second operand. For conditionals, the semantic value of the operands is a set of worlds or situations, and the preferred class is usually glossed as the *closest possible worlds*.

<!-- Variably strict cond -->
{% def Variably strict conditional %}
  {{ "conditionals|variably strict conditional|translation" | formalize: "notitle" }}
  {{ "conditionals|variably strict conditional|definition" | formalize: "notitle" }}
{% enddef %}

The variably strict analysis avoids the sticky situation because it fails to verify thinning. The closest possible worlds in which Pooh eats less honey need not be a superset of the closest ones in which he both eats less honey and wears his puffy jacket. The ordering relation on the antecedent worlds opens an avenue for the antecedent sets to come apart.

Despite its de-sticking success, Thony Gillies {% cite gillies2007 | noname %} argues that the standard response is not the preferred extraction method. We can preserve the strict analysis of counterfactuals if we allow them to act as monsters {% cite kaplan1977 | noname %}, shifting the index of evaluation in the course of interpretation. A principled monster for counterfactual conditionals shifts the context against which the consequent is evaluated to one that is fixed in part by the antecedent.

<!-- Shifty strict conditionals -->
{% def Shifty strict conditional %}
  {{ "conditionals|shifty strict conditional|translation" | formalize: "notitle" }}
  {{ "conditionals|shifty strict conditional|definition" | formalize: "notitle" }}
{% enddef%}

Monsters are more pragmatically complicated, but they allow us to maintain a simpler semantics. And a simpler semantics is more general. It is a virute of Gillies' extraction technique that it interprets the counterfactual as an operator that takes the face-value antecedent as its first operand. The shifty strict analysis also captures the same effect as the variably strict analysis. The selection function (&delta;(i)) picks a set of worlds from within the set determined by the antecedent, and the selection is then added to the domain against which the consequent is evaluated. The semantic rule still demands set inclusion between the antecedent worlds and consequent worlds, but the shifted contextual restriction on those sets effectively loosens the requirement of strictness. Since there are more worlds included in the set determined by the consequent relative to the domain i<sup>+</sup>(A) than relative to i, the set inclusion demand is more easily met. But since the additionally included worlds are specifically antecedent-relevant, the inclusion demand is not wantonly loose. The result is that the evaluation context for the claim that if Pooh had eaten less honey, he would have fit through the hole is different from the evaluation context for the claim that if he had eaten less honey and worn his puffy coat, he would have gotten stuck. And that difference makes a difference.

The formulation of shifty strict conditionals provided above differs from Gillies' formulation in a couple ways. Primarily, Gillies models evaluation contexts as *hyperdomains* -- nested sets of worlds centered on the evaluation world. The nesting is accomplished by an ordering relation supplied by context. The effect of the context shift enacted by the use of a counterfactual is dictated by this ordering in such a way that the particular set of worlds used to evaluate the counterfactual is the minimal hyperdomain (*closest* set of worlds to the evaluation world) that includes at least some antecedent worlds. Thus, Gillies' framework of choice directly implements the closeness account of counterfactuals.

In contrast, the formulation I have chosen models evaluation domains as unstructured information states, and the context shift is enabled by a contextually determined selection function. I chose this formulation in order to highlight the parallel between counterfactual conditionals and my preferred analysis of bare plurals. But there is a lacuna in my formulation. Because there is no ordering on evaluation domains built into the framework, the operation of the selection function is left underspecified. The manner in which worlds are selected from the set of antecedent worlds and added to the evaluation context for the consequent must be fully determined by the context. We thus end up with a messier {% gloss metasemantics %}, but I think this is preferable. The semantic rules should tell us what is required for truth (or other semantic concepts) but not how to get it. By not building expression-specific formalism (e.g., *hyperdomains*) into the semantic machinery, we keep it more general. Of course, the task of picking a selection function is a large one with which to burden the pragmatic machinery, and I grant that it would be nice to have a more complete story about how this is done. For now, I remain satisfied with specifying constraints on the selection function and leaving its complete definition unspecified.

The other difference between Gillies' and my formulations involves the elements to which the context shift applies. Gillies takes the context shift to be instigated by an *entertainability presupposition* -- that the antecedent be possible relative to the evaluation domain -- carried by the antecedents of conditionals. The presupposition projects up to the whole counterfactual, and it occasionally requires {% gloss accommodation %}, which is the mechanism by which the shift takes place. So, on Gillies proposal, uttering a counterfactual in context first enacts a context shift, taking us to an evaluation domain that includes the closest antecedent worlds to the evaluation world. Then, the entire counterfactual is evaluated relative to the shifted domain. The formulation I have chosen selectively applies the shifted domain to evaluation of the consequent. I believe that doing so has two benefits. First, it allows for a more integrated application of pragmatic and semantic rules. It needn't be that the semantic rules operate only after the context change rules have been exhaustively applied. The linguistic interpretation system is highly nuanced, and this formulation allows for potential feedback between the modules. Second, a virtue of the collaborative update framework is its ability to represent interlocutors selectively modifying previous contributions to discourse. Thus, the selective application of context shifting fits better with the collaborative framework that will form the basis of our analysis of bare plural sentences, to which we now turn.