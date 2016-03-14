{% capture strictcond %}
{% include sem.html term='*A* &#x297d; B' index="i" %}
{% endcapture %}

{% capture shiftstrictcond %}
{% include sem.html term='*A* &#x297d;<sub>s</sub> B' index="i" %}
{% endcapture %}
 
{% capture univgen %}
{% include sem.html term='&forall;(A)(B)' index="i" %}
{% endcapture %}

{% capture subset %}
{% include sem.html term='A' index="i" %} &sube; {% include sem.html term='B' index="i" %}
{% endcapture %}

{% capture shiftsubset %}
{% include sem.html term='A' index="i" %} &sube; {% include sem.html term='B' index="i+A" %}
{% endcapture %}

{% capture varstrictcond %}
{% include sem.html term='A <span style="letter-spacing:-4px;">&#x25a1;&rarr;</span> B' index="i" %}
{% endcapture %} 

{% capture acsubb %}
{% include sem.html term='A &amp; C' index='i' %} &sube; {% include sem.html term='B' index='i' %}
{% endcapture %}

{% capture acstrictb %}
{% include sem.html term='(A &amp; C) &#x297d; B' index='i' %}
{% endcapture %}

{% capture aprefsem %}
{% include sem.html term='*A*<sub>pref</sub>' index="i" %}
{% endcapture %}

{% capture aprefset %}
{ *x* &isin; *A* : *x* &isin; &delta;(*i*) }
{% endcapture %}

{% capture aprefsubb %}
{% include sem.html term='A<sub>pref</sub>' index="i" %} &sube; {% include sem.html term='B' index="i" %}
{% endcapture %}

<!-- English counterfactual -->
{% capture counterfact %}
If had &#x231c;A&#x231d;, would have &#x231c;B&#x231d;
{% endcapture %}

<!-- English bare plural -->
{% capture bareplural %}
&#x231c;As&#x231d; are &#x231c;B&#x231d;
{% endcapture %}

<!-- Variably strict conditional -->
{% capture vsc %}
<span style="letter-spacing:-4px;">&#x25a1;&rarr;</span>
{% endcapture %}

{% capture abvsc %}
{% capture abvscnowrap %}
{% include op.html kind="op" op1="A" op2="B" conn=vsc %}
{% endcapture %}
{{ abvscnowrap | markdownify | remove: '<p>' | remove: '</p>' }}
{% endcapture %}

{% capture abvscsem %}
{% include sem.html term=abvsc index="i" %}
{% endcapture %}