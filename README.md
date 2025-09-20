# maximielfrancisco-pixel/maximielfrancisco-pixel_Francisco-Maximiel-Anton-V.--PA-4

------
### 1)  Problem 1: ECE BOARD EXAM PROBLEM
```python    
  (ECE['Track'] == 'Instrumentation') &
    (ECE['Hometown'] == 'Luzon') &
    (ECE['Electronics'] > 70),
    ['Name', 'GEAS', 'Electronics']

  subjects = ['Math', 'Electronics', 'GEAS', 'Communication']
    ECE["Average"] = ECE[subjects].mean(axis=1)
```
##### Step-by-Step Procedure of Functions:
#### a. Instru = [“Name”, “GEAS”, “Electronics >70”]
- `_.loc[]` → use to filter rows, it also selects specified columns and rows from the data
#### b. Mindy = [ “Name”, “Track”, “Electronics”, “Average >=55”]
- `subjects = ['']` → this code gathers and defines a list of subjects.
- `ECE[subjects].mean(axis=1)` → Function computes the row-wise average across these subjects

------

### 2) Problem 2: VISUALIZATION FOR SPECIFIC HIGHER AVERAGE
```python
   plt.figure(figsize=(4,4))
  plt.bar(gaverage.index, gaverage.values)
  plt.title('Average Comparison (Gender)')
  plt.xlabel('Gender')
  plt.ylabel('Average Grade')
  plt.show()
```
##### Step-by-Step Procedure of Functions: 
- `gaverage1 = ECE.groupby('Gender')['Average'].mean()` → This code groups the dataset by whats needed and calculates the mean of the Average column for each group.
- `plt.figure()` → Creates the size of the length by width
- `plt.bar()` → This Code plots a bar chart with its designated axis, .index for x axis and .values for y axis
- `plt.title()` → This creates the title for the plotted graph
- `plt.xlabel()` → Labeling the x axis to your liking
- `plt.ylabel()` → Labeling the y axis to your liking
- `plt.show()` → Command that tells python to display the graph created
- ------
