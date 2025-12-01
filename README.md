

# **YouTube Shorts Performance Analysis — Detailed Data Analyst Report**

## **1. Introduction**

The rise of YouTube Shorts has created a new opportunity for creators and businesses to reach a large audience in a short time. However, many creators still do not know what factors actually influence engagement.

This project focuses on understanding how **video duration** affects **engagement**, especially the **Likes per View** ratio. The analysis is built using Python, statistical testing, and visual insights.

---

## **2. Problem Statement**

Creators often assume that making longer or shorter videos will automatically improve performance.
But is this actually true?

The core question of this study is:
**“Does the duration of a YouTube Short significantly impact engagement?”**

To answer this, a full data analysis workflow is applied:

* Data cleaning
* Feature engineering
* Visualization
* Statistical testing (T-Test)
* Insights and recommendations

---

## **3. Objective of the Study**

The project aims to:

1. Explore the relationship between video duration and engagement.
2. Understand patterns in viewer behavior.
3. Compare performance across different duration groups.
4. Use hypothesis testing to validate assumptions.
5. Provide clear insights for creators and marketers.

---

## **4. Dataset Description**

The dataset contains several key fields related to YouTube Shorts performance, including:

* **Views**
* **Likes**
* **Duration (seconds)**
* **Engagement indicators**

From this, new metrics were created to better study user behavior.

### **4.1 Data Quality Check**

Before analysis, the dataset was inspected for:

* Missing values
* Incorrect types
* Outliers
* Zero views or zero likes cases

The dataset required minor cleaning but overall had a manageable structure.

---

## **5. Tools & Technologies Used**

This entire project was completed using standard data analysis tools:

### **Programming & Libraries**

* **Python**
* **Pandas** → data cleaning, transformation
* **NumPy** → mathematical operations
* **Matplotlib & Seaborn** → data visualization
* **SciPy (stats.ttest_ind)** → hypothesis testing
* **Jupyter Notebook** → end-to-end workflow

These tools helped build a structured and repeatable analysis process.

---

## **6. Data Cleaning & Preparation**

### **6.1 Data Cleaning Steps**

* Removed rows with missing values
* Converted duration fields to numeric format
* Handled rows with zero views (to avoid division errors)
* Checked for duplicated entries

### **6.2 Feature Engineering**

Created new key metrics:

#### **Likes per View ratio**

```
likes_per_view = likes / views
```

This metric gives a fair measure of engagement, regardless of how many views a video gets.

#### **Duration Binning**

The videos were grouped into duration categories:

* **Short**
* **Medium**
* **Long**

This allowed comparing groups clearly.

---

## **7. Exploratory Data Analysis (EDA)**

EDA helped understand the dataset before formal testing.

### **7.1 Views vs Likes**

There was no strict linear relationship.
Some short videos went viral, while others didn't.
Medium videos were more consistent but not always high performing.

### **7.2 Duration Distribution**

Most videos were concentrated in Short and Medium categories.
Long videos were fewer.

### **7.3 Engagement Trends**

* Very short videos had high variance: some very viral, some very weak.
* Medium-duration videos showed stable patterns.
* Duration alone did not predict likes.

---

## **8. Hypothesis Testing (T-Test)**

The statistical test was used to see if Short and Medium videos differ in engagement.

### **8.1 Hypotheses**

* **Null Hypothesis (H0):**
  The average Likes per View is the same for Short and Medium duration videos.

* **Alternative Hypothesis (H1):**
  The average Likes per View is different between the two groups.

### **8.2 Test Used**

Independent **two-sample T-Test** via SciPy.

### **8.3 Result Summary**

* p-value ≈ 0.31
* Since p > 0.05, we **fail to reject the null hypothesis**

### **8.4 Interpretation**

There is **no statistically significant difference** in engagement between Short and Medium duration videos.
In simple words:
➡️ **Duration does not strongly change engagement.**

---

## **9. Visual Analysis**

### **9.1 Box Plots**

Box plots for Short and Medium categories showed overlap in engagement distributions.

### **9.2 Scatter Plots (Duration vs Likes)**

No strong trend.
Engagement depended more on content, not duration.

### **9.3 Histograms**

Duration groups did not show drastically different engagement patterns.

---

## **10. Key Insights**

### **Insight 1: Duration does not guarantee engagement**

The hypothesis testing and visuals both show that duration alone cannot predict likes.

### **Insight 2: High variation in very short videos**

Short videos (<10 seconds) can be very viral or very weak.
This suggests that content quality plays a major role.

### **Insight 3: Medium videos are stable but not exceptional**

Engagement is more predictable but not always high.

### **Insight 4: Content quality > Length**

The initial hook and topic matter far more.

### **Insight 5: Creators should optimize content, not duration**

Focusing on visuals, captions, audio, and storytelling gives better results.

---

## **11. Recommendations**

### For Creators

* Don't worry too much about perfect duration.
* Focus on a strong hook in the first 2 seconds.
* Use trending audio or topics.
* Improve thumbnails and captions.
* Keep videos visually engaging throughout.

### For Marketers

* Duration should not be the only target metric.
* Use engagement metrics (likes per view) for real performance tracking.
* Test multiple variations of content style instead of duration.

### For Data Teams

* Add more features: tags, category, upload time, audio usage, etc.
* Build models predicting engagement based on content attributes.

---

## **12. Conclusion**

This analysis clearly shows that **video duration alone does not significantly influence engagement on YouTube Shorts**.
Creators often assume that making longer videos will get them more likes, but the statistical test proves otherwise.

The project demonstrates a complete analytical workflow using Python, from data cleaning to hypothesis testing, and provides actionable insights for creators and marketing teams.


