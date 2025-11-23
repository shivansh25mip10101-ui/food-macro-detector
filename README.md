# food-macro-detector
AI-powered food macro estimation system using image classification + USDA FDC dataset.
🍽️ Food Macro Detector
Estimate Protein, Fat & Carbohydrates using Machine Learning + USDA FoodData Central

This project recognizes food items (via image classification) and retrieves macronutrient values from the USDA FoodData Central dataset. It is designed as a complete academic project following the “Build Your Own Project” guidelines.

📌 Features

✔ Local SQLite database with FDC bulk data

✔ Automated macronutrient extraction per 100g

✔ MobileNetV2 image classifier (transfer learning)

✔ Fuzzy label-to-FDC mapping

✔ Serving-size based macro calculation

✔ Flask API endpoint: /api/analyze

✔ Full PDF report included

📁 Project Structure
food_macro_project/
│
├── load_fdc.py
├── extract_macros.py
├── auto_map_labels.py
├── load_mappings.py
├── fdc_client_local.py
├── train.py
├── inference_example.py
├── app.py
│
├── requirements.txt
├── README.md
├── statement.md
└── project_report.pdf

🔧 Installation
python -m venv venv
source venv/bin/activate    # Windows: venv\Scripts\activate
pip install -r requirements.txt

🗄 Load USDA FoodData Central

Place bulk JSON files into data/ then run:

python load_fdc.py
python extract_macros.py
python auto_map_labels.py
python load_mappings.py

🤖 Train the Image Classifier

Arrange dataset like:

dataset/
  train/
    pizza/
    rice/
    ...
  val/
    pizza/
    rice/


Train:

python train.py --data_dir dataset --img_size 160 --batch 8 --epochs 12

🔍 Run Inference
python inference_example.py

🌐 Run Flask API
python app.py

📄 Report

Full academic project report (PDF) included:

✔ Abstract
✔ Architecture
✔ Dataset
✔ Methodology
✔ Algorithms Used
✔ UML-like descriptions
✔ Results & Challenges
✔ Future Scope
