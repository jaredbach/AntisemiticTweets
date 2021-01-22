# AntisemiticTweets
This is the beginning of a repository that will be used to create a Twitter bot that will be capable of identifying and labeling antisemitic Tweets on Twitter. The first component of this project is to, first, set up the environment. The second component is to use the snscrape module to collect training data from Twitter. The third component is to use the collected data to create word clouds to better understand the substance of the Tweets being analyzed. Future components will be added as this project progresses.

# Component 1: Virtual Environment
## Step 1: Create a Virtual Environment
I recommend creating a Virtual Environment in Visual Studio Code or PyCharm. Please note that the instructions for creating a virtual environment assume that you are using a Mac. Users with a PC may need to follow different instructions.

Let’s say that the name of the virtual environment that you want to create is:
		
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
To learn more about the scnscrape module, check out this [Medium article by Martin Beck](https://medium.com/better-programming/how-to-scrape-tweets-with-snscrape-90124ed006af). In this repository, the PullAntisemiticTweets.ipynb contains the pull_twitter_query(). This function was used to pull the Twitter queries of 'Jews', 'Zionist', and 'Israel'. 50 Tweets from each day of the year in 2020 were pulled from Twitter. This created a total of 54,900 Tweets collected in .json format. A .json file was created for each day of the year for each query. These query .json files can be found in their respective named folders. These .json files were then combined, cleaned, and exported to the Tweets.csv file. Another CSV file was also created using a different type of model contained in the Ekphrasis.ipynb file and was exported to the Ekphrasis_Tweets.csv file.

**Please Note: the PullAntisemiticTweets.ipynb file does _NOT_ need to be run locally on your computer, since the final, cleaned CSV file with the 54,900 Tweets is already located in this repository by the names Tweets.csv and Ekphrasis_Tweets.csv. If you wish to run this file locally on your own computer for other queries that you may be interested in exploring, make sure the OS directory that is referenced in the pull_twitter_query() function is adjusted, so it works on your local system. Pay attention to the comments in the PullAntisemiticTweets.ipynb file for more context and guidance.**

# Component 3: Word Cloud
The next compoent of this project is to create word clouds to help us visually better understand the content of our Tweets. In this repository, the WordCloud.ipynb file contains the word_cloud() function. This function can be used to create different word cloud images from the Tweets.csv file and the Ekphrasis_Tweets.csv file. I encourage this function to be run a variety of times and for lots of different word clouds to be created. Word cloud images will be automatically saved to the repository. 

Files are named using the following formula: <br>
"WordCloud _ {# of Words} _ Words _ {# of Tweets Requested} _ Tweets_Queries _ {Query Filter} _ Seed _ {Seed #}.png"  <br>

Which means if: <br>
+ There are 60 words in your word cloud
+ A random sample of 5000 Tweets are in your word cloud
+ Your query(ies) include: 'Jews', 'Zionist', and 'Israel'
+ Your seed is 80

The file name would look like this: <br>
"WordCloud_60_Words_5000_Tweets_Queries_JZI_Seed_80.png" <br>

**Please Note: pay attention to the user input being asked for in the command prompt. The user input is supposed to help customize the word clouds. The options inputted will also affect the naming of the files saved.**


