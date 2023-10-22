# YouTube-Scrapping.
 I harnessed the YouTube Data API to evaluate Shyan Wahedi's performance alongside other content creators. By extracting data on subscribers, video counts, and views, I used pandas and seaborn to create insightful visualizations, revealing trends and distinctions among the YouTubers, aiding in strategic analysis and decision-making.
## Project Overview

Welcome to my Python capstone project, where I explore YouTube data through web scraping. This project stems from my fascination with extracting valuable insights from YouTube, and it revolves around assessing the success of my favorite personal development content creator, Shyan Wahedi, in comparison to other competitors in the field.

## Project Steps

1. **API Key Creation**: The project begins with the creation of an API key using the Google Cloud Platform. This key is essential for accessing YouTube data.

2. **Library Imports**: I've imported necessary modules into my Anaconda notebook, including `googleapiclient.discovery`, `pandas`, and `seaborn`, which will be instrumental for data extraction and analysis.

3. **Data Collection**: With the API key in hand, I've gathered the channel IDs of the creators I wish to compare and stored them in a variable called `channel_ids` as a list.

4. **YouTube Service**: Next, I created a YouTube service using the `googleapiclient.discovery.build` command, passing in three parameters: the API service name (YouTube), the API version (v3), and the developer key (API key). This service object is stored in a variable called `youtube`.

5. **Data Extraction**: To extract channel details, I created a function named `get_channel_stats`. It takes two parameters: the service created (`YouTube`) and the channel IDs. Using the `youtube.channels.list` method, I retrieved a dictionary containing all the details of each channel. Afterward, I extracted the specific data I needed, including channel names, total subscriber counts, total view counts, and the total number of videos for each YouTuber. This data was stored in a DataFrame.

6. **Data Transformation**: Upon checking the data types of each column using `df.dtypes`, I noticed that all the columns were of the object data type. To rectify this, I converted the data type of subscriber count, view count, and video count into integers using the `astype` method.

7. **Data Visualization**: Following data preparation, I created three bar charts using `sns.barplot`, with channel names on the x-axis and subscriber count, view count, and video count on the y-axis. These visualizations help in making sense of the data.

   ![Screenshot 2023-10-22 203522](https://github.com/RashidEriyakalam/YouTube-Scrapping./assets/142217254/d75e079d-c8b9-4f92-8122-348b2b0b960c)

## Conclusion

From the visualizations, I've drawn some key insights. Shyan Wahedi's channel appears to be relatively new with fewer subscribers, videos, and views. Lewis stands out as the most successful YouTuber among the six, consistently delivering high-quality content. Mel Robbins, despite uploading more videos than Lewis, had significantly fewer views, possibly indicating lower content quality. Tony, with a higher subscriber count despite uploading less content, seems to have the potential for significant growth.

This project showcases the power of data analysis in the world of YouTube content creation.

## Tools Used

- Python: Data cleaning and initial exploration
- Google Cloud Platform: For creating the API key
- YouTube Data API
- Pandas and Seaborn: For data manipulation and visualization

Feel free to explore the project code and the insights uncovered. Let's continue exploring the world of data together!



