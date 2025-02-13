### **Network Security Project for Phishing Data**  

#### **Project Purpose**  
This is a **Data Science project** focused on detecting phishing attacks using machine learning. The system processes data, trains a model, and deploys it as an API for real-time predictions.  

---

### **Project Structure:**  
🔹 **Get Data** → Data is retrieved from **MongoDB** and processed.  
🔹 **Check Data** → The system **validates** if the data is correct.  
🔹 **Transform Data** → Data is **cleaned and prepared** for training.  
🔹 **Train Model** → A **machine learning model** is trained.  
🔹 **Evaluate Model** → The model is tested for performance.  
🔹 **Deploy Model** → If the model meets accuracy requirements.  

---

### **Data Ingestion:**  
✅ **Get Data from MongoDB** → Fetches data from a **MongoDB** database.  
✅ **Store Data in Feature Store** → Saves raw data in **CSV format**.  
✅ **Drop Unnecessary Columns** → Removes **unimportant** columns.  
✅ **Split Data into Train & Test** → Divides cleaned data into **train.csv** and **test.csv**.  

---

### **Data Validation:**  
1️⃣ **Configuration & Setup**  
   - Defines paths for **valid/invalid data**, **train/test files**, and **drift report**.  

2️⃣ **Data Validation Checks**  
   - Reads **train.csv** and **test.csv**.  
   - Verifies **column count** and **data types**.  
   - Updates status if **missing columns** are found.  

3️⃣ **Data Drift Detection**  
   - Ensures **schema correctness** (10 features).  
   - Compares **train vs. test distributions** wuth ks test.  
   - Generates a **Drift Report** if differences are significant.  

4️⃣ **Validation Report Output**  
   - Saves results in **report.yaml**, including:  
     ✅ Validation status  
     ✅ File paths for valid/invalid data  
     ✅ Data drift summary  

---

### **Data Transformation:**  
✅ Handles **missing values** using **Simple Imputer & KNN Imputer**.  
✅ **Removes duplicates** from the dataset.  
✅ **Feature scaling is already applied**.  
✅ The **data is balanced** before training.  
✅ **Saves transformed data** for further model training.  

---

### **Model Training & Evaluation:**  
✅ Loads **transformed NumPy data** for training.  
✅ Trains and evaluates **multiple models** to find the best one.  
✅ Compares model performance against a **predefined accuracy threshold**.  
✅ Saves the **best model as `model.pkl`** for deployment.  

---

### **Deployment with FastAPI & Docker:**  
✅ **FastAPI Integration** → A REST API is built using **FastAPI**, where users can upload a file for prediction.  
✅ **Docker Deployment** → The model is containerized using **Docker**, making it portable and easy to deploy.  
✅ **CI/CD Pipeline with GitHub Actions** →  
   - **Automates testing & deployment** of the API.  
   - Ensures seamless updates & version control.  

---

### **Experiment Tracking with MLflow on DagsHub**  
📌 You can **track model performance, experiments, and logs** using **MLflow on DagsHub** at this link:  
🔗 [**Click here to view MLflow tracking**]([(https://dagshub.com/Nasr201/Network-Security-Project-For-Phising-Data]) 

---

### **Final Outcome:**  
A **real-time phishing detection system** that takes input data, predicts phishing attacks, and deploys the model using **FastAPI, Docker, and CI/CD**, while tracking experiments with **MLflow on DagsHub**. 🚀
