This project seeks to create a diagnostic system based on deep learning for the detection and classification of lung conditions from chest X-ray images, specifically for COVID-19, Pneumonia, and Normal (healthy) states. At the core of the classification framework is a VGG19 Convolutional Neural Network fine-tuned for its excellent performance in visual tasks.

In healthcare, accuracy is not enough for an AI model; the decisions also need to be interpretable and clinically transparent. To tackle this, the project introduces a wide range of XAI techniques that visually and analytically justify how the model arrived at a specific prediction. These justifications play a pivotal role in establishing trust with doctors and allowing for safe deployment of AI in actual diagnostic environments.

✅About Project Does**

🔍 Classifies Lung Diseases Using VGG19
  Utilizes a pre-trained **VGG19** model, fine-tuned on chest X-ray images. The model outputs predictions for three classes: COVID-19, Pneumonia, and Normal.

🖼️ **Processes and Augments X-ray Data**
  Performs image resizing, normalization, and augmentation (rotations, shifts, zooms, flips) to improve model generalization and robustness.

🧠 **Implements Multiple XAI Techniques to Explain Predictions**

  ### 📌 **Grad-CAM (Gradient-weighted Class Activation Mapping)**

  * Highlights the spatial regions in an image that influenced the model’s decision the most.

  ### 📌 **LIME (Local Interpretable Model-Agnostic Explanations)**

  * Explains individual predictions by approximating the model locally with an interpretable model (e.g., linear model).

  ### 📌 **Integrated Gradients**

  * A gradient-based method that attributes a prediction to each input feature by integrating the gradients along the path from a baseline to the input.It produces precise pixel-level attribution maps, useful for identifying fine-grained visual cues that influenced the model.

  ### 📌 **Layer-wise Relevance Propagation (LRP)**

  * Propagates the prediction backward through the network, distributing relevance scores to each neuron and input feature.

  ### 📌 **Decision Tree Interpretation**

  * A simple interpretable decision tree model is used either:

    * as a surrogate to approximate CNN behavior in a human-readable format, or
    * to classify feature representations extracted from intermediate CNN layers.

  ### 📌 **Feature Map Visualization (Layer Outputs)**

  * Helps interpret how the network processes and transforms input images layer by layer, offering insight into **what the model "sees"** at different depths.


