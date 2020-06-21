<h3 id="turbomachines"><s>Turbomachines</s></h3>
<ul>
<li><s>Ajouter section general</s>
<ul>
<li><s>similiratité</s></li>
<li><s>Triangle de vitesse</s></li>
<li><s>enthalpy variation</s></li>
</ul>
</li>
</ul>
<h3 id="thermo"><s>Thermo</s></h3>
<ul>
<li><s>Ajouter section a propos des différentes transformations</s></li>
</ul>
<h3 id="cycle-de-brayton"><s>Cycle de Brayton</s></h3>
<ul>
<li><s>Corriger et commenter les graphes</s></li>
</ul>
<h2 id="implementation-composants">Implementation composants</h2>
<h3 id="fluides---propriété">Fluides - propriété</h3>
<ul>
<li>Gas
<ul>
<li>Tables NASA pour l’enthalpie et le cp (pour augmenter la rapidité) – regression polynomiale</li>
<li>Gas constant - relation avec fuel air ratio</li>
<li>viscosité dynamique et conductivité thermique --&gt; CoolProp</li>
<li>utilisation des fractions massiques/molaires pour le calcul de variables thermo d’un mélange de gaz idéaux</li>
</ul>
</li>
<li>Liquide (eau)
<ul>
<li>CoolProp pour tout car enthalpie,  cp et entropie dépendent de la température <strong>et</strong> de la pression</li>
<li></li>
</ul>
</li>
</ul>
<h3 id="turbomachines-1">Turbomachines</h3>
<ul>
<li>Expansion/compression --&gt; equations (intégrales,…)</li>
<li>Map de performance
<ul>
<li>Implémentation
<ul>
<li>Cas particulier de la turbine</li>
<li>Délimitation de la zone de fonctionnement compresseur</li>
</ul>
</li>
<li>Vérification de la précision de l’interpolation</li>
<li>Methode de stockage</li>
</ul>
</li>
</ul>
<h3 id="chambre-de-combustion">Chambre de combustion</h3>
<ul>
<li>Calcul de la composition des gaz d’échappement</li>
<li>Calcul du PCI</li>
<li>Conservation de l’enthalpie</li>
</ul>
<h3 id="echangeur-de-chaleur">Echangeur de chaleur</h3>
<ul>
<li>Regenerateur
<ul>
<li><span class="katex--inline"><span class="katex"><span class="katex-mathml"><math><semantics><mrow><msub><mi>T</mi><mrow><mi>s</mi><mi>u</mi></mrow></msub></mrow><annotation encoding="application/x-tex">T_{su}</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 0.83333em; vertical-align: -0.15em;"></span><span class="mord"><span class="mord mathdefault" style="margin-right: 0.13889em;">T</span><span class="msupsub"><span class="vlist-t vlist-t2"><span class="vlist-r"><span class="vlist" style="height: 0.151392em;"><span class="" style="top: -2.55em; margin-left: -0.13889em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight"><span class="mord mathdefault mtight">s</span><span class="mord mathdefault mtight">u</span></span></span></span></span><span class="vlist-s">​</span></span><span class="vlist-r"><span class="vlist" style="height: 0.15em;"><span class=""></span></span></span></span></span></span></span></span></span></span> connu</li>
<li><span class="katex--inline"><span class="katex"><span class="katex-mathml"><math><semantics><mrow><mover accent="true"><mi>m</mi><mo>˙</mo></mover></mrow><annotation encoding="application/x-tex">\dot{m}</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 0.66786em; vertical-align: 0em;"></span><span class="mord accent"><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height: 0.66786em;"><span class="" style="top: -3em;"><span class="pstrut" style="height: 3em;"></span><span class="mord"><span class="mord mathdefault">m</span></span></span><span class="" style="top: -3em;"><span class="pstrut" style="height: 3em;"></span><span class="accent-body" style="left: -0.13889em;">˙</span></span></span></span></span></span></span></span></span></span> connu</li>
</ul>
</li>
<li>Echangeur d’eau
<ul>
<li><span class="katex--inline"><span class="katex"><span class="katex-mathml"><math><semantics><mrow><msub><mi>T</mi><mrow><mi>s</mi><mi>u</mi></mrow></msub></mrow><annotation encoding="application/x-tex">T_{su}</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 0.83333em; vertical-align: -0.15em;"></span><span class="mord"><span class="mord mathdefault" style="margin-right: 0.13889em;">T</span><span class="msupsub"><span class="vlist-t vlist-t2"><span class="vlist-r"><span class="vlist" style="height: 0.151392em;"><span class="" style="top: -2.55em; margin-left: -0.13889em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight"><span class="mord mathdefault mtight">s</span><span class="mord mathdefault mtight">u</span></span></span></span></span><span class="vlist-s">​</span></span><span class="vlist-r"><span class="vlist" style="height: 0.15em;"><span class=""></span></span></span></span></span></span></span></span></span></span> connu</li>
<li><span class="katex--inline"><span class="katex"><span class="katex-mathml"><math><semantics><mrow><msub><mi>T</mi><mrow><mi>e</mi><mi>x</mi></mrow></msub></mrow><annotation encoding="application/x-tex">T_{ex}</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 0.83333em; vertical-align: -0.15em;"></span><span class="mord"><span class="mord mathdefault" style="margin-right: 0.13889em;">T</span><span class="msupsub"><span class="vlist-t vlist-t2"><span class="vlist-r"><span class="vlist" style="height: 0.151392em;"><span class="" style="top: -2.55em; margin-left: -0.13889em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight"><span class="mord mathdefault mtight">e</span><span class="mord mathdefault mtight">x</span></span></span></span></span><span class="vlist-s">​</span></span><span class="vlist-r"><span class="vlist" style="height: 0.15em;"><span class=""></span></span></span></span></span></span></span></span></span></span> eau connu</li>
<li><span class="katex--inline"><span class="katex"><span class="katex-mathml"><math><semantics><mrow><mover accent="true"><mi>m</mi><mo>˙</mo></mover></mrow><annotation encoding="application/x-tex">\dot{m}</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 0.66786em; vertical-align: 0em;"></span><span class="mord accent"><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height: 0.66786em;"><span class="" style="top: -3em;"><span class="pstrut" style="height: 3em;"></span><span class="mord"><span class="mord mathdefault">m</span></span></span><span class="" style="top: -3em;"><span class="pstrut" style="height: 3em;"></span><span class="accent-body" style="left: -0.13889em;">˙</span></span></span></span></span></span></span></span></span></span> gas connu</li>
</ul>
</li>
<li>Calcul de l’éfficacité de l’échangeur<br>
wo</li>
</ul>

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTU1MzQxOTYsLTEwOTc1NDU4NThdfQ==
-->