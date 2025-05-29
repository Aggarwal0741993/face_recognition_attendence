Face Recognition Attendance System 🎯

A face recognition–based attendance system built using [InsightFace](https://github.com/deepinsight/insightface) and ONNXRuntime in Python. This project encodes known faces and matches them in real time to mark attendance.

---

## 🔍 Overview

This system allows you to:

- Upload a dataset of registered users (face images)
- Extract and store face embeddings using `InsightFace`
- Compare incoming faces to known embeddings
- Mark attendance based on successful recognition

---

## 🧰 Technologies Used

- Python 3
- InsightFace (`buffalo_l` model)
- ONNXRuntime
- NumPy
- Pillow (PIL)
- zipfile, pickle
- Google Colab (for running the notebook)

---

## 📁 Folder Structure

FACES_PROJECT_ML/ ├── Alice/ │   ├── image1.jpg │   ├── image2.jpg ├── Bob/ │   ├── image1.png │   ├── image2.jpg

Each subfolder is named after a person and contains their face images.

---

## 📦 Files Generated

- `known_faces.pkl`: Stores face embeddings and corresponding names.

---

## 🚀 How to Run

1. Upload your ZIP file (e.g., `FACES_PROJECT_ML.zip`) to Colab.
2. The notebook:
   - Extracts the ZIP
   - Processes images from each person’s folder
   - Uses InsightFace to extract embeddings
   - Saves all embeddings to `known_faces.pkl`
3. Use these embeddings later for face recognition (live or from static input).

---

## 🧠 Sample Code Flow

```python
from insightface.app import FaceAnalysis

app = FaceAnalysis(name='buffalo_l')
app.prepare(ctx_id=0)

# Loop over face folders
# Extract and save embeddings to known_faces.pkl


---

✅ TODO (Future Enhancements)

Real-time webcam attendance marking

CSV or Excel attendance logs

Add GUI using Tkinter or PyQt

Notification system (e.g., SMS or email on entry)



---

📄 License

This project is released under the MIT License.


---

🙏 Acknowledgements

InsightFace for amazing face recognition models

Google Colab for free compute
