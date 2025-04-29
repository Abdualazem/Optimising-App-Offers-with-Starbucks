# Starbucks Capstone Challenge

## Motivation

This project analyses simulated data from the Starbucks rewards mobile app to determine which demographic groups respond best to different offer types. The goal is to optimise the targeting of app offers to maximise customer engagement and business value.

## Libraries Used

- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- json

## Repository Structure

| File/Folder                      | Description                                                                 |
|----------------------------------|-----------------------------------------------------------------------------|
| `Starbucks_Capstone_notebook.ipynb` | Main Jupyter notebook with data exploration, cleaning, analysis, and modelling |
| `data/portfolio.json`            | Offer metadata (type, duration, reward, etc.)                               |
| `data/profile.json`              | Customer demographic data                                                   |
| `data/transcript.json`           | Transaction and offer event records                                         |
| `README.md`                      | Project overview and documentation                                          |

## Data Description

The project uses three main data files:

- **portfolio.json**: Contains offer ids and meta data about each offer (duration, type, reward, difficulty, channels).
- **profile.json**: Contains demographic data for each customer (age, gender, income, date joined).
- **transcript.json**: Contains records for transactions, offers received, offers viewed, and offers completed, including timestamps and amounts.

## Summary of Results

- Explored and cleaned the Starbucks app data, addressing missing values and data inconsistencies.
- Analysed customer demographics and offer response patterns.
- Built models/heuristics to predict offer response and optimise offer targeting.
- **Customer Segmentation:**  
  Used KMeans clustering to segment customers based on age, income, membership duration, total spend, and offer engagement.  
  Four segments were identified:
    - **Segment 0:** Older, higher-income, long-tenured, high spend and engagement.  
      *Target with premium offers, loyalty rewards, and exclusive deals.*
    - **Segment 1:** Middle-aged, moderate-income, longest-tenured, moderate spend and engagement.  
      *Target with retention campaigns and personalized offers.*
    - **Segment 2:** Older, higher-income, shorter-tenured, lower spend and engagement.  
      *Target with onboarding and engagement strategies.*
    - **Segment 3:** Younger, lower-income, shortest-tenured, lowest spend and engagement.  
      *Target with introductory offers, discounts, and educational content.*

- **Key findings:**  
  - Long-tenured, high-income customers are the most engaged and spend the most.
  - Younger and lower-income customers have the lowest engagement and spend.
  - The model is effective at identifying likely offer responders but less so at identifying non-responders, indicating class imbalance.

More discussion of the results is given in the blog postv[here](https://abdualazem-fadol.medium.com/the-starbucks-rewards-experiment-surprising-trends-in-customer-behaviour-tell-f7def0067d63).

---

## Acknowledgments

- The data used in this project was provided by Starbucks and Udacity for educational purposes as part of the Udacity Data Scientist Nanodegree Capstone.
- Special thanks to Udacity, Starbucks, and the open-source Python community for their tools and resources.

---

*This project was completed as part of the Udacity Data Scientist Nanodegree Capstone.*