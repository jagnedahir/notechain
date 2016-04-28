# Data Science Daily Discoveries

This is a daily diary to keep me focussed and moving. 
Every day I will upload something related to learning Python, git and other 
tools useful for data science. 

I'm using the [IPython Notebook](http://ipython.org) the Anaconda (2.4.1) 
Python (2.7.11) distribution.


### Links to each day:

**Day 1**                                                                 
I learned some [git commands](001-git-basics.md) and [played around 
with some data](pandas-notebooks-csv/001-LendingClub.ipynb) in ipython using 
the data frames (df) in pandas library. 
`df.columns(), df.index(), df.dtypes()`

-------------

**Day 2**                                                                       
                                               More pandas practise 
[here](pandas-notebooks-csv/002-LendingClub.ipynb). Re-discovered the 
usefulness of cheatsheats. Now have a number of functions for exploring the 
data.    
```df.head(), df.unique(), df.describe(), df.iloc(), df.count(), 
df.isin(), np.where()```

---------------

**Day 3**  
%timeit : time how long a command takes to run.  
More pandas practise [here](pandas-notebooks-csv/003-LendingClub.ipynb).   
`df.dropna(), df.isnull(), df.any(), df.sum()`

----------------

**Day 4**  
If you remove from local directory you must do this before the changes will be 
made on the remote repository:   
`git rm filename`
`git commit -m "message"`
`git push`

I made [this](http://learnpythonthehardway.org/book/ex50.html) work, only after 
working out (google useless!) where to put a line continuation in 
index.html  
`$if greeting:
    I just wanted to say <em style="color: green; font-size: 
2em;">$greeting</em>.`

Did not fit in one line in my editor. When I shortened it to one line it 
worked. An \ was needed between the message and the html emphasized text.

```$if greeting:
    I just wanted to say \    
<em style="color: green; font-size: 2em;">$greeting</em>.```

Started [plotting the data](pandas-notebooks-csv/004-LendingClub.ipynb) with  
`df.plot(kind = 'box'), df.hist() and scatter_matrix(df)`

To suppress the printing of the object before a panel of plots
`_ = df.hist()` etc.

----------------

**Day 5**
Notebook found [here](pandas-notebooks-csv/004-LendingClub.ipynb).  
Removed % signs and "months" and converted the rest into a number.  
Removed null values with `df.dropna()`. Can investigate the rows with these 
null values by saving them in a new df.  
Removed data above the 95th percentile by using conditional statements for each 
column. There must be a cleaner way to do it than this:

`no_outliers = nonan[(nonan[columns[0]] < p[0]) & (nonan[columns[1]] < p[1]) &
(nonan[columns[2]] < p[2]) & (nonan[columns[3]] < p[3]) & (nonan[columns[4]] < 
p[4]) & (nonan[columns[5]] < p[5])]` 
  
Saved no_outliers as a new dataframe and then a csv using `to_csv()`. 
Eyeballed the difference before/after cleaning with a subset of columns in 
`scatter_matrix`

`df.count()` only returns non-nans.




----------------


