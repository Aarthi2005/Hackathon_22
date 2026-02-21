**# Hackathon_22**

**PROBLEM STATEMENT**

**Build → Break → Improve:**

1.Build a detector → train & evaluate with explainability.

2.Break it → craft adversarial modifications that fool the model.

3.Improve it → analyze weaknesses and propose defenses to make the detector more robust.


**Phase 1:** Build – Synthetic Image Detector

        Goal: Create a classifier to distinguish real vs. AI-generated images.
        
        Approach:
        
        Either build a custom CNN or fine-tune a pretrained model (ResNet, EfficientNet, etc.).
        
        Train on the provided dataset.
        
        
        Evaluation Metrics: 
        
        Accuracy, Precision, Recall, F1-score, Confusion Matrix.
        
        
        Explainability:
        
        Use Grad-CAM, saliency maps, or similar to show which image regions drive the model’s decisions.


**Phase 2:** Break – Adversarial Modifications

        Goal: Fool the detector into misclassifying synthetic images as real.
        
        Process:
        
        Pick synthetic test images the detector correctly flags as fake.
        
        Iteratively apply small modifications (pixel perturbations, frequency-domain tweaks, filtering, latent-space edits).
        
        Track confidence scores at each step until the detector is tricked.
        
        
        Key Principle: 
        
        Changes should be minimal — images must still look realistic to humans.
        
        Analysis:
        
        Explain why the evasion worked (e.g., suppression of texture patterns, alteration of color statistics).


**Phase 3:** Improve – Robustness Proposal

      Goal: Strengthen the detector against the weaknesses revealed.
      
      Process:
      
      Use Grad-CAM/saliency maps + evasion results to identify what the model relied on (textures, artifacts, color cues, etc.).
      
      Pinpoint blind spots and vulnerabilities.
      
      Propose concrete improvements (e.g., retraining with adversarial examples, adding frequency-domain features, ensemble methods).
      
      Emphasis:
      
      The reasoning behind the improvement is more important than the attack itself.
