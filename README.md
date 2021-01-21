# AntisemiticTweets
 
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


