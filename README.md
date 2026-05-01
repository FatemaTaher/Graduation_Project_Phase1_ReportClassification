# Graduation_Project_Phase1_ReportClassification
🇪🇬 Egyptian Citizen Reports - Synthetic Data Generator
Python
License

This repository contains a Python script to generate high-quality synthetic datasets simulating citizen utility reports in Egypt. It is designed for Data Scientists and NLP engineers to train, test, and validate machine learning models (e.g., text classification, urgency detection, and fake report filtering).

📌 Overview
The script generate_data.py creates a CSV file (synthetic_reports_egypt.csv) containing 15,000+ records. Each record represents a citizen report regarding issues such as electricity outages, water leaks, garbage accumulation, and more.

The data includes realistic features:

Geographic Data: Real Egyptian governorates and cities with simulated GPS coordinates.
Textual Data: Auto-generated headlines and details using dynamic templates.
Labels: Multi-class labels indicating the nature of the report (True, False, Emergency, Repeated, etc.).
Noise: Informal phrases and contradictions to simulate real-world human behavior.
✨ Key Features
Realistic Geography: Covers 14 major governorates (Cairo, Alexandria, Giza, etc.) with specific districts.
Smart Text Generation:
Uses templates for different utility sectors (Electricity, Water, Gas, Road, Telecom).
Injects "human noise" (informal complaints, rumors).
Handles specific edge cases (Out-of-scope topics, Unclear/Garbled text).
ML-Ready Labels:
True: Legitimate complaints.
False: Rumors or second-hand information.
Emergency: Life-threatening situations (Fire, Explosion).
Repeated: Follow-up complaints.
Out_of_scope: Irrelevant topics (Traffic, Lost pets).
Unclear: Gibberish or very short texts.
Geospatial Support: Generates Latitude and Longitude coordinates clustered around governorate centers.
📊 Dataset Schema
The generated synthetic_reports_egypt.csv includes the following columns:

Column
Type
Description
report_date	Date	Random date within the last year.
governorate	String	The Egyptian governorate (e.g., "Cairo").
city	String	The specific district or city.
latitude	Float	Simulated GPS latitude.
longitude	Float	Simulated GPS longitude.
issue_type	String	Category of issue (e.g., "electricity", "water").
report_headline	String	Summary of the issue.
report_detail	String	Full description of the report.
text_length	Integer	Character count of the report.
report_category	String	"citizen" or "business".
report_truth	String	Target Label (True, False, Emergency, etc.).

🚀 Getting Started
Prerequisites
You need Python installed on your machine. You also need to install the following libraries:

bash

pip install pandas numpy
Usage
Clone the repository:
bash

git clone https://github.com/your-username/egyptian-reports-generator.git
cd egyptian-reports-generator
Run the script:
bash

python generate_data.py
Output:
Upon completion, a file named synthetic_reports_egypt.csv will be created in the root directory containing the generated data.
📝 Sample Output
Here is a preview of what the generated data looks like:

report_truth
governorate
issue_type
report_headline
report_detail
Emergency	Cairo	gas_issue	!!! URGENT !!! - Gas Leak	A very strong smell of gas detected at Building 12. Immediate danger — residents are evacuating. Please help quickly!
False	Alexandria	waste_garbage	Garbage Pile	I think there might be Trash has not been collected from Street 45 for a week. though everything looks fine from outside.
Repeated	Giza	electricity	[Follow-up] Power Outage	I reported this before but it was not fixed: The electricity has been out at Building 5 for hours.
Out_of_scope	Luxor	telecom	Traffic Accident Report	A car accident occurred at Street 88, need police assistance.

🎯 Use Cases
Text Classification: Train models to detect whether a report is an Emergency or not.
Spam Detection: Identify False or Rumored reports.
Sentiment Analysis: Analyze the tone of citizen complaints.
Dashboard Prototyping: Populate analytics dashboards for municipal management systems.
⚠️ Disclaimer
This data is synthetic and randomly generated. Any resemblance to actual persons, locations, or events is purely coincidental. Do not use this data for making real-world decisions.

📄 L
