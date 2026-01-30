# 🥗 NutriSense

> **Smart Food Analysis & Personalized Health Insights**

![Project Status](https://img.shields.io/badge/status-active-success.svg)
![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Frontend](https://img.shields.io/badge/frontend-React%20%7C%20Vite%20%7C%20Tailwind-blueviolet)
![Backend](https://img.shields.io/badge/backend-FastAPI%20%7C%20Python-green)

NutriSense is an advanced full-stack application designed to empower users with instant, detailed nutritional analysis of food products. By leveraging barcode scanning, OCR (Optical Character Recognition), and personalized health profiling, NutriSense goes beyond simple calorie counting to provide actionable health warnings and suitability checks based on individual medical conditions and allergies.

---

## 🚀 Key Features

### 🔍 **Smart Product Analysis**
- **Barcode Scanning**: Instantly retrieve product details using the OpenFoodFacts database.
- **OCR Fallback**: Intelligent text recognition to extract ingredients and nutritional info when barcodes fail or are missing.
- **Visual Health Score**: content-rich visual indicators (Nutri-Score, NOVA group) to assess food quality at a glance.

### 🩺 **Personalized Health Engine**
- **Medical Condition Checks**: Automatically warns users if a product conflicts with conditions like *Diabetes, Hypertension, or Heart Disease*.
- **Allergen Detection**: Scans ingredients for user-specified allergens (e.g., *Gluten, Dairy, Peanuts*) and provides immediate "DO NOT CONSUME" warnings.
- **Hidden Ingredient Detection**: Identifies hidden sugars, harmful additives, and ultra-processed ingredients that aren't immediately obvious.

### 📱 **Modern User Experience**
- **Mobile-First Design**: Optimized for on-the-go usage in grocery stores.
- **History & Favorites**: Keep track of scanned items for quick reference.
- **Secure Authentication**: User profiles and data syncing via Supabase.

---

## 🛠️ Technology Stack

### **Frontend**
- **Framework**: [React](https://reactjs.org/) + [Vite](https://vitejs.dev/)
- **Language**: TypeScript
- **Styling**: [Tailwind CSS](https://tailwindcss.com/)
- **UI Components**: [shadcn/ui](https://ui.shadcn.com/)
- **State Management**: React Query

### **Backend**
- **Framework**: [FastAPI](https://fastapi.tiangolo.com/) (Python)
- **OCR Engine**: [Tesseract-OCR](https://github.com/tesseract-ocr/tesseract) & `pytesseract`
- **Product Database**: [Open Food Facts API](https://world.openfoodfacts.org/)
- **Data Model**: Pydantic

### **Infrastructure & Auth**
- **Database**: [Supabase](https://supabase.com/) (PostgreSQL)
- **Authentication**: Supabase Auth

---

## 🏁 Getting Started

Follow these instructions to set up the project locally.

### Prerequisites
- **Node.js** (v18+)
- **Python** (v3.9+)
- **Tesseract-OCR** installed on your system ([Installation Guide](https://github.com/tesseract-ocr/tessdoc/blob/main/Installation.md))

### 1. Clone the Repository
```bash
git clone https://github.com/DevBolt07/nutri_sense.git
cd nutri_sense
```

### 2. Frontend Setup
Install the Node.js dependencies:
```bash
npm install
```

### 3. Backend Setup
Set up the Python environment:

**Windows:**
```powershell
# Create virtual environment
python -m venv backend/venv

# Activate virtual environment
.\backend\venv\Scripts\activate

# Install dependencies
pip install -r backend/requirements.txt
```

**Mac/Linux:**
```bash
python3 -m venv backend/venv
source backend/venv/bin/activate
pip install -r backend/requirements.txt
```

### 4. Configuration
Create a `.env` file in the `backend/` directory (or rely on the root `.env` for the frontend to pass to Supabase).

**Backend `.env`:**
```env
SUPABASE_URL=your_supabase_url
SUPABASE_ANON_KEY=your_supabase_key
```

### 5. Running the Application
We have configured a concurrent runner to start both the frontend and backend with a single command:

```bash
npm run dev:all
```

- **Frontend**: http://localhost:8080
- **Backend**: http://localhost:8000
- **API Docs**: http://localhost:8000/docs

---

## 📸 Screenshots

*(Add screenshots of the Dashboard, Scanner, and Product Result pages here)*

---

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).
