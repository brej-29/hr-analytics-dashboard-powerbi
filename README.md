<div align="center">
  <h1>📊 HR Analytics Dashboard – Power BI</h1>
  <p><i>Interactive HR insights on headcount, diversity, age, salary, and leave built in Microsoft Power BI Desktop</i></p>
</div>

<br>

<div align="center">
  <a href="https://github.com/YOUR_GITHUB_USERNAME/hr-analytics-dashboard-powerbi">
    <img alt="Last Commit" src="https://img.shields.io/github/last-commit/brej-29/hr-analytics-dashboard-powerbi">
  </a>
  <img alt="Tool" src="https://img.shields.io/badge/Tool-Power%20BI-0066ff">
  <img alt="Language" src="https://img.shields.io/badge/Language-DAX%20%7C%20Power%20Query-yellow">
  <img alt="Data Source" src="https://img.shields.io/badge/Data-Excel%20HR%20Dataset-brightgreen">
  <img alt="License" src="https://img.shields.io/badge/License-MIT-black">
</div>

<div align="center">
  <br>
  <b>Built with the tools and technologies:</b>
  <br><br>
  <code>Microsoft Power BI Desktop</code> |
  <code>DAX</code> |
  <code>Power Query</code> |
  <code>Excel</code>
</div>

---

## **Screenshot**

<!-- Replace with your own screenshot URL (inside the repo or an uploaded asset) -->
<img width="1919" height="928" alt="HR Analytics Dashboard in Power BI" src="https://raw.githubusercontent.com/brej-29/hr-analytics-dashboard-powerbi/main/screenshots/hr-dashboard-main.png" />

---

## **Table of Contents**
* [Overview](#overview)
* [Features](#features)
* [Getting Started](#getting-started)
    * [Project Structure](#project-structure)
    * [Prerequisites](#prerequisites)
    * [Installation](#installation)
    * [Configuration](#configuration)
    * [Usage](#usage)
* [License](#license)
* [Contact](#contact)

---

## **Overview**

**HR Analytics Dashboard – Power BI** is an end-to-end data analytics project that transforms a raw HR dataset into a clean, interactive Power BI report.

The dashboard surfaces key HR questions:

- How many employees do we have, and in which job roles?
- What is our gender distribution across the organisation?
- How are employees distributed by age and qualification?
- How do salary and leave patterns vary by role and education?
- How has our team grown over time?

The project is inspired by the classic HR analytics dashboard walkthrough for Power BI and extended with multiple detailed analysis pages, DAX measures, and clean report layout.

<br>

### **Project Highlights**

- **End-to-end Power BI workflow:** Import, clean, model, and visualise HR data from Excel.
- **Simple star schema model:** Central `Staff` table plus a `Qualification Dimension` table.
- **Reusable DAX measures:** Headcount, average salary, min/max salary, average leave, staff with high leave balance, and cumulative headcount.
- **Multi-page design:** One main dashboard + focused drill-down pages (job count, gender, age, salary, leave, employee index).
- **Portfolio-ready:** Clear layout, descriptive titles, and business-friendly wording suitable for interviews and data-analytics portfolios.

---

## **Features**

### **Main HR Dashboard**

- **Key Metrics Cards**
  - Total headcount
  - Average salary
  - Average leave balance
  - Number of employees with leave balance over a threshold (e.g. > 20 days)

- **Job Role Distribution**
  - Horizontal bar chart: headcount by job title  
  - Shows which roles dominate the workforce (e.g. Packaging Associate, Production Operator, Research Scientist, etc.)

- **Gender Composition**
  - Pie / donut chart showing male vs female headcount percentages.
  - Gives an instant view of diversity.

- **Age Distribution**
  - Column chart using age bins (20–25, 25–30, 30–35, …).
  - Optional split by gender to see where age groups differ across genders.

- **Salary vs Qualification**
  - Scatter / dot plot of salary versus qualification level.
  - Colour legend for education levels (High School, Diploma, Bachelor’s, Master’s).
  - Reveals overlaps and gaps in salary ranges by education.

- **Team Growth Over Time**
  - Line chart of cumulative headcount by date of joining.
  - Highlights hiring waves and organisational growth since a base year (e.g. 2018).

---

### **Detailed Analysis Pages**

You can adapt or remove pages as you like; this is the structure used in the `.pbix`:

- **Job Count**
  - Bar chart: headcount by job title.
  - Dedicated page for quick staffing overview by role.

- **Gender Job Analysis**
  - Pie chart: headcount by gender.
  - Slicer by job title to see gender mix for specific roles.

- **Age Analysis**
  - Column chart: headcount by age bins and gender.
  - Identifies age clusters and any gender skew by age group.

- **Salary Analysis**
  - Table / matrix:
    - Job Title
    - Average Salary
    - Headcount
    - Minimum Salary
    - Maximum Salary
  - Great for HR and finance-style discussions about pay ranges.

- **Salary Employee Analysis**
  - Bar chart: headcount by job title.
  - Table: Top 3 highest-paid employees.
  - Table: Top 3 lowest-paid employees.
  - Useful for spotting outliers for further review.

- **Salary Qualification Analysis**
  - Scatter chart: salary vs qualification ID with colour by qualification name.
  - Helps compare compensation across education levels.

- **Employee Count Analysis**
  - Line chart: cumulative headcount over time.
  - Table: employee list with job title and numeric measure (e.g. salary or headcount).
  - Useful for understanding hiring trends and workforce growth.

- **Employee Index**
  - Flat table of all staff:
    - Emp ID, Name, First Letter, Job Title, Salary, etc.
  - Functions as an interactive employee directory.

- **Leave Balance Analysis**
  - Bar chart: average leave balance by job title, plus measure of employees with high leave balance.
  - Optional gender split to see leave usage patterns by gender.

---

## **Getting Started**

Follow the steps below to run and explore the dashboard locally.

### **Project Structure**

A typical layout of this repository:

    hr-analytics-dashboard-powerbi/
    ├─ HR_Dashboard.pbix              # Main Power BI report
    ├─ data/
    │  └─ HR_Staff_Data.xlsx          # HR dataset (embedded or used for refresh)
    ├─ screenshots/
    │  └─ hr-dashboard-main.png       # Main dashboard screenshot
    ├─ LICENSE                        # MIT License (optional)
    └─ README.md

You can rename files, but update the README and Power BI connections accordingly.

---

### **Prerequisites**

- **Operating System**
  - Windows 10 or later (Power BI Desktop is Windows-only at the moment).
- **Power BI Desktop**
  - Download from the official Microsoft Power BI download page.  
  - Either install from the Microsoft Store or via the standalone installer.  
- **Excel or CSV Viewer (optional)**
  - To inspect or modify `HR_Staff_Data.xlsx` before loading or refreshing.

---

### **Installation**

You have two main options: cloning via Git or downloading the ZIP.

1. **Clone the repository (recommended)**

   - In a terminal:

     - git clone https://github.com/brej-29/hr-analytics-dashboard-powerbi.git
     - cd hr-analytics-dashboard-powerbi

2. **Download ZIP (no Git needed)**

   - Go to the GitHub repository page.
   - Click the green **Code** button → **Download ZIP**.
   - Extract the ZIP to a local folder.

After either method, you should see `HR_Dashboard.pbix` and the `data/` & `screenshots/` folders locally.

---

### **Configuration**

Depending on how the `.pbix` is set up, you may or may not need to re-point the data source.

1. **Open the report**
   - Launch **Power BI Desktop**.
   - Open `HR_Dashboard.pbix`.

2. **Check data source**
   - If the report opens without any warnings, the data is already embedded and you can explore immediately.
   - If you see a **“Couldn’t find the data source”** or **“Permission”** warning:
     - Go to **Home > Transform data > Data source settings**.
     - Edit the file path to point to your local copy of `data/HR_Staff_Data.xlsx`.
     - Apply changes and refresh.

3. **Refresh the dataset**
   - Click **Home > Refresh** to reload the data and recompute measures.

---

### **Usage**

Once the report is open in Power BI Desktop:

1. **Main HR Dashboard**
   - Start on the main page to see:

     - KPI cards for headcount, average salary, average leave, high-leave employees.
     - Job role bar chart, gender pie, age distribution.
     - Salary vs qualification scatter.
     - Cumulative headcount over time.

   - Use the filters or slicers (if present) to slice data by job title, gender, or other dimensions.

2. **Navigate to Analysis Pages**
   - Use the **page tabs** at the bottom of Power BI:

     - `Job Count`
     - `Gender Job Analysis`
     - `Age Analysis`
     - `Salary Analysis`
     - `Salary Employee Analysis`
     - `Salary Qualification Analysis`
     - `Employee Count Analysis`
     - `Employee Index`
     - `Leave Balance Analysis`

   - Each page focuses on one analytical angle:
     - Job roles, diversity, demographics, salary structure, leave balances, or individual employees.

3. **Interactivity & Exploration**
   - Hover over charts to view tooltips (individual data points).
   - Click on bars, slices, or scatter points to cross-filter other visuals.
   - Experiment with different combinations of filters to answer HR questions such as:
     - “Which roles have the highest average salary?”
     - “What is the age and gender mix in specific job titles?”
     - “Which employees have unusually high or low salaries?”
     - “Which roles accumulate more unused leave?”

4. **Modifying the Report (Optional)**
   - Use **Model view** to inspect the relationship between `Staff` and `Qualification Dimension`.
   - Open **Power Query** to review data cleaning steps.
   - Add your own measures and visuals to extend the project.

---

## **License**

This project is licensed under the **MIT License**.  
See the `LICENSE` file in this repository for full details.

---

## **Contact**

If you’d like to discuss this project, provide feedback, or connect:

- LinkedIn: <a href="https://www.linkedin.com/in/brejesh-balakrishnan-7855051b9/">Brejesh Balakrishnan</a>

Feel free to fork the repo, open issues, or suggest improvements!
