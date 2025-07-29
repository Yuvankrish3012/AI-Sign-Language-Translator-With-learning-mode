#  AI Sign Language Translator

An advanced deep learning project to translate American, Indian, and Argentinian Sign Language from images and videos into text, using **CNN, ResNet, MobileNetV2**, and **CNN-LSTM** models — all inside a beautiful **Streamlit Web App**.

---

## 🚀 Final Feature List

### 📁 I. Dataset Handling

- ✅ Merged multiple datasets:
  - ASL Alphabet Dataset (A-Z, "del", "nothing", "space")
  - Indian Sign Language Dataset (Alphabets & Numbers)
  - LSA64 Dataset (Argentinian Sign Language - 64 signs)
  - Mendeley Dynamic Sign Language Dataset (Video-based)

- 🔄 Static Dataset Preprocessing:
  - Resized images to a **uniform dimension** (e.g., 64×64)
  - Normalized pixel values (0–1 range)

- 🎞 Dynamic Dataset Preprocessing:
  - Extracted frames from `.mp4` / `.mov` videos
  - Stored frames as `.jpg` images for training

---

### 🧠 II. Model Development

| Model           | Purpose                         |
|----------------|----------------------------------|
| CNN            | Static image recognition         |
| CNN + LSTM     | Dynamic video-based prediction   |
| ResNet         | Accurate image classification    |
| MobileNetV2    | Lightweight + fast predictions   |

- 🚀 Optimized data loading with `.npy` format
- 🧠 Reduced training lag & GPU overload
- 🛠 Fine-tuned with **transfer learning** (ResNet, MobileNetV2)

> 📊 **Visualization – Model Accuracy & Loss Curves**  
> *(Insert Training Graphs Image Here)*

---

### 🔍 III. Testing and Predictions

#### 📷 Image-based Prediction
- Upload a single image.
- Get the predicted sign instantly.

#### 🎞 Video-based Prediction
- Upload video clip (`.mp4` / `.mov`)
- Frames extracted → passed to CNN-LSTM → final sign predicted


#### 🔠 Word Formation from Images
- Upload multiple images (one per letter)
- Model combines predictions into a full word


---

### 🧪 IV. Interactive Learning Mode

1. **Step-by-Step Spelling**
   - User uploads images one by one for a word.
   - System checks each letter.

2. **Real-time Feedback**
   - Upload an image.
   - See prediction and model confidence.
   - Compare with expected output.

3. **Word Generation**
   - Combines recognized letters into word output.



---

### 🧬 V. Model Improvement & Fine-Tuning

- ✅ Fine-tuned ResNet & MobileNetV2 models
- ✅ Updated models saved as `.h5`
- ✅ **Model Learning Mode**: System learns new patterns on user feedback (foundation for incremental training)

---

### 🌐 VI. Deployment and Finalization

- ✅ Final models exported in `.h5` for reuse:
  - `asl_sign_language_model_Resnet.h5`
  - `sign_language_mobilenetv2.h5`
  - `updated_asl_sign_language_model_Resnet.h5`
- ✅ Provided `.py` testing scripts and `.h5` image data
- ✅ Deployed on **Streamlit frontend**

  # Streamlit UI
  
  ![image](https://github.com/user-attachments/assets/0d7219c5-2ba8-4793-8e53-0934ce0f5d49)

> 💻 To Run the App:
```bash
streamlit run "D:/ML PROJECTS/AI Sign Language Translator/signlanguageapp.py"
🖥️ Frontend Features – Streamlit UI
🎛 Model Selector:

Choose between ResNet / MobileNet / Updated ResNet

📷 Upload image for instant translation

🎞 Upload video for dynamic sign detection

🧠 Learning Mode → Letter correctness check

🔤 Word creation by multiple image input

🎨 Clean design with logo + responsive layout

📸 Visualization – Web UI Preview
(Insert Screenshot of App UI)

📂 File Structure
mathematica
Copy
Edit
📁 AI Sign Language Translator/
├── signlanguageapp.py
├── asl_images.h5
├── asl_sign_language_model_Resnet.h5
├── sign_language_mobilenetv2.h5
├── updated_asl_sign_language_model_Resnet.h5
├── label_encoder.pkl
🙌 Acknowledgements
Datasets from Kaggle and Mendeley

Built using TensorFlow, Keras, OpenCV, MoviePy, and Streamlit

Developed by Yuvan

🌱 Future Scope
🖥️ Real-time webcam integration

🔄 Auto-updating models with feedback

🧩 Expand to sentence-level translation

📡 Deploy as Flask/FastAPI REST API
