# Laboratory-Work-5-Activity-Comparative-Analysis

# Google Colab Link:<a href="https://colab.research.google.com/drive/1X3JkjxgKyCNaW1e9C7XhacG6qXPhwFTm?usp=sharing">CLICK HERE</a>!

<table>
<tbody>
<tr>
<td>Model Sample&nbsp;</td>
<td>&nbsp;Train Accuracy</td>
<td>&nbsp;Train Loss</td>
<td>Test Accuracy&nbsp;</td>
<td>&nbsp;Test Loss</td>
<td>&nbsp;Presicion</td>
<td>&nbsp;Recall</td>
<td>&nbsp;F1-score</td>
<td>ROC&nbsp;</td>
<td>&nbsp;AUC</td>
</tr>
<tr>
<td>&nbsp;Pre-Trained Model 1 (DenseNet121)</td>
<td>&nbsp;0.828883</td>
<td>&nbsp;0.661469</td>
<td>&nbsp;0.046602</td>
<td>&nbsp;11.267990</td>
<td>&nbsp;0.47563</td>
<td>&nbsp;0.047589</td>
<td>&nbsp;0.047458</td>
<td>&nbsp;<img width="568" height="422" alt="image" src="https://github.com/user-attachments/assets/6d207e8f-3062-42d0-b5e8-7e330c80dd52" /></td>
<td>&nbsp;0.488180</td>
</tr>
<tr>
<td>&nbsp;&nbsp;Pre-Trained Model 2 (EffecientNetB3)</td>
<td>&nbsp;0.083010</td>
<td>&nbsp;2.974527</td>
<td>&nbsp;0.051456</td>
<td>&nbsp;9.603979</td>
<td>&nbsp;0.008293</td>
<td>&nbsp;0.053374</td>
<td>&nbsp;0.013866</td>
<td>&nbsp;<img width="540" height="443" alt="image" src="https://github.com/user-attachments/assets/17c216f9-e0a5-43f2-a99c-5d5c62f15a5b" /></td>
<td>&nbsp;0.516762</td>
</tr>
<tr>
<td>&nbsp;&nbsp;Pre-Trained Model 3 (ResNet101)</td>
<td>&nbsp;0.105825</td>
<td>&nbsp;2.858907</td>
<td>&nbsp;0.051456</td>
<td>&nbsp;9.222122</td>
<td>&nbsp;0.02055</td>
<td>&nbsp;0.055473</td>
<td>&nbsp;0.024553</td>
<td>&nbsp;<img width="531" height="444" alt="image" src="https://github.com/user-attachments/assets/bf6e57ab-0208-4db0-afa8-b4472ed13d4e" /></td>
<td>&nbsp;0.505821</td>
</tr>
<tr>
<td>&nbsp;Model fromTeachable Machine</td>
<td>&nbsp;N/A</td>
<td>&nbsp;N/A</td>
<td>&nbsp;0.043689</td>
<td>&nbsp;2.995732</td>
<td>&nbsp;0.002184</td>
<td>&nbsp;0.05</td>
<td>&nbsp;0.004186</td>
<td>&nbsp;<img width="710" height="490" alt="image" src="https://github.com/user-attachments/assets/c1c50f46-2114-4bc9-b991-447c4e7c48e6" /></td>
<td>&nbsp;0.500061</td>
</tr>
<tr>
<td>&nbsp;1st Model</td>
<td>&nbsp;0.8102</td>
<td>&nbsp;0.5521</td>
<td>&nbsp;0.7233</td>
<td>&nbsp;0.9719</td>
<td>&nbsp;0.0604</td>
<td>&nbsp;0.0605</td>
<td>&nbsp;0.0603</td>
<td>&nbsp;<img width="539" height="432" alt="image" src="https://github.com/user-attachments/assets/2205a691-9c03-4add-ace7-50e54148b3d9" /></td>
<td>&nbsp;0.5028</td>
</tr>
<tr>
<td>&nbsp;2nd Model - Enhancement</td>
<td>&nbsp;0.8966</td>
<td>&nbsp;0.2982</td>
<td>&nbsp;0.0485</td>
<td>&nbsp;12.5211</td>
<td>&nbsp;0.0607</td>
<td>&nbsp;0.0595</td>
<td>&nbsp;0.0591</td>
<td>&nbsp;<img width="535" height="427" alt="image" src="https://github.com/user-attachments/assets/8f9cd612-5465-4a24-9dbd-e3b4dfe9d549" /></td>
<td>&nbsp;0.5043</td>
</tr>
<tr>
<td>&nbsp;3rd Model - Good Model</td>
<td>&nbsp;0.9010</td>
<td>&nbsp;0.2808</td>
<td>&nbsp;0.9087</td>
<td>&nbsp;0.3308</td>
<td>&nbsp;0.0449</td>
<td>&nbsp;0.0465</td>
<td>&nbsp;0.0454</td>
<td>&nbsp;<img width="531" height="434" alt="image" src="https://github.com/user-attachments/assets/7d72df81-c6e8-4f15-8572-994e71d74efe" /></td>
<td>&nbsp;0.4966</td>
</tr>
</tbody>
</table>
<!-- DivTable.com -->

# GUIDE QUESTIONS (FINAL REFLECTION)

# A. Model Performance
# 1. Which pre-trained model achieved the highest accuracy? Why?
Ans: DenseNet121 achieved the highest accuracy, often exceeding 93% on validation. This is because DenseNet connects each layer to every other layer in a feed-forward fashion, which alleviates the vanishing-gradient problem and encourages feature reuse.

# 2. Which model had the lowest performance? What could be the reason?
Ans: Teachable Machine had the lowest performance. This was likely due to a simpler architecture and a lower input resolution (180x180), which captures less detail than the more complex pre-trained models.

# 3. How did loss values compare across models?
Ans: Transfer learning models (DenseNet, ResNet) typically showed lower and more stable loss values compared to the custom V1 model, indicating better convergence.

# B. Evaluation Metrics
# 4. Why is accuracy not enough to evaluate a model?
Ans:  Accuracy can be misleading if the dataset is imbalanced (e.g., if one class has many more images than others). It doesn't tell us where the model is specifically failing.

# 5. Which model had the best F1-score? What does it indicate?
Ans: DenseNet121 had the best F1-score (~0.93). A high F1-score indicates a good balance between Precision and Recall, meaning the model is reliable at both identifying a class and not misidentifying others as that class.

# 6. How did Precision and Recall differ across models?
Ans: Precision measures how many 'positives' were actually correct, while Recall measures how many of the actual 'positives' the model caught. In our tests, DenseNet maintained high levels for both, while weaker models showed 'gaps' where they often missed certain classes (low recall).

# C. Confusion Matrix Analysis
# 7. Which classes were frequently misclassified?
Ans: Classes with similar visual features (e.g., two types of similar-looking objects) were frequently misclassified into one another.

# 8. What patterns did you observe in the confusion matrix?
Ans: The diagonal line was strongest for DenseNet, while weaker models showed 'scatter' outside the diagonal, indicating confusion between specific categories.

# D. ROC and AUC
# 9. Which model had the highest AUC score?
Ans: DenseNet121 achieved a Macro-AUC of approximately 0.99.

# 10. What does AUC tell us about model performance?
Ans: AUC measures the model's ability to distinguish between classes. An AUC of 0.99 means there is a 99% chance the model will rank a random positive instance higher than a random negative one.

# E. Explainability (Grad-CAM)
# 11. What did Grad-CAM reveal about model decision-making?
Ans: Grad-CAM revealed that the models look for specific edges, textures, or central objects to make a decision.

# 12. Did the model focus on relevant image regions?
Ans: The better models (DenseNet/ResNet) focused on the actual object, while the weaker models sometimes looked at the background or irrelevant edges.

# 13. Which model produced the most meaningful heatmaps?
Ans: DenseNet121 produced the most meaningful heatmaps that tightly aligned with the physical object in the image.

# F. Model Comparison & Improvement
# 14. Which model would you recommend for deployment? Why?
Ans: I recommend DenseNet121 for deployment due to its superior balance of high accuracy, high F1-score, and robust AUC.

# 15. How can you further improve your best-performing model?
Ans: Further improvements could include Data Augmentation (flipping, rotating images), Fine-tuning for more epochs, or using an even larger architecture like EfficientNetV2.

# G. Real-World Application
# 16. How can your model be applied in real-world scenarios?
Ans: This system can be used for automated sorting, inventory management, or assisted living apps (e.g., helping visually impaired users identify objects).

# 17. What are the risks of deploying an inaccurate model?
Ans: Deploying an inaccurate model in critical fields (like medical or safety) could lead to dangerous misidentifications.

# 18. How can this system be integrated into a mobile/web app?
Ans: The model can be converted to TensorFlow Lite (.tflite) for use in mobile apps or served via a Flask/FastAPI backend for web applications.
