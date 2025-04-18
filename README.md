Created by: Courtney Cheung and Ayush Roy

## Description ##
The "Trending this week" feature shows trending articles based on viewership. <br/>
Data is from the past 7 days, with viewership of recent articles weighted higher than older articles. <br/>
Viewership data is updated every two hours.

## Structure ##
Backend
* source/main.py: finds the top articles' url, image url, headline, subheadline, date, and bylines using Google Analytics API and Arc Content API 
* template.yaml: creates an AWS lambda function, event rule, and s3 bucket
* Google Analytics credentials file located in AWS lambda function (not in public repo)

Frontend
* arc_display.html: displays the top 5 articles (paste this code into the Arc html box)

## Requirements ##
To run source/main.py, install requirements.txt and Pandas. Obtain Google Analytics API credentials file, and place it under source. <br/>
To deploy template.yaml, install AWS CLI and AWS SAM CLI. Deploy through PyCharm using "sync serverless application".

## Product ##

![trending_screenshot.png](trending_screenshot.png)


