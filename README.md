# Fitbit Fitness Tracker Data Analysis (Bellabeat Case Study)

This repository contains an Exploratory Data Analysis (EDA) project analyzing smart device fitness tracker data to gain insights into user behavior and inform marketing strategies for **Bellabeat**, a high-tech manufacturer of health-focused smart products for women.

The analysis is performed using Python in a Jupyter Notebook.

---

## 📌 Project Overview & Business Task

**Bellabeat** wants to analyze smart device usage data to understand how consumers use their smart devices. Using these insights, the goal is to provide high-level recommendations that can guide the company's marketing strategy and unlock new growth opportunities.

### **Business Task**
> Identify patterns and trends in user activity, sleep, and physical measurements. Translate these insights into recommendations for Bellabeat's marketing strategy and product features.

---

## 🛠️ Technologies Used

- **Language:** Python 3
- **Libraries:**
  - `pandas` for data loading, cleaning, merging, and manipulation.
  - `numpy` for mathematical operations.
  - `matplotlib` and `seaborn` for data visualization.
- **Environment:** Jupyter Notebook

---

## 📊 Dataset Description

The analysis uses the public dataset **Fitbit Tracker Data** (distributed by [Fitabase](https://fitabase.com/)), which tracking data from 30+ Fitbit users. The data covers a two-month period (March 12, 2016 – May 12, 2016) and contains:
- **Daily Activity:** Total steps, distance, active minutes, and calories.
- **Hourly Calories & Intensities:** Tracking hourly activity levels and energy expenditure.
- **Sleep Log:** Daily sleep duration and time in bed (available for April 12 – May 12).
- **Weight Log:** Weight measurements and BMI (available for 13 users).

---

## 🔄 Project Workflow (Data Pipeline)

### **1. Data Preparation & Merging**
- Appended two separate monthly cycles of Fitbit export data to construct a continuous dataset.
- Standardized file paths and columns (e.g., date formats, column names).

### **2. Data Cleaning & Normalization**
- Converted date/time columns into correct `datetime` formats.
- Handled duplicate records (specifically, aggregated duplicate entries for the same user on the same date by summing values).
- Filtered out insufficient datasets (e.g., the Weight dataset only had 13 users, which was deemed statistically insignificant for broader conclusions).

### **3. Exploratory Data Analysis (EDA)**
- Calculated descriptive statistics for steps, sedentary minutes, active time, and sleep.
- Explored relationships such as:
  - Sleep duration vs. Bedtime duration.
  - Sleep duration vs. Sedentary time.
  - Activity intensity vs. Calories burned.
  - Hourly distribution of activity throughout the day.

---

## 💡 Key Findings

- **Daily Steps Deficit:** The average daily steps per user is **7,408**, which falls short of the CDC-recommended **10,000 steps** for healthy adults.
- **Excessive Sedentary Time:** On average, users spend **1,010 minutes (approx. 17 hours)** per day being sedentary, accounting for over **75%** of their day.
- **Sleep and Bedtime Correlation:** Time asleep has a very strong positive correlation with time spent in bed. Users can potentially improve sleep quality by setting consistent bedtime schedules.
- **Sedentary vs. Sleep:** A negative correlation was observed between sedentary minutes and total sleep time.
- **Peak Activity Hours:** User activity levels (intensities and calorie burn) peak between **5:00 PM and 7:00 PM**, suggesting workouts typically occur post-work hours.

---

## 🚀 Marketing & Product Recommendations

### **Target Audience**
* **Office Workers / Working Professionals:** Focus on individuals with highly sedentary routines who want to build healthier habits.

### **Suggested Features & Notification Strategies**
1. **Sedentary Alerts:** Gentle reminders on the Bellabeat app to stand up, stretch, or walk if a user has been inactive for a prolonged period.
2. **Bedtime Reminders:** Automatic notifications helping users Wind Down and get into bed at a consistent time to improve overall sleep duration and quality.
3. **Post-Work Workout Prompts:** Send motivational prompts around **4:30 PM - 5:00 PM** to encourage physical activity, matching the naturally observed peak workout window.
4. **Step-Count Challenges:** Create milestones to guide users from their baseline average (~7k steps) towards the healthy threshold of 10k steps.

---

## 📂 Project Structure

```bash
├── Data/                             # Fitbit dataset directories
│   ├── mturkfitbit_export_3.12.16-4.11.16/
│   └── mturkfitbit_export_4.12.16-5.12.16/
├── Result_final.ipynb                # Main Jupyter Notebook
└── README.md                         # Project documentation
```

---

## ⚙️ How to Run

1. Clone this repository:
   ```bash
   git clone <repository_url>
   ```
2. Place the dataset folders into the `Data/` directory.
3. Install the required Python packages:
   ```bash
   pip install pandas numpy matplotlib seaborn jupyter
   ```
4. Launch the Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
5. Open `Result_final.ipynb` and run the cells.
