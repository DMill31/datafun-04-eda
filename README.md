# datafun-04-eda

This repository is for Project 4 of Data Analytics Fundamentals where we will be creating a project using Jupyter Notebook.

## How to Install and Run the Project

First you must clone the project to your local machine.

1. Copy the URL of the GitHub Repository you would like
2. Open Powershell and run the following commands

```shell
cd \
cd Projects
git clone https://github.com/**account**/**repo-name**
cd **repo-name**
code . 
```

If .gitignore and/or requirements.txt aren't created, create them.

After creating these files we can now Git add-commit-push using the following code in the terminal

```shell
git add . 
git commit -m "YOUR MESSAGE HERE"
git push -u origin main
```

Once pushed, we now create our virtual environment by running the command:

```shell
py -m venv .venv
```

Now we will activate the virtual environment using this command:

```shell
.venv\Scripts\activate
```

Once the virtual environment has been activated, we can install our dependencies from requirements.txt.

Before installing, it's best to update key packages first.

```shell
py -m pip install --upgrade pip setuptools wheel
py -m pip install -r requirements.txt
```

Lastly, we will select our VS Code Interpreter

1. Press Ctrl+Shift+P
2. Search for "Python: Select Interpreter"
3. Choose the Interpreter for the local .venv 

Now your project is ready and the real fun can begin

Don't forget to regularly Git add-commit-push to keep everything up to date

## Workflow for this Jupyter Notebook

### Step 1

1. Add a Title using Markdown
2. Create a header with the author name, purpose, and date
3. Create a numbered list for imports 
4. Create a Python cell for the import statements

### Step 2

Load data into a pandas Dataframe

Example:

```shell
# Load the Iris dataset into pandas DataFrame
iris_df: pd.DataFrame = sns.load_dataset('iris')

# List column names
iris_df.columns

# Inspect first few rows of the DataFrame
iris_df.head()
```

### Step 3

Initial Data Inspection

After loading the data, it's important to know what we're working with, so we take an initial look at our DataFrame.

Example:

```shell
# Specify the number of rows to display
iris_df.head(10)

# Inspect the shape of the DataFrame with shape attribute
# The shape is a tuple with count of rows and columns in the DataFrame
iris_df.shape

# Inspect the data types of the columns with dtypes attribute
# The data types are returned as a pandas Series
iris_df.dtypes

# Inspect the data types of the columns with info() method
iris_df.info()
```

### Step 4

Initial Descriptive Statistics

We now look at the summary statistics by using the DataFrame describe() method.

Example:

```shell
# Inspect summary statistics for numerical columns
iris_df.describe()
```

### Step 5 Part 1

Initial Data Distribution for Numerical Columns

We will show some histograms made by using the hist() method.

Example:
```shell
# Inspect histogram by one numerical column
iris_df['sepal_length'].hist()

# Inspect histograms for ALL numerical columns
iris_df.hist()

# Show all plots
matplotlib.pyplot.show()
```
