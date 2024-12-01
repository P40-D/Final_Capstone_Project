# Final Capstone Project Proposal Outline

## I. Introduction

- **Brief overview of the project idea**:  
  This project aims to explore the chat history of Twitch videos, analyzing the positivity or negativity of the messages over time. By performing sentiment analysis on the chat, an interactive timeline will be created, allowing users to visualize the positivity of the chat and click on specific areas to open links to the corresponding timestamps in the video.

- **Explanation of the chosen project type (EDA or model)**:  
  This project falls under **Exploratory Data Analysis (EDA)** as it involves analyzing and visualizing Twitch chat data to gain insights into user sentiment, trends, and interactions during the stream.

## II. Project Objective

- **Clear statement of the project's goal and what you aim to achieve**:  
  The primary goal is to create an interactive and insightful exploration of Twitch chat messages from a specific video, identifying patterns of positivity and negativity throughout the stream. The project will present a timeline of chat sentiment, and users will be able to click on the timeline to access corresponding timestamps in the Twitch video.

- **The problem you want to solve, or the questions you aim to answer**:  
  - How does the sentiment of chat messages evolve over the course of a Twitch stream?  
  - Are there any specific moments in the video that correlate with spikes in positivity or negativity in the chat?  
  - Can a timeline be created to visualize sentiment changes and provide users with an interactive way to explore the data?

## III. Data Description

- **Description of the dataset(s) you plan to use**:  
  The dataset will consist of chat messages from a selected Twitch video. This will include:
  - The text of each message.
  - The timestamp of when each message was posted.
  - User information (such as username and badges) for context, although this will not be the primary focus.
  - The sentiment of each message, derived through sentiment analysis.

- **Source(s) of the data**:  
  The chat data will be sourced using tools like **Twitch Chat Downloader** for historical data or using **Twitch IRC** for live chat scraping. The video data will be sourced from Twitch’s platform, specifically the URL of the video being analyzed.

- **Overview of the data's structure and format**:  
  The data will be structured in a CSV file, where each entry will contain the following fields:
  - **timestamp**: Time of the message.
  - **message**: Text content of the chat message.
  - **user**: Username of the person who posted the message.
  - **sentiment**: Sentiment label based on sentiment score (e.g., Positive, Neutral, Negative).

## IV. Methodology

- **Explanation of the approach you intend to take to accomplish your project objectives**:  
  - **Data Collection**: Use **Twitch Chat Downloader** or **Twitch IRC** to collect chat logs from a specific Twitch video.
  - **Sentiment Analysis**: Apply sentiment analysis using tools like **VADER** or **TextBlob** to classify chat messages into positive, neutral, or negative categories.
  - **Data Processing**: Clean and preprocess the data to ensure it is suitable for visualization, including timestamp formatting and sentiment classification.
  - **Visualization**: Create an interactive timeline using **Plotly** or **Dash** where sentiment changes over time are visualized as a time series. The x-axis will represent time (timestamps from the chat messages), and the y-axis will represent sentiment, with markers for the positive, neutral, and negative sentiments.

- **For EDA projects: Outline of the analytical techniques and visualization tools you plan to use**:
  - **Sentiment Analysis**: Using sentiment analysis libraries to classify chat messages.
  - **Data Aggregation**: Group messages by timestamp or time intervals (e.g., every minute or every 100 messages) to visualize sentiment over time.
  - **Visualization**: Use **Plotly** or **Dash** to create the interactive timeline where users can click on a point to view a specific timestamp and open the video at that time.

## V. Expected Deliverables

- **Detailed description of what you plan to deliver as the final outcome of your project**:  
  - An interactive web-based timeline of Twitch chat sentiment that allows users to explore positivity and negativity throughout the stream.
  - A visual representation of chat sentiment over time using a time-series plot.
  - A description of key moments during the stream where sentiment spikes, with links to those timestamps in the video.

- **For EDA projects: Description of the interactive component of your project**:  
  - The interactive timeline will be clickable, allowing users to select specific areas and view the corresponding Twitch video link. Each section of the timeline will represent sentiment changes, and clicking on it will open the relevant video timestamp in a new tab or window.

## VI. Timeline and Tasks

- **Now-Dec 4th**:  
  - Collect data from a selected Twitch video (either using **Twitch Chat Downloader** or the **Twitch IRC** method).
  - Perform initial data cleaning and preprocessing.
  - Implement sentiment analysis on the chat data.
  - Test sentiment analysis on sample data and refine the analysis process.
  - Create visualizations of the sentiment data, focusing on an interactive timeline.
  - Implement the interactivity (clicking on the timeline to view video links).
  - Final testing and refinement of the project.
  - Ensure the interactive components work seamlessly, and all data is correctly displayed.
  - Prepare the final report and presentation.
  - Deploy the web app (using **Dash**, **Streamlit**, or **Heroku**).

## VII. Potential Challenges

- **Identification of any potential obstacles or challenges you anticipate facing during the project**:  
  - Difficulty in obtaining chat logs for older Twitch videos.
  - Sentiment analysis accuracy, particularly with informal or slang-heavy language often used in Twitch chats.
  - Ensuring smooth interactivity with the timeline visualization, especially handling timestamp precision and video links.
  
- **Brief outline of how you plan to address these challenges**:  
  - For chat logs, consider using multiple sources or reaching out to streamers for chat data access.
  - Improve sentiment analysis accuracy by training custom models or adjusting thresholds to better capture the unique language of Twitch chats.
  - Test the interactive components thoroughly and ensure proper handling of video URLs and timestamps for a seamless user experience.
