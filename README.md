# State of the art of knowledge-based explainability methods for deep neural networks

## Problem formalization

![image](https://user-images.githubusercontent.com/81907010/181770346-ea579d57-50d3-49c8-862e-43bef09675d6.png)

Reverse engineering approach for explaining deep neural networks : <br>
the learned black box predictor is queried with a test dataset D={X,Y} to produce an oracle &#374;, which associate to each sample x∈X, a label that is not real but assigned by the black box

## Methods in terms of : data type, NN type, explanator, problem and reproducibility

- Data types : Images (IMG), Text (TXT), Tabular (TAB), Anything (ANY) 
- Black Boxes : Deep neural networks (DNN), Convolutional neural networks (CNN), Recurrent neural networks (RNN), Agnostic (AGN)
- Explanator : Feature importance (FI), Saliency map (SM), Marginal Contribution (MC), Neural Circuit (NC), Concept (C)
- Family : Interpretable Local Surrogates (ILS), Occlusion Analysis (OA), Layerwise Relevance Propagation (LRP), Attribution methods(AM), Concept-Based (CB)
- Problem : Outcome explanation (OUT), Model explanation (MOD)

<table>
  <tr>
    <th>Name</th>
    <th>Data type</th>
    <th>Black Box</th>
    <th>Explanator</th>
    <th>Family</th>
    <th>Problem</th>
    <th>Code</th>
    <th>BB Model</th>
    <th>Dataset</th>
    <th>Examples</th>
    <th>Evaluation</th>
    <th>Axiomatic</th>
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
    <td class="name">TCAV<a href="#tcav">[7]</a> </td>
    <td class="dt">IMG</td>
    <td class="bb">CNN</td>
    <td class="expl">C</td>
    <td class="fam">CB</td>
    <td class="prob">MOD</td>
    <td class="code"><a href="https://github.com/tensorflow/tcav">&#x2713;</a> </td>
    <td class="bbmod"><a href="https://pytorch.org/hub/pytorch_vision_googlenet/">GoogleNet</a>
                      <a href="https://keras.io/api/applications/inceptionv3/">InceptionV3</a></td>
    <td class="ds"><a href="https://www.kaggle.com/datasets/google-brain/messidor2-dr-grades">MESSIDOR-2 DR</a></td>
    <td class="ex">&#x2713;</td>
    <td class="eval"><a href="https://github.com/rimelcheikh/RnX-SOTA/blob/main/evaluations.md">[I]</a></td>
    <td class="axioms">&#x2715;</td>
  </tr>
  
  
  <tr>
    <td class="name">CCE<a href="#abid">[8]</a> </td>
    <td class="dt">IMG</td>
    <td class="bb">CNN</td>
    <td class="expl">C</td>
    <td class="fam">CB</td>
    <td class="prob">OUT+MOD</td>
    <td class="code"><a href="https://github.com/mertyg/debug-mistakes-cce">&#x2713;</a></td>
    <td class="bbmod">ResNet18 <br> <a href="https://github.com/mattgroh/fitzpatrick17k">Fitzpatrick17k</a></td>
    <td class="ds"><a href="https://github.com/mattgroh/fitzpatrick17k">Fitzpatrick17k</a>
                    <a href="https://github.com/bethgelab/imagecorruptions">imagecorruptions</a></td>
    <td class="ex">&#x2713;</td>
    <td class="eval"><a href="https://github.com/rimelcheikh/RnX-SOTA/blob/main/evaluations.md">[J]</a></td>
    <td class="axioms">&#x2715;</td>
  </tr>
  
  
  <tr>
    <td class="name">Completeness-aware<a href="#yeh">[9]</a> </td>
    <td class="dt">ANY</td>
    <td class="bb">DNN</td>
    <td class="expl">C</td>
    <td class="fam">CB</td>
    <td class="prob">OUT+MOD</td>
    <td class="code"><a href="https://github.com/chihkuanyeh/concept_exp">&#x2713;</a></td>
    <td class="bbmod"><a href="https://keras.io/api/applications/inceptionv3/">InceptionV3</a></td>
    <td class="ds"><a href="https://academictorrents.com/details/1490aec815141cdb50a32b81ef78b1eaf6b38b03">AwA</a> <br>
                    <a href="https://www.kaggle.com/datasets/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews">IMDB</a></td>
    <td class="ex">&#x2713;</td>
    <td class="eval"><a href="https://github.com/rimelcheikh/RnX-SOTA/blob/main/evaluations.md">[K]</a></td>
    <td class="axioms">&#x2713;</td>
  </tr>
  
  <tr>
    <td class="name">X-NeSyL(2022) <a href="#diaz">[10]</a> </td>
    <td class="dt">IMG</td>
    <td class="bb">DNN</td>
    <td class="expl"></td>
    <td class="fam">AM</td>
    <td class="prob">MOD</td>
    <td class="code"><a href="https://github.com/JulesSanchez/X-NeSyL">&#x2713;</a></td>
    <td class="bbmod"><a href=""></a></td>
    <td class="ds"><a href="https://github.com/ari-dasci/OD-MonuMAI">MonuMAI</a></td>
    <td class="ex">&#x2713;</td>
    <td class="eval"><a href="https://github.com/rimelcheikh/RnX-SOTA/blob/main/evaluations.md">[M]</a></td>
    <td class="axioms">&#x2715;</td>
  </tr>
  
  
  <tr>
    <td class="name">CoCoX<a href="#">[11]</a> </td>
    <td class="dt">IMG</td>
    <td class="bb">CNN</td>
    <td class="expl">Concept</td>
    <td class="fam"></td>
    <td class="prob"></td>
    <td class="code"><a href="https://github.com/arjunakula/CoCoX">&#x2713;</a> </td>
    <td class="bbmod"><a href=""></a></td>
    <td class="ds"></td>
    <td class="ex">&#x2713;</td>
    <td class="eval"><a href="https://github.com/rimelcheikh/RnX-SOTA/blob/main/evaluations.md">[]</a></td>
    <td class="axioms"></td>
  </tr>

  <tr>
    <td class="name"><a href="#">[]</a> </td>
    <td class="dt"></td>
    <td class="bb"></td>
    <td class="expl"></td>
    <td class="fam"></td>
    <td class="prob"></td>
    <td class="code"><a href=""></a> </td>
    <td class="bbmod"><a href=""></a></td>
    <td class="ds"></td>
    <td class="ex"></td>
    <td class="eval"><a href="https://github.com/rimelcheikh/RnX-SOTA/blob/main/evaluations.md">[]</a></td>
    <td class="axioms"></td>
  </tr>
  
  
  <tr>
    <td class="name"><a href="#">[]</a> </td>
    <td class="dt"></td>
    <td class="bb"></td>
    <td class="expl"></td>
    <td class="fam"></td>
    <td class="prob"></td>
    <td class="code"><a href=""></a> </td>
    <td class="bbmod"><a href=""></a></td>
    <td class="ds"></td>
    <td class="ex"></td>
    <td class="eval"><a href="https://github.com/rimelcheikh/RnX-SOTA/blob/main/evaluations.md">[]</a></td>
    <td class="axioms"></td>
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



