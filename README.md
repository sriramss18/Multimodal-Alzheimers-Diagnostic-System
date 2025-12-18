Multimodal Alzheimer’s Diagnostic Web Application
==================================================

This project is an AI-powered web application that assists in the early detection of Alzheimer’s disease using brain MRI scans. It combines a deep learning model for image classification, Grad-CAM–based explainability, and an integrated medical chatbot, all deployed through a Streamlit interface for practical clinical and research use.

Objective
---------

The main objectives of this system are to:  

- Classify MRI brain scans into Alzheimer’s-related categories (for example, Normal vs Demented) using a CNN-based model.
- Visualize important brain regions influencing the model’s prediction using Grad-CAM heatmaps to improve transparency and clinician trust.
- Provide an interactive chatbot that explains results in simple language and answers general questions about Alzheimer’s disease.

This tool is intended for educational and research purposes and is not a replacement for professional medical diagnosis.

Key Features
------------

- **MRI Upload and Preprocessing**: Users can upload brain MRI images (JPG/PNG, optionally NIfTI), which are automatically resized and normalized to match the model’s training configuration.
- **Deep Learning–Based Classification**: A convolutional neural network (for example, ResNet or MobileNet) predicts the presence or stage of Alzheimer’s disease from the MRI scan and returns a label with a confidence score.
- **Grad-CAM Explainability**: The application generates Grad-CAM heatmaps that highlight critical regions in the MRI image contributing most to the prediction, improving interpretability of the model’s decisions.
- **Integrated Medical Chatbot**: A chatbot interface allows users to ask questions about Alzheimer’s disease, symptoms, risk factors, and to obtain natural-language explanations of the model output.
- **Results History and Reporting**: Recent predictions, timestamps, and key metadata are stored so users can review previous analyses and export results for documentation or research.
- **Streamlit Web UI**: A clean, responsive Streamlit front end provides a straightforward workflow from upload → analyze → view prediction and Grad-CAM → chat.

Application Workflow
--------------------

1. **Home Page / Dashboard**  
   The user lands on a dashboard showing the project title, a brief description, and clear instructions. From here, they can upload an MRI scan, access previous results, or open the chatbot.

2. **MRI Upload**  
   The user selects an MRI image through a file uploader. The application validates the file type and displays a preview, ensuring the correct scan is selected before analysis.

3. **Prediction and Grad-CAM**  
   After the user selects “Analyze”, the backend runs preprocessing and feeds the image to the trained CNN. The result page displays:  
   - Predicted class and confidence score  
   - Original MRI image  
   - Grad-CAM heatmap overlay highlighting disease-relevant regions  

   This helps clinicians visually verify whether the model focuses on medically meaningful brain structures.

4. **Chatbot Interaction**  
   With the prediction context available, the user can open the chatbot and ask follow-up questions such as “What does this result mean?”, “What are typical symptoms?”, or “What are the next steps?”. The chatbot responds in clear, understandable language.

5. **History and Export**  
   Each analysis (image name, prediction, confidence, date/time) is logged so users can revisit previous scans and use them for comparison, presentations, or further research.

Model and Data (High-Level)
---------------------------

- **Model**: Convolutional neural network (for example, ResNet or MobileNet) trained on publicly available MRI datasets for Alzheimer’s disease classification.
- **Explainability**: Grad-CAM is applied to the last convolutional layers to generate class-specific attention maps.
- **Use Case**: Demonstrates how deep learning, explainable AI, and conversational interfaces can be combined into a practical decision-support tool for neurodegenerative disease screening.


