# garbage-classifier
"An image classification project using deep learning to identify and sort different types of garbage — part of my goal to apply AI for environmental sustainability."

🗑️ Garbage Classification with MobileNetV2
A deep learning project to classify garbage into categories like cardboard, metal, glass, and more — using MobileNetV2 for lightweight performance and Google Colab for training and evaluation.

📂 Dataset
- 7 classes: cardboard, metal, glass, paper, plastic, trash, organic
- Image size: 224x224
- Augmentation applied to underrepresented classes (e.g. cardboard, trash)
- 
🧠 Model Architecture
- Base model: MobileNetV2 (frozen for transfer learning)
- Classifier: GlobalAveragePooling + Dense output
- Optimizer: Adam, Loss: categorical_crossentropy
- Trained for 10 epochs with early stopping
- 
🔍 Evaluation Results
- Test Accuracy: 73%
- Confusion Matrix:
- ### Confusion Matrix Summary

| True Class | Most Confused With | Notes |
|------------|--------------------|-------|
| Cardboard  | Metal              | Often misclassified due to visual similarity |
| Glass      | Metal              | 100% misclassified as metal |
| Metal      | ✅ Correct          | Perfect predictions |
| Paper      | Metal              | Weak separation |
| Plastic    | Metal              | Needs improvement |
| Trash      | Metal              | High confusion |


Class-wise observations:
- Cardboard and glass had initial misclassifications
- Augmentation and retraining improved class performance

📦 Deployment Plan
- Possible deployment via Gradio web app
- Lightweight enough for mobile deployment using TensorFlow Lite

🚀 How to Run
# Clone this repo
git clone https://github.com/yourusername/garbage-classification.git

# Open notebook in Colab
# Or run main notebook locally with required libraries


📄 Requirements
tensorflow
numpy
matplotlib
seaborn
opencv-python


(Full list in requirements.txt)
🏷️ License
MIT License – free to use, modify, and share!



