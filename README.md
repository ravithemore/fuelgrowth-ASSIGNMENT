**AI Backend Internship Assignment**

Project Overview:
This project is designed to analyze influencer performance data by extracting and processing video content. It combines automated video downloading, 
face detection, performance analysis, and PDF reporting to deliver a comprehensive summary of influencer metrics. 
The goal is to identify unique influencers, calculate their average performance and reliability, 
and present the results in an organized format for easy interpretation.

Features:
Extracts facial images from videos
Analyzes influencer performance metrics
Generates reports with metrics and images

Setup Instructions:

Access the dataset.
Install required dependencies ,"pip install pandas opencv-python face_recognition requests reportlab".
Run the scripts in the following order:  Extraction.ipynb, Process.ipynb and Analyze.ipynb.

Workflow Stages:
1. Extraction Phase
Purpose: To download videos listed in the provided dataset.
Process:
A CSV file (Assignment Data - Sheet1.csv) containing video URLs is loaded.
Videos are downloaded using their URLs and saved locally in the videos folder, with filenames corresponding to their dataset row indices (e.g., 0.mp4, 1.mp4).
Output:
A videos folder containing all downloaded video files.

2. Processing Phase
Purpose: To identify unique influencers and calculate performance metrics.
Process:
Each video is analyzed to detect faces using face recognition technology.
Unique faces are identified and saved in the influencer_faces folder.
Average performance and reliability metrics are calculated for each influencer:
Average Performance: Computed from the performance scores in the dataset.
Reliability: Measured using test-retest reliability from multiple video scores.
A summary CSV file, sorted_unique_influencers_with_reliability.csv, is generated.
Output:
influencer_faces folder: Contains unique face images of influencers.
sorted_unique_influencers_with_reliability.csv: Summarized influencer metrics.

3. Analysis Phase
Purpose: To create a professional report summarizing the influencer analysis.
Process:
The sorted_unique_influencers_with_reliability.csv file and face images from the influencer_faces folder are used.
A PDF (influencer_table.pdf) is generated with a table showing:
Influencer ID
Influencer Face (if available)
Average Performance
Reliability
Output:
influencer_table.pdf: A visually appealing report summarizing influencer data.

File Descriptions:
1. Input Files
CSV File: Assignment Data - Sheet1.csv
Contains influencer video URLs and performance data.

2. Output Files
CSV File: sorted_unique_influencers_with_reliability.csv
Summarizes influencer metrics, including:
_Influencer ID
Average Performance
Reliability
First Video URL_
PDF File: influencer_table.pdf , Displays influencer data in a table format with images.

Folder: influencer_faces, Stores unique face images extracted from the videos.

Project Highlights:

Automation: Automates downloading and processing of video data, reducing manual effort.

Face Recognition: Utilizes face recognition to identify unique influencers, ensuring no duplicate faces are included.

Reliability Metrics: Calculates test-retest reliability to measure consistency in influencer performance.

User-Friendly Reporting: Generates a PDF summarizing data in an easily understandable format

Assumptions:
Videos without visible faces are not processed or included in the final output.
Each influencer is uniquely identified based on their face encoding.
Test-retest reliability is only calculated for influencers with multiple performance scores.
