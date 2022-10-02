# Web Scraping: NBA Players

## Introduction
This repository is an introductory tutorial on web scraping using the [rvest](https://rvest.tidyverse.org/) package in R. Specifcally, we are interested in
scraping information about current players in the National Basketball Association (NBA) from the ESPN [website](https://www.espn.com/nba/teams).

## Web scraping
Each team has their own web page for their roster, for example, the [Boston Celtics](https://www.espn.com/nba/team/roster/_/name/bos/boston-celtics) and the [New York Knicks](https://www.espn.com/nba/team/roster/_/name/ny/new-york-knicks).
It contains a table of all their current active players and details about their: 
- Name 
- Position
- Age
- Height 
- Weight
- College 
- Salary

In order to extract this information, we use a Chrome extension called [SelectorGadget](https://chrome.google.com/webstore/detail/selectorgadget/mhjhnkcfbdhnjickkkdbjoemdmbfginb?hl=en) which generates the CSS selector of an element. We then store them into variables that are used to create a final data frame. 

Furthermore, on each player's name, there is a hyperlink that leads us to their individual player profile, which contains statistics in the most recent NBA season:
- Average points per game
- Average rebounds per game
- Average assists per game
- Player efficiency rating

For this, we write a function that fetches the season statistics for each player on the team roster and combine them into the data frame from earlier on.

After the whole process is completed and validated for one team, we use a for loop to repeat the scraping process for all 30 NBA teams by changing the URL.

## Exploratory data analysis
Some simple exploratory analysis was also done on the scraped data. In summary, the key insights are as follows:
- Point guards are the shortest and lightest players, while centers are the tallest and heaviest players
- Average points per game is highly positively correlated with annual player salary
- Height is negatively correlated with average rebounds per game 
- Kentucky and Duke are by far the most popular colleges for NBA prospects 
- The current combined annual salary for the top 10 highest-paid players total around $438 million

![image](https://user-images.githubusercontent.com/68457884/193443887-e8a0c4e0-5ba2-46d9-a282-92a2140c94ba.png)
![image](https://user-images.githubusercontent.com/68457884/193444086-a558b617-4a6c-4735-a6ca-9e3f703b54b8.png)
![image](https://user-images.githubusercontent.com/68457884/193444090-c60b5df2-fd10-46e0-85ab-2a15cd52b85e.png)
![image](https://user-images.githubusercontent.com/68457884/193444092-de7d39ee-6394-4067-be55-577d1e69399a.png)
![image](https://user-images.githubusercontent.com/68457884/193444095-ba3ff414-9336-485f-8b3f-1bb99b55e023.png)

## Medium article 
Link to full project write-up on Level Up Coding [here](https://levelup.gitconnected.com/practical-introduction-to-web-scraping-in-r-nba-players-15393a3a0f78).

## Follow me 
- [Facebook](https://www.facebook.com/chongjason914)
- [Instagram](https://www.instagram.com/chongjason914)
- [Twitter](https://www.twitter.com/chongjason914)
- [LinkedIn](https://www.linkedin.com/in/chongjason914)
- [YouTube](https://www.youtube.com/jasonchong914)
- [Medium](https://www.medium.com/@chongjason)
