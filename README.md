# Play-Store-App-Review-Analysis

## 1. **Problem Statement**

The Play Store apps data has enormous potential to drive app-making businesses to success. Actionable insights can be drawn for developers to work on and capture the Android market.Each app (row) has values for catergory, rating, size, and more. Another dataset contains customer reviews of the android apps.Explore and analyze the data to discover key factors responsible for app engagement and success.
## 2. **Introduction:**
### **We are provided with two dataset**
* Play_store_data: It contains the basic details of the app like number of user reviews, ratings, etc.
* User_reviews: It contains the user reviews and its sentiment score for the respective app. We need to explore and analyze the data to discover key factors responsible for app engagement and success.
### The contents of play_store_data are:
* App: It contains the name of the app with a short description (optional).
* Category: This section gives the category to which an app belongs. In this dataset, the apps are divided among 33 categories.
* Size: The disk space required to install the respective app.
* Rating: The average rating given by the users for the respective app. It can be in between 1 and 5.
* Reviews: The number of users that have dropped a review for the respective app.
* Installs: The approximate number of times the respective app was installed.
* Type: It states whether an app is free to use or paid.
* Price: It gives the price payable to install the app. For free type apps, the price is zero.
* Content rating: It states which age group is suitable to consume the content of the respective app.
* Genres: It gives the genre(s) to which the respective app belongs.
* Last updated: It gives the day in which the latest update for the respective app was released.* 
* Current Ver: It gives the current version of the respective app.
* Android Ver: It gives the android version of the respective app.
### The contents of user_reviews are:
* App: It contains the name of the app with a short description (optional).
* Translated_Review: It contains the English translation of the review dropped by the user of the app.
* Sentiment: It gives the attitude/emotion of the writer. It can be ‘Positive’, ‘Negative’, or ‘Neutral’.
* Sentiment_Polarity: It gives the polarity of the review. Its range is [-1,1], where 1 means ‘Positive statement’ and -1 means a ‘Negative statement’.
* Sentiment_Subjectivity: This value gives how close a reviewer’s opinion is to the opinion of the general public. Its range is [0,1]. Higher the subjectivity, closer is the reviewer’s opinion to the opinion of the general public, and lower subjectivity indicates the review is more of a factual information.
## 3. Business KPIs for developing a successful app:
Almost all the companies/organizations involved in app development maintain business KPIs divided into 3 metrics; namely, UX and performance metrics, Engagement KPI metrics, and Revenue metrics.

### a. UX and Performance metrics:
Performance metrics provide the data about an app’s technical performance. These metrics allow the development team to improve the app from a technical standpoint and pinpoint issues that hamper the user experience.
Eg: Crash reports, load speed, screen resolution, OS, etc.
### b. Engagement KPI metrics:
Engagement metrics characterize the way the users interact with the app and show whether they like it or not. The KPIs in this metric have a direct relationship with the revenue generated. Hence, this is one of the most focused metrics in an app development company.
Eg: Churn rate, retention rate, session length and depth, daily/weekly/monthly active users, etc.
### c. Revenue metrics:
These metrics give a bird' eye view of the cash flow taking place on the app. These metrics also include the money spent to acquire new users and buyers.
Eg: Average revenue per user, purchases, conversion rate, cost per install, time to first purchase, etc.
Mobile app metrics are crucial for any application. They show how well the application works from a technical standpoint, how engaged the people are, and how much money active users bring to the business.

## 4. Data pipeline:
Once we have defined and understood the columns and the type of data it contains, it is necessary to eliminate the obvious errors, NaN values, and duplicates. Apart from this in some cases it is necessary to convert the datatype of the entries in the columns into more appropriate datatype.
These were approached one column at a time. Following is a brief summary of how the error, NaN, and duplicate values were handled:
### a. Play_store_data:
* Removing Duplicate Apps
* Removing 19.0 from the column rating
* Removing 1.9 from the column category
* Convert the dates in datetime.
* The resultant number of rows post cleaning the data: 9660
### b. User_review:
All the rows containing NaN values were dropped.
The resultant number of rows post cleaning the data: 37427
## 5. Data Visualization
## a. App Type
* The first thing that comes to mind when downloading an app is whether it is free or paid.
* Here we can see there is a total of 8902 apps that are free and 756 apps are paid.
![image](https://user-images.githubusercontent.com/85746056/155701788-d0bfbe6b-620f-4822-bb18-25bdb0906549.png)

## b. Content Rating
![image](https://user-images.githubusercontent.com/85746056/155705715-0727e740-7ee2-4453-b93a-6780611d1835.png)
* Here we can see that the 7903 app belongs to the content rating everyone and 1036 is for teens. 
* For Mature 17+ there are 393 apps. 
* Only 3 apps fall under the 18+ category.
## C. Number of apps in each category
* The apps in the dataset are divided among various categories based on its applications and use-cases.
* In this dataset, the apps are divided into a total of 33 categories.
* The higher the number of apps in a category, the more competitive it is to launch an app in the said category.
* From the bar graph below, we can say that the “Family” category has the highest number of apps, followed by the “Game” and “Tools” category. From this we can say that these categories are the most competitive to get in to.

![image](https://user-images.githubusercontent.com/85746056/155705986-2fedbaba-b289-4a3f-ada7-230261c89308.png)



