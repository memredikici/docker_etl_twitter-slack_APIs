# Docker Pipeline - ETL Job - Twitter, Slack APIs 
Docker Pipeline created with ETL Job, Sentiment Analysis and Posting on Slack.

## Table of Contents
- [General info](#general-info)
- [Technologies and Libraries](#technologies-and-libraries)
- [Setup](#setup)
- [Status](#status)

### General info
In this Project, I've built Docker Pipeline which consists of tweet collector, its sentiment analysis and posting them via slack bot.  
Every 10 minutes last tweet about Covid is collected, saved into Database and shared in Slack.  
Followings applied:
- Docker Image, Container, Compose
- Twitter API
- Slack API
- Logging
- .env -> key protection
- polling method

### Technologies and Libraries
- Python 3.8
- requests
- pandas
- logging
- tweepy
- vaderSentiment
- sqlalchemy
- dotenv
- time

### Setup
The main reason of using docker-container is to make setup easy.  
Here you can find Docker commands:
- For running these commands you need to `cd` into the folder that contains the `docker-compose.yml` file.

- (re-)build images of services 
    ```
    docker-compose build
    ```

- run/start containers in the background
    ```
    docker-compose run -d
    ```

- list all running containers/ services
    ```
    docker-compose ps
    ```

- view the output of individual services
    ```
    docker-compose logs <servicename>
    ```

### Status
The goal of this project is almost accomplished. Some creative ideas for the use of Tweets can be applied to program:
1. Tweets of some specific users could be collected, analyzed and compared their sentiments.
2. Creating a program which collects your own tweets and gives you a feedback according to your tweets' sentiments.