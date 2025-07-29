## 🚴 Cyclistic Bike-Share Case Study – Data Analysis with R

## 📝 Project Overview
This project is the first case study in the **Google Data Analytics Professional Certificate**.
The goal is to analyze historical bike trip data from Cyclistic, a fictional bike-share company in Chicago, to understand user behavior and inform a new marketing strategy. [cite_start]The primary objective is to convert casual riders into annual members, as they are more profitable. [cite: 9, 11, 32-34]

---

## 🎯 Objective
- [cite_start]Analyze how annual members and casual riders use Cyclistic bikes differently. [cite: 11, 41, 44-45]
- [cite_start]Identify trends and relationships in their usage patterns. [cite: 137]
- [cite_start]Provide data-backed insights and recommendations to convert casual riders into annual members. [cite: 12, 13]
- [cite_start]Visualize findings through compelling and professional data plots. [cite: 13, 51, 173-174]

---

## 🛠 Tools & Technologies
- **Language:** R
- **Environment:** RStudio
- **Libraries:** `tidyverse`, `lubridate`, `conflicted`
- **Visualization Output:** Bar Charts
- **Data Format:** CSV

---

## 📁 Dataset
- [cite_start]**Source:** Divvy 2019 Q1 and Divvy 2020 Q1 trip data (made available by Motivate International Inc. under public license). [cite: 66, 68]
    * [cite_start]*(Note: "Cyclistic" is a fictional company, so "Divvy" data is used as a proxy).* [cite: 68]
- Data includes:
  - `Divvy_Trips_2019_Q1.csv`
  - `Divvy_Trips_2020_Q1.csv`
- [cite_start]Data covers historical bike trip information, including ride IDs, bike types, start/end times, station names/IDs, and user type (member/casual). [cite: 64]
- [cite_start]Personally identifiable information is excluded due to data privacy issues. [cite: 69]

---

## 🔍 Process (Ask, Prepare, Process, Analyze, Share, Act)

### 1. **Ask**
- [cite_start]The guiding question for this analysis is: How do annual members and casual riders use Cyclistic bikes differently? [cite: 41, 44-45]
- [cite_start]The insights will drive business decisions on converting casual riders to members. [cite: 57]

### 2. **Prepare**
- [cite_start]Downloaded Q1 2019 and Q1 2020 trip data. [cite: 65, 106]
- [cite_start]Stored data appropriately and identified its organization. [cite: 84-85]
- [cite_start]Verified data integrity and considered licensing/privacy. [cite: 78-79]

### 3. **Process**
- Loaded data into RStudio using `read_csv()`.
- [cite_start]Renamed columns in `Divvy_Trips_2019_Q1.csv` to match `Divvy_Trips_2020_Q1.csv` for consistency. [cite: 142]
- Converted `ride_id` and `rideable_type` columns to character type in 2019 data.
- Combined Q1 2019 and Q1 2020 dataframes into a single `all_trips` dataframe using `bind_rows()`.
- Removed irrelevant columns (e.g., `start_lat`, `end_lng`, `birthyear`, `gender`, `tripduration`).
- Recoded `usertype` values ("Subscriber" to "member", "Customer" to "casual") for consistency.
- [cite_start]Calculated `ride_length` (in seconds) by subtracting `started_at` from `ended_at`. [cite: 117-118]
- [cite_start]Extracted `date`, `month`, `day`, `year`, and `day_of_week` from `started_at`. [cite: 119-120]
- [cite_start]Cleaned data by removing negative `ride_length` values and rides starting at "HQ QR" station. [cite: 100]

### 4. **Analyze**
- [cite_start]Conducted descriptive analysis on `ride_length` (mean, median, max, min). [cite: 144, 146-148]
- [cite_start]Compared average, median, max, and min ride lengths between members and casual riders. [cite: 150]
- [cite_start]Aggregated data to find the average ride time by day of the week for both user types. [cite: 151-152]
- Ordered the `day_of_week` column chronologically for better analysis.
- Summarized the number of rides and average duration by member type and weekday.

### 5. **Share**
- Visualized findings using `ggplot2`.
- Created bar charts to illustrate:
    - Total number of rides by day of the week for members vs. casual riders.
    - Average ride duration by day of the week for members vs. casual riders.
- Included all charts in this repository.

---

## 📈 Key Findings
- **Casual riders have significantly longer average ride durations** compared to annual members across all days of the week. This suggests casual riders might use bikes for leisure or longer single trips.
- **Casual rider activity is notably higher on weekends** in terms of both ride length and number of rides, indicating recreational usage.
- **Annual members demonstrate more consistent daily usage**, with a higher overall number of rides throughout the week, particularly on weekdays, suggesting commuter or routine use.
- Both user types show a higher volume of rides during weekdays, but casual riders' average ride length on weekends often surpasses their weekday ride length.

---

## 💡 Recommendations

1.  **Introduce Weekend Pass Conversion Offers:** Target casual riders taking long weekend rides with special discounts or incentives to upgrade to an annual membership, highlighting the cost savings for their typical ride patterns.
2.  **Promote Membership for Extended Rides:** Create marketing materials that clearly demonstrate how an annual membership provides better value for longer, leisure-oriented rides, using examples of typical casual rider trip durations.
3.  **Develop "Weekday Commuter" Benefits:** While casual riders are prominent on weekends, appeal to those who might occasionally commute by bike by showcasing how membership streamlines weekday travel, with benefits like unlimited rides and quicker access.
4.  **Leverage Visual Marketing with Testimonials:** Use compelling visuals and testimonials on digital media (e.g., social media, email campaigns) featuring casual riders who converted to members and are now enjoying the benefits, particularly focusing on weekend adventurers and occasional commuters.

---

## 👨‍💻 Author

**[rishi nandan]**
🎓 [bba] | 📊 [Aspiration for data anlyst]
📌 Tools: R | SQL | Excel | Tableau
🌐 GitHub: [https://github.com/rishinandan3125]
📫 Email: [nandanrishi27@gmail.com]
🔗 LinkedIn: [https://www.linkedin.com/in/rishi-nandan-612874256/]

---
