# State of the art of knowledge-based explainability methods for deep neural networks

## Problem formalization

![image](https://user-images.githubusercontent.com/81907010/181770346-ea579d57-50d3-49c8-862e-43bef09675d6.png)

Reverse engineering approach for explaining deep neural networks : <br>
the learned black box predictor is queried with a test dataset D={X,Y} to produce an oracle &#374;, which associate to each sample x∈X, a label that is not real but assigned by the black box

## Methods in terms of : data type, NN type, explanator, problem and reproducibility

- Step : at which knowledge intervene : Post-hoc (P), Training (T), Designing (D)
- Data types : Images (IMG), Text (TXT), Tabular (TAB), Anything (ANY) 
- Target to explain : Prediction (PRED), Group of predictions (GRP), Whole model (MOD)
- Knowledge Form : Ontology (O), Knowledge Graph (G), Library of concepts (C)

<table>
  <tr>
    <th>Name</th>
    <th>Step</th>
    <th>Data type</th>
    <th>Target</th>
    <th>Knowledge Form</th>
    <th>Code</th>
  </tr>


  <tr>
    <td class="name">TCAV<a href="#tcav">[1]</a> </td>
    <td class="step">P</td>
    <td class="dt">IMG</td>
    <td class="prob">GRP</td>
    <td class="kform">C</td>
    <td class="code"><a href="https://github.com/tensorflow/tcav">&#x2713;</a> </td>
  </tr>

  <tr>
    <td class="name">ACE<a href="#ace">[2]</a> </td>
    <td class="step">P</td>
    <td class="dt">IMG</td>
    <td class="prob">GRP</td>
    <td class="kform">C</td>
    <td class="code"><a href="https://github.com/amiratag/ACE"></a> </td>
  </tr>
  
  
  <tr>
    <td class="name">CCE<a href="#cce">[3]</a> </td>
    <td class="step">P</td>
    <td class="dt">IMG</td>
    <td class="prob">PRED</td>
    <td class="kform">C</td>
    <td class="code"><a href="https://github.com/mertyg/debug-mistakes-cce">&#x2713;</a></td>
  </tr>
  
  
  <tr>
    <td class="name">CACE<a href="#cace">[4]</a> </td>
    <td class="step">P</td>
    <td class="dt">IMG+TXT</td>
    <td class="prob">GRP</td>
    <td class="kform">C</td>
    <td class="code"><a href="https://github.com/chihkuanyeh/concept_exp">&#x2713;</a></td>
  </tr>

  <tr>
    <td class="name">CoCoX<a href="#cocox">[5]</a> </td>
    <td class="step">P</td>
    <td class="dt">IMG</td>
    <td class="prob">PRED</td>
    <td class="kform">C</td>
    <td class="code"><a href="https://github.com/arjunakula/CoCoX">&#x2713;</a></td>
  </tr>

  <tr>
    <td class="name">X-NeSyL(2022) <a href="#xnesyl">[6]</a> </td>
    <td class="step">T</td>
    <td class="dt">IMG</td>
    <td class="prob">PRED</td>
    <td class="kform">G</td>
    <td class="code"><a href="https://github.com/JulesSanchez/X-NeSyL">&#x2713;</a></td>
  </tr>

  <tr>
    <td class="name">EDUCE (2019)<a href="#educe">[7]</a> </td>
    <td class="step">T</td>
    <td class="dt">ILG+TXT</td>
    <td class="prob">PRED</td>
    <td class="kform">C</td>
    <td class="code"><a href="">&#x2715;</a></td>
  </tr>
  
  
  <tr>
    <td class="name">Bisturi (2022)<a href="#bisturi">[5]</a> </td>
    <td class="dt">IMG</td>
    <td class="bb">CNN</td>
    <td class="expl">NC</td>
    <td class="fam">CB</td>
    <td class="prob">MOD</td>
    <td class="code"><a href="https://github.com/rmassidda/bisturi">&#x2713;</a> </td>
    <td class="bbmod">AlexNet ResNet DenseNet </td>
    <td class="ds"><a href="https://github.com/CSAILVision/places365">Places-365</a></td>
    <td class="ex">&#x2713;</td>
    <td class="eval"><a href="https://github.com/rimelcheikh/RnX-SOTA/blob/main/evaluations.md">[L]</a></td>
    <td class="axioms">&#x2715;</td>
  </tr>
  
  
  <tr>
    <td class="name"><a href="#">[]</a> </td>
    <td class="step"></td>
    <td class="dt"></td>
    <td class="prob"></td>
    <td class="kform"></td>
    <td class="code"><a href="">&#x2713;</a></td>
  </tr>
 
  

  
  
</table>

<!--- 
## Methods in terms of : problem, data type, NN

### Outcome explanation
<table>
  <tr>
    <th></th>
    <th>IMG</th>
    <th>TAB</th>
    <th>TXT</th>
    <th>ANY</th>
  </tr>
  
  <tr>
    <td>DNN</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  
  <tr>
    <td>CNN</td>
    <td>GRAD-CAM <a href="#grad-cam">[1]</a></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  
  <tr>
    <td>RNN</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  
  <tr>
    <td>NN</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  
  <tr>
    <td>AGN</td>
    <td></td>
    <td></td>
    <td></td>
    <td>LIME <a href="#lime">[2] </a></td>
  </tr>
</table>

### Model explanation
<table>
  <tr>
    <th></th>
    <th>IMG</th>
    <th>TAB</th>
    <th>TXT</th>
    <th>ANY</th>
  </tr>
  
  <tr>
    <td>DNN</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  
  <tr>
    <td>CNN</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  
  <tr>
    <td>RNN</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  
  <tr>
    <td>NN</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  
  <tr>
    <td>AGN</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
</table>
-->



## References:
<div class="csl-entry"> <a id="bisturi"> [5] </a> Massidda, Riccardo, and Davide Bacciu. "Knowledge-Driven Interpretation of Convolutional Neural Networks." </div>

<div class="csl-entry"> <a id="tcav"> [7] </a> Kim, Been, Martin Wattenberg, Justin Gilmer, Carrie Cai, James Wexler, Fernanda Viegas, et Rory Sayres. « Interpretability Beyond Feature Attribution: Quantitative Testing with Concept Activation Vectors (TCAV) ». arXiv, 7 juin 2018. http://arxiv.org/abs/1711.11279.</div>

<div class="csl-entry"> <a id="abid"> [8] </a>Abid, Abubakar, Mert Yuksekgonul, et James Zou. « Meaningfully Debugging Model Mistakes Using Conceptual Counterfactual Explanations ». In Proceedings of the 39th International Conference on Machine Learning, 66‑88. PMLR, 2022. https://proceedings.mlr.press/v162/abid22a.html. </div>

<div class="csl-entry"> <a id="yeh"> [9] </a>Yeh, Chih-Kuan, Been Kim, Sercan O. Arik, Chun-Liang Li, Tomas Pfister, et Pradeep Ravikumar. « On Completeness-aware Concept-Based Explanations in Deep Neural Networks ». arXiv, 7 février 2022. https://doi.org/10.48550/arXiv.1910.07969.
</div>

<div class="csl-entry"> <a id="diaz"> [10] </a> Díaz-Rodríguez, Natalia, et al. "EXplainable Neural-Symbolic Learning (X-NeSyL) methodology to fuse deep learning representations with expert knowledge graphs: The MonuMAI cultural heritage use case." Information Fusion 79 (2022): 58-83.</div>

<div class="csl-entry"> <a id=""> [11] </a> </div>


<div class="csl-entry"> <a id=""> [] </a> </div>



