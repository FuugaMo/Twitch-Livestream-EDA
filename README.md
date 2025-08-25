# Twitch-Livestream-EDA

## Project Description

This project conducts an Exploratory Data Analysis (EDA) of a sample Twitch livestream interaction dataset. The primary goal is to understand user behavior and the streamer ecosystem to inform the design of a foundational metric framework for assessing the "health" of livestreaming platforms like Twitch Live. The analysis covers data cleaning, preprocessing, metric calculation, time-series analysis, and in-depth visualization.

---

## Key Findings & Insights

Through this analysis, we have derived the following core insights:

* **Long-Tail Engagement**: User engagement (such as watch duration) and the popularity of livestream streams (number of viewers) both exhibit a typical long-tail distribution. Most interactions are brief, and most streams have few viewers, while a small number of top streamers attract significant traffic.
* **High Content Supply**: In this data sample, the number of unique streamers (over 160,000) even exceeds the number of unique viewers (100,000), revealing an ecosystem with a very abundant supply of content creators.
* **Positive Correlation Between Activity and Popularity**: The data shows that streamers who broadcast more frequently tend to attract a larger unique audience. However, this relationship is not absolute, indicating that content quality and the streamer's personal brand are also crucial factors for success.
* **Brief Average Watch Duration**: The average watch duration is only about 3.14 minutes, suggesting that users have short attention spans and may frequently engage in "channel surfing."

---

## Dataset

The dataset used for this analysis is sourced from Kaggle:

* **Dataset Name**: [Twitch Live Streaming Interactions Sample Dataset](https://www.kaggle.com/datasets/volodymyrpivoshenko/twitch-live-streaming-interactions-sample-dataset)
* **Description**: This dataset contains a sample of livestream viewing interaction records from 100,000 users.
* **Key Fields**:
  * `UserId`: Unique identifier for a viewer.
  * `StreamID`: Unique identifier for a specific livestream.
  * `Streamer`: The name of the streamer.
  * `StartTime`: The time (in relative minutes) the user began watching.
  * `StopTime`: The time (in relative minutes) the user stopped watching.

---

## Technologies Used

* **Programming Language**: Python 3
* **Core Computation Engine**: Apache Spark (via `pyspark`)
* **Data Processing**: Pandas
* **Data Visualization**: Matplotlib, Seaborn
* **Development Environment**: Jupyter Notebook

---

## Setup and Usage

You can reproduce this analysis locally by following these steps:

1. **Clone this repository**:

   ````bash
   git clone https://github.com/FuugaMo/Twitch-Livestream-EDA.git
   ````

2. **Create and activate a virtual environment** (recommended):

   ````bash
   # For macOS/Linux
   python3 -m venv venv
   source venv/bin/activate
   
   # For Windows
   python -m venv venv
   .\venv\Scripts\activate
   ````

3. **Install dependencies**:
   All necessary libraries for this project are listed in the `requirements.txt` file.

   ````bash
   pip install -r requirements.txt
   ````

   *Note: Running PySpark depends on a Java environment. Please ensure that Java 8 or a later version is installed on your system.*

4. **Run Jupyter Notebook**:

   ````bash
   jupyter notebook
   ````

   In the browser page that opens, click on the `twitch_eda.ipynb` file to view and run the code.

---

## Future Work

Based on this initial analysis, future in-depth research can be conducted in the following directions:

* **Retention Analysis**: Measure user stickiness through Cohort Analysis, which is a core metric for platform health.
* **Streamer & User Segmentation**: Segment streamers and users into different tiers (e.g., top/mid/long-tail, high/low-frequency) and study their behavior patterns separately.
* **Time-Series Forecasting**: Build forecasting models based on metrics like Daily Active Users to gain insights into future trends.
* **Refine Health Metrics Framework**: Incorporate metrics for interaction, monetization, content diversity, and other dimensions to build a more comprehensive evaluation model.

---

## License

This project is licensed under the [MIT License](LICENSE).
