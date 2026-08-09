# devlab-internship-Week5-Task2
# YouTube Trending Videos — Data Analysis

## Project Overview

This project analyzes trending YouTube videos from the United States to understand the main factors associated with video popularity, audience engagement, and trending performance.

The analysis combines video-level metrics such as views, likes, dislikes, comments, publishing day, tags, and category information. The goal is to identify patterns that can help content teams understand what types of videos achieve high reach and strong audience interaction.

The project includes data cleaning, category mapping, engagement metric calculation, exploratory data analysis, correlation analysis, and visualization.

---

## Dataset
https://www.kaggle.com/datasets/datasnaek/youtube-new

The dataset contains **40,949 rows and 16 columns** representing trending YouTube videos.

The `US_category_id.json` file was also processed to map `category_id` values to readable `category_name` labels.

### Main Data Processing Steps

* Loaded `USvideos.csv` using UTF-8 encoding.
* Parsed `US_category_id.json`.
* Mapped `category_id` to `category_name`.
* Converted relevant date fields into datetime format.
* Created additional engagement-related metrics.
* Analyzed video performance by category and publishing day.
* Examined relationships between views, likes, dislikes, comments, and tags.

---

## Engagement Metrics

Several metrics were created to better understand audience interaction.

### Engagement Rate

```text
(likes + dislikes + comment_count) / views × 100
```

This metric measures the overall level of interaction relative to the number of views.

### Like Rate

```text
likes / views × 100
```

This shows the percentage of viewers who interacted with the video through likes.

### Dislike Rate

```text
dislikes / views × 100
```

This measures the proportion of views associated with dislikes.

---

## Exploratory Analysis

The analysis focused on several important questions:

* Which categories receive the most views?
* Which categories have the strongest engagement?
* Does a high number of views lead to more likes and comments?
* Does high engagement necessarily mean high reach?
* Which publishing days perform better?
* Is the number of tags associated with video popularity?
* Which videos achieve trending status particularly quickly?

---

# Key Findings

## 1. Music content has the strongest overall performance

Music videos show the strongest overall performance in terms of both reach and audience interaction.

The **Music** category has the highest average views at approximately **1.39M** and also has the highest engagement rate at approximately **8.23%**.

This suggests that music-related content can be an effective format when the objective is to achieve both:

* High audience reach
* Strong audience interaction

For a content team, music-related formats may therefore be prioritized when both visibility and engagement are important goals.

---

## 2. Publishing day can matter, but it is not the only factor

Publishing day appears to have an association with video performance.

**Friday** has the highest average number of views at approximately **894K**, followed by **Sunday** with approximately **859K** average views.

This suggests that Friday and Sunday publishing windows may be worth testing.

However, publishing day should not be considered independently. Other factors such as:

* Content category
* Channel strength
* Audience size
* Topic popularity
* Initial promotion

can also strongly influence video performance.

Therefore, changing the publishing strategy based only on weekday performance may not be sufficient.

---

## 3. Views are strongly connected with likes and comments

The analysis shows a clear relationship between video reach and audience interaction.

The correlation between **views and likes is 0.761**, while the correlation between **views and comments is 0.600**.

This indicates that videos reaching a larger audience generally generate more visible audience interaction.

In practical terms, increasing reach can also increase the absolute number of likes and comments. However, this does not necessarily mean that the audience is proportionally more engaged.

---

## 4. High engagement does not automatically mean high reach

One of the most important findings is the very weak relationship between views and engagement rate.

The correlation between **views and engagement rate is only 0.057**.

This means that a video can have:

* A relatively small number of views
* But a highly engaged audience

At the same time, a video can receive millions of views while having a relatively low engagement rate.

Therefore, **reach and engagement should be evaluated as separate performance metrics**.

Content teams should not rely only on engagement rate when evaluating video success. A more complete evaluation should consider both:

* **Reach:** views
* **Audience interaction:** engagement rate

---

## 5. Fast trending performance is common among high-performing content

Several highly successful videos reached trending status very quickly, with some entering the trending list within approximately **0.25–1 day**.

Examples include:

* YouTube Rewind
* Avengers: Infinity War
* VENOM
* BTS — FAKE LOVE

This pattern suggests that strong initial audience demand can help a video reach trending status very quickly.

For content teams, this highlights the importance of the first hours after publication.

Early promotion and audience activation strategies may help increase initial momentum. Examples include:

* Strong launch-day promotion
* Social media promotion
* Notifications to existing audiences
* Encouraging early interaction
* Coordinated release campaigns

---

# Additional Findings

### Category Performance

* **Music** has the highest average views at approximately **1.39M**.
* Music also shows very strong engagement performance.
* **News & Politics** has the highest average engagement rate in the broader category analysis at approximately **6.8%**.
* Some categories can achieve strong engagement without necessarily achieving the highest view counts.

### Correlation Findings

The analysis identified several important relationships:

| Variables               | Correlation | Interpretation                 |
| ----------------------- | ----------: | ------------------------------ |
| Views & Likes           |       0.761 | Strong positive relationship   |
| Views & Comments        |       0.600 | Moderate positive relationship |
| Views & Engagement Rate |       0.057 | Very weak relationship         |
| Tags & Views            |        0.18 | Weak positive relationship     |

These results show that audience size is strongly related to the absolute number of likes and comments, but not necessarily to engagement rate.

---

# Business Insights

## 1. Prioritize content that combines reach and engagement

Music content demonstrates that it is possible to achieve both high views and strong audience interaction.

Content teams can study successful music formats and apply similar engagement strategies to other categories.

## 2. Test Friday and Sunday publishing windows

Since Friday and Sunday show relatively high average views, these days can be used for controlled publishing experiments.

Rather than immediately changing the entire publishing strategy, channels can compare performance across different days while controlling for content type.

## 3. Track reach and engagement separately

A video with millions of views is not automatically more successful from an engagement perspective.

Teams should monitor both **views** and **engagement rate** to distinguish between broad-reach content and highly engaged niche content.

## 4. Focus on early audience activation

Videos that become trending shortly after publication demonstrate the importance of early momentum.

Launch-day promotion should therefore be considered an important part of the content distribution strategy.

## 5. Do not over-rely on tags

The correlation between tags and views is relatively weak (**r = 0.18**).

This suggests that simply adding more tags is unlikely to be a major driver of video popularity. Greater attention should be given to content quality, topic selection, audience demand, and promotion.

---

# Visualizations

The analysis includes visualizations designed to make the main patterns easier to understand:

* Correlation heatmap
* Average views by category
* Engagement rate by category
* Views distribution by publishing weekday
* Views vs engagement rate scatter plot
* Category-based performance comparisons

The scatter plot is particularly useful for identifying different audience patterns, such as:

* **High views + low engagement:** passive audience
* **Low views + high engagement:** niche but loyal audience
* **High views + high engagement:** strong overall performers
* **Low views + low engagement:** weaker-performing content

---

# Conclusion

The analysis shows that YouTube video performance depends on multiple factors rather than a single metric.

Music content demonstrates particularly strong performance in both reach and engagement, while publishing day may also influence average views. Views have a strong relationship with absolute likes and comments, but high reach does not necessarily result in a high engagement rate.

The low correlation between views and engagement rate highlights an important business lesson: **reach and audience engagement should be measured separately**.

The analysis also suggests that early audience activation can be important for videos aiming to reach the trending list quickly.

Overall, content teams can use these findings to make more informed decisions about content formats, publishing schedules, launch strategies, and performance measurement.
