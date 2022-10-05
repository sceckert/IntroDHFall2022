## `Pandas` Cheatsheet: Operations we can peform on DataFrames

### Using string methods to clean or transform data in columns: 

![image](../_images/pusheen-yarn.png)

| **Pandas String Method** | **Explanation**                                                                                   |
|:-------------:|:---------------------------------------------------------------------------------------------------:|
| df['column_name']`.str.lower()`         | makes the string in each row lowercase                                                                                |
| df['column_name']`.str.upper()`         | makes the string in each row uppercase                                                |
| df['column_name']`.str.title()`         | makes the string in each row titlecase                                                |
| df['column_name']`.str.replace('old string', 'new string')`      | replaces `old string` with `new string` for each row |
| df['column_name']`.str.contains('some string')`      | tests whether string in each row contains "some string" |
| df['column_name']`.str.split('delim')`          | returns a list of substrings separated by the given delimiter |
| df['column_name']`.str.join(list)`         | opposite of split(), joins the elements in the given list together using the string                                                                   


### Renaming, adding, dropping columns
![image](../_images/pusheen-bake.png)

| Pandas operation | Explanation |
| :--- |:--- |
|df`.rename(columns={'old_name_of_column': 'new_name_of_column'})` | rename a column (or columns)|
|df`.add(columns='name_of_column')`| add a column |
|df`.drop(columns='name_of_column')`| drop a column |

### Working with missing data
![image](../_images/pusheen-detective.jpg)

| Pandas operation | Explanation |
| :--- | :--- |
| df['column_name']`.isna()` |returns a True/False pairs for each row in a dataframe that is blank|
| df['column_name']`.notna()` |returns a True/False pairs for each row in a dataframe that is **NOT** blank|
| df['column_name']`.fillna()` | will allow you to fill in blank values with a new value |

### Sorting, calculating, and `groupby()`
![image](../_images/pusheen-typing.png)

Note: some of these operations will only be able to run on certain data types (like integers and floats), while others, like `.count()` can help you generate quantitative data about a column of qualitative values (like the number of times a value appears).

| Pandas operation | Explanation |
| :--- | :--- |
|df['column_name']`.count()`| gives you the number of observations, ie the number of rows with non-blank values|
|df['column_name']`.value_counts()` | aggregates the data in a column and counts (cumulatively) each unique value |
|df['column_name']`.sum()` | gives you the sum of values|
|df['column_name']`.mean()` | gives you the mean of values in the column
|df['column_name']`.median()`| median of values|
|df['column_name']`.min()` | gives the minimum value in the column |
|df['column_name']`.max()` |gives the maximum value in the column|
|df['column_name']`.mode()`| gives the mode of the column |
|df['column_name'].`std()`| gives the "unbiased standard deviation" - a statistical term for the estimated dispersion of values| 
|df`.describe(include='all')` | calculates the summary statistics for all columns of the dataframe|
|df`.groupby('column_name')` | allows us to group data and perform calculations on the groups.|

> Note! Pay attention to the difference in syntax between `.describe()`, `.groupby()` and other commands.

