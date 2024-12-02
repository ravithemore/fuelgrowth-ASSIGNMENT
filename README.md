# 🎥 AI Backend Internship Assignment 🚀

This project analyzes **influencer performance data** by extracting and processing video content. It automates video downloading, face detection, performance analysis, and report generation, delivering an organized summary of influencer metrics. 📊

---

## 🌟 **Features**
- 🎭 **Extracts facial images** from videos.
- 📈 **Analyzes influencer performance metrics** for average performance and reliability.
- 📝 **Generates professional PDF reports** with influencer metrics and images.

  

---
# 🔄 Workflow Stages

## 1️⃣ Extraction Phase
**Purpose:** Downloads videos from the provided dataset.  
- **Input:** CSV file (`Assignment Data - Sheet1.csv`) with video URLs.  
- **Process:**  
  - Downloads videos into the `videos` folder, with filenames matching their row indices (e.g., `0.mp4`, `1.mp4`).  
- **Output:** `videos` folder containing the downloaded videos.  

---

## 2️⃣ Processing Phase
**Purpose:** Identifies unique influencers and calculates metrics.  
- **Input:** Downloaded videos from the `videos` folder.  
- **Process:**  
  - Detects faces using `face_recognition`.  
  - Saves unique faces in the `influencer_faces` folder.  
  - Calculates:  
    - **Average Performance:** Computed from dataset scores.  
    - **Reliability:** Measured using test-retest reliability.  
- **Output:**  
  - `influencer_faces` folder with unique face images.  
  - CSV file (`sorted_unique_influencers_with_reliability.csv`) summarizing influencer metrics.  

---

## 3️⃣ Analysis Phase
**Purpose:** Creates a professional PDF summarizing the analysis.  
- **Input:**  
  - `sorted_unique_influencers_with_reliability.csv`.  
  - Face images from the `influencer_faces` folder.  
- **Output:**  
  - 📄 PDF file (`influencer_table.pdf`) containing:  
    - Influencer ID.  
    - Influencer Face (if available).  
    - Average Performance.  
    - Reliability.  

---

# 📂 File Descriptions

## 🗂 Input Files
- **CSV File:** `Assignment Data - Sheet1.csv`  
  Contains influencer video URLs and performance data.  

## 🗂 Output Files
- **CSV File:** `sorted_unique_influencers_with_reliability.csv`  
  Summarizes:  
  - Influencer ID.  
  - Average Performance.  
  - Reliability.  
  - First Video URL.  
- **PDF File:** `influencer_table.pdf`  
  A user-friendly report displaying influencer metrics in table format with images.  

- **Folder:** `influencer_faces`  
  Stores unique face images extracted from videos.  

---

# 🌟 Project Highlights

- 🤖 **Automation:** Simplifies downloading and processing video data, reducing manual effort.  
- 🧑‍🦰 **Face Recognition:** Ensures unique identification of influencers, avoiding duplicates.  
- 📊 **Reliability Metrics:** Measures consistency in influencer performance with test-retest reliability.  
- 💼 **User-Friendly Reporting:** Provides an organized, visually appealing PDF report.  

---

# 🤔 Assumptions
- Videos without visible faces are excluded from processing.  
- Influencers are uniquely identified based on face encoding.  
- Reliability is calculated only for influencers with multiple scores.  

---

# 💻 Technologies Used
- **Programming Languages:** Python  
- **Libraries:**  
  - `pandas`  
  - `opencv-python`  
  - `face_recognition`  
  - `requests`  
  - `reportlab`  

---

# 🙌 Contributing
Contributions are welcome! Create a pull request or open an issue for feedback.  

---

# 📧 Contact
For any queries, reach out to:  
📩 **Email:** damorravi540@gmail.com 

## ⚙️ **Setup Instructions**
**Clone the repository**:  
   ```bash
   git clone <repository-url>
   cd <repository-name>
# Install dependencies
pip install pandas opencv-python face_recognition requests reportlab

# Run the scripts in order
# Step 1: Download videos
jupyter nbconvert --to notebook --execute Extraction.ipynb

# Step 2: Process data to detect faces and compute metrics
jupyter nbconvert --to notebook --execute Process.ipynb

# Step 3: Generate a summary report in PDF format
jupyter nbconvert --to notebook --execute Analyze.ipynb ```.




