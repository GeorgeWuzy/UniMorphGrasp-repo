<div align="center">

<div style="font-size: 48px; font-weight: bold;">
UniMorphGrasp: Diffusion Model with Morphology-Awareness for Cross-Embodiment Dexterous Grasp Generation
</div>

<br>

<video src="figs/demo.mp4" controls="controls" width="90%"></video>

<br>
<br>

<div style="font-size: 24px; font-weight: bold;">Abstract</div>
<br>
<p style="text-align: justify;">
Cross-embodiment dexterous grasping aims to generate stable and diverse grasps for robotic hands with varying structures. Existing methods are either hand-specific, computationally prohibitive, or fail to generalize beyond the training distribution when encountering novel hand structures. Motivated by the observation that dexterous hands inherently possess graph-structured morphologies, we propose <span style="color: #0070C0">UniMorphGrasp</span>, a morphology-aware diffusion model that integrates explicit morphological information into the generative process for cross-embodiment dexterous grasp synthesis. Our approach first maps diverse hand structures into a unified human-like hand representation, and then employs a morphology-aware encoder that conditions grasp generation on graph-structured morphological features. We further introduce a morphology-aware loss function that leverages hierarchical kinematic relationships to guide training. Extensive experiments demonstrate that UniMorphGrasp achieves state-of-the-art performance on existing benchmarks and successfully <span style="color: #0070C0">generalizes to novel hand structures in a zero-shot way</span>, enabling practical cross-embodiment grasp deployment.
</p>

<img src="figs/teaser.png" alt="Teaser Image" width="70%">

<br>
<br>
<hr> <br>
<br>

<div style="font-size: 24px; font-weight: bold;">Method</div>
<br>
<img src="figs/pipeline.png" alt="Pipeline Image" width="80%">

<p style="text-align: justify;">
<span style="color: #0070C0">(Left)</span> The overview of our proposed UniMorphGrasp for cross-embodiment dexterous grasp generation. Given an object point cloud and an arbitrary hand morphology extracted from its URDF specification (mapped to a pre-defined canonical hand format), we employ a morphology encoder to extract morphology representations from the hand's joint structure. The hand pose (noised via a diffusion scheduler in training) is embedded through a linear layer, and concatenated with its active joint mask embedding to obtain the hand representation. This representation is then processed through a morphology-aware denoising model, where the iterative process is conditioned on both the morphology representation and the point cloud representation extracted via a Point Transformer. The entire framework is trained using a morphology-aware loss function. <span style="color: #0070C0">(Right)</span> The structure of our morphology-aware denoising model, which is conditioned on the encoded morphology and the point cloud representations via cross-attention.
</p>

<br>
<br>
<hr> <br>
<br>

<div style="font-size: 24px; font-weight: bold;">Method Performance</div>
<br>
<img src="figs/multidex.gif" alt="MultiDex Performance" width="80%">
<br><br>
<img src="figs/more_multidex.gif" alt="More MultiDex Results" width="80%">
<br><br>
<img src="figs/quantitative1.png" alt="Quantitative Results 1" width="80%">

<br>
<br>
<hr> <br>
<br>

<div style="font-size: 24px; font-weight: bold;">Zero-Shot Generalization to Novel Hand Morphologies</div>
<br>
<img src="figs/generalization1.gif" alt="Generalization 1" width="80%">
<br><br>
<img src="figs/generalization2.gif" alt="Generalization 2" width="80%">

<br>
<br>
<hr> <br>
<br>

<div style="font-size: 24px; font-weight: bold;">Cross-Dataset Results</div>
<br>
<img src="figs/multi-graspllm.gif" alt="Multi GraspLLM" width="80%">
<br><br>
<img src="figs/objaverse.gif" alt="Objaverse Results" width="80%">
<br><br>
<img src="figs/quantitative2.png" alt="Quantitative Results 2" width="80%">

<br>
<br>
<hr> <br>
<br>

<div style="font-size: 24px; font-weight: bold;">Real-World Experiments</div>
<br>
<img src="figs/real-world1.gif" alt="Real World 1" width="80%">
<br><br>
<img src="figs/real-world2.gif" alt="Real World 2" width="80%">
<br><br>
<img src="figs/quantitative3.png" alt="Quantitative Results 3" width="80%">

</div>
