# DEHAZEproj
CNN-based deep learning model for single image dehazing with real and synthetic datasets.

#Image Dehazing using CNN

This project provides a full-stack solution for single image dehazing using a deep learning-based CNN model. It features a responsive frontend interface, a Flask backend for image upload and enhancement, and integration with a trained CNN model for haze removal.

🛠️ Features
🔍 Single Image Dehazing using a trained CNN

🌐 Frontend Interface built with HTML, TailwindCSS & JavaScript

⚙️ Flask Backend with image upload and processing endpoints

🧠 Model Integration using PyTorch/TensorFlow (pluggable)

💾 Image metadata storage via SQLite + SQLAlchemy

💡 Real-time image enhancement: Dehaze, Contrast, Sharpen

📥 Download enhanced results with a single click

🧠 How It Works
1. Frontend
Users upload up to 4 images via a user-friendly interface.

Choose from Dehaze, Contrast, or Sharpen enhancements.

Displays original and processed images side-by-side.

Offers a download button for enhanced images.

2. Backend
Flask API accepts image uploads via /upload.

Uploaded images are saved to uploads/ folder.

Images are optionally processed by the CNN model.

Processed images are saved to processed/ folder and served via /processed/<filename> route.

3. CNN Model
Trained on the RESIDE dataset or custom synthetic datasets.

Input: Hazy image → Output: Clean/dehazed image

Integrated into the Flask backend with a simple inference function.


🚀 Getting Started

🔧 Prerequisites
Python 3.8+

pip

Node.js (optional for frontend build tools)

📦 Install Dependencies

bash
Copy
Edit
pip install -r requirements.txt

🗂️ Project Structure

csharp
Copy
Edit
project-root/
│
├── app.py                   # Flask backend
├── templates/
│   └── index.html           # Frontend HTML
├── uploads/                 # Uploaded images
├── processed/               # Enhanced images
├── static/                  # CSS, JS (optional)
├── your_model_module.py     # CNN model script
├── samples/                 # Sample input/output
├── requirements.txt
└── README.md

⚙️ Running the App

bash
Copy
Edit
# Start Flask server
python app.py
Then open your browser and navigate to:
http://127.0.0.1:5000/

🧪 Model Details

Model Type: Convolutional Neural Network (CNN)

Architecture: Encoder-Decoder or U-Net based

Input: RGB hazy image

Output: RGB dehazed image

Framework: PyTorch or TensorFlow (configurable)

Evaluation Metrics: PSNR, SSIM

📄 API Endpoints

Method	Route	Description
GET	/	Loads the main upload page
POST	/upload	Uploads and processes an image
GET	/processed/<filename>	Returns enhanced image

📚 Dataset

RESIDE Dataset: RESIDE GitHub

Optionally use synthetic data generated with the Atmospheric Scattering Model.

📥 Example Usage (via cURL or JS)

bash
Copy
Edit
curl -F "fileInput=@hazy.jpg" http://localhost:5000/upload

🎯 Future Improvements

Integrate real-time CNN inference on GPU/Cloud

Add image preview gallery

Implement authentication for multi-user usage

Add support for video dehazing


📝 License

This project is licensed under the MIT License.

🙋‍♂️ Contact

For questions or collaborations, feel free to open an issue or pull request.
