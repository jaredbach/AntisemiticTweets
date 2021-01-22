# AntisemiticTweets
This is the beginning of a repository that will be used to create a Twitter bot that will be capable of identifying and labeling antisemitic Tweets on Twitter. The first component of this project is to, first, set up the environment. The second component is to use the snscrape module to collect training data from Twitter. The third compoent is to use the collected data to create word clouds to better understand the substance of the Tweets being analyzed. Future components will be added as this project progesses.

# Component 1: Virtual Environment
## Step 1: Create a Virtual Environment
I recommend creating a Virtual Environment in Visual Studio Code or PyCharm.
Lets say that the name of the virtual environment that you want to create is:
		
		env

1. Create the virtual environment by opening the folder where you want the virtual environment in the terminal. 
   Execute the following code:
		
		python3 -m venv env

2. Now it is time to install packages.
   Update the terminal with this code to make sure you are working in the context of the virtual environment:
		
		source env/bin/activate

3. Make sure that the interpreter is updated to the virtual environment.
   
4. Make sure to update pip as well, using the command:
		
		pip install --upgrade pip


## Step 2: Install the Packages in the Virtual Environment
Run this command in the terminal in the virtual environment:
		
		pip install -r requirements.txt

If you are working on a pull of this repository, update this file before pushing this git repository.
		
		pip freeze > requirements. txt

# Component 2: Scraping and Cleaning Tweets
To learn more about the scnscrape module, check out this [Medium article by Martin Beck](https://medium.com/better-programming/how-to-scrape-tweets-with-snscrape-90124ed006af). In this repository, the PullAntisemiticTweets.ipynb contains the pull_twitter_query(). This function was used to pull the Twitter queries of 'Jews', 'Zionist', and 'Israel'. 50 Tweets from each day of the year in 2020 were pulled from Twitter. This created a total of 54,900 Tweets collected in .json format. A .json file was created for each day of the year for each query. These querie .json files can be found in their respective named folders. These .json files were then combined, cleaned, and exported to the Tweets.csv file. Another CSV file was also created using a different type of model contained in the Ekphrasis.ipynb file and was exported to the Ekphrasis_Tweets.csv file. **Please Note: this file does [_NOT_] need to be run, since the final, cleaned CSV file with the 54,900 Tweetss is already located in this repository by the name Jews-Tweets_Final.csv. If you wish to run this file locally on  your own computer for other queries that you may be interested in exploring, make sure the OS directory that is referenced in the pull_twitter_query() function needs to be adjusted to your own local system.**

# Component 3: Word Cloud
The next compoent of this project is to create word clouds to help us visually better understand the content of our Tweets. In this repository, the WordCloud.ipynb file contains the word_cloud() function. This function can be used to create different word cloud images from the Tweets.csv file and the Ekphrasis_Tweets.csv file. I encourage this function to be run a variety of times and for lots of different word clouds to be created. Word cloud images will be automatically saved to the repository.


