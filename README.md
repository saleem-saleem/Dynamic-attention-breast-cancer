<h1>Dynamic Attention Fusion for Breast Cancer Classification</h1>



<p>This repository provides a Python implementation of an attention-based multimodal deep learning framework that combines mammographic images and incomplete clinical records for breast cancer classification.</p>



<h2>1. Overview</h2>

<p>The proposed framework employs separate image and clinical-data encoders. A dynamic attention mechanism assigns case-specific weights to both modalities before fusion and classification.</p>

<p>The framework includes:</p>

<ul>
<li>Three-block CNN for mammogram feature extraction.</li>
<li>Clinical MLP with missing-value indicators.</li>
<li>Dynamic attention-based multimodal fusion.</li>
<li>Binary breast cancer classification.</li>
<li>Temperature scaling for probability calibration.</li>
<li>Patient-independent training and evaluation.</li>
<li>Five-seed experiments and five-fold cross-validation.</li>
<li>Baseline comparisons, statistical testing and explainability.</li>
</ul>

<h2>2. Proposed Model Architecture</h2>

<table>
<tr><th>Component</th><th>Architecture</th></tr>
<tr><td>Input image</td><td>224 × 224 × 3</td></tr>
<tr><td>CNN Block 1</td><td>64 filters, 3 × 3, ReLU, MaxPooling</td></tr>
<tr><td>CNN Block 2</td><td>128 filters, 3 × 3, ReLU, MaxPooling</td></tr>
<tr><td>CNN Block 3</td><td>256 filters, 3 × 3, ReLU, MaxPooling</td></tr>
<tr><td>Image embedding</td><td>Global Average Pooling + Dense(128)</td></tr>
<tr><td>Clinical input</td><td>4 clinical values + 4 missingness indicators</td></tr>
<tr><td>Clinical encoder</td><td>Dense(64), ReLU</td></tr>
<tr><td>Attention module</td><td>32-dimensional projections and softmax weighting</td></tr>
<tr><td>Fusion</td><td>192-dimensional weighted concatenation</td></tr>
<tr><td>Classification head</td><td>Dense(64), ReLU, Dropout(0.40)</td></tr>
<tr><td>Output</td><td>Dense(1), binary classification</td></tr>
<tr><td>Total parameters</td><td>422,945</td></tr>
</table>

<h2>3. Software Requirements</h2>

<ul>
<li>Python 3.11 recommended</li>
<li>TensorFlow 2.16–2.18</li>
<li>NumPy</li>
<li>Pandas</li>
<li>SciPy</li>
<li>Scikit-learn</li>
<li>Matplotlib</li>
<li>Pillow</li>
<li>PyYAML</li>
<li>pydicom</li>
<li>Git</li>
</ul>





