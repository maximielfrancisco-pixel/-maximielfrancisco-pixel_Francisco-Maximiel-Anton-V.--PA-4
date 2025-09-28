# maximielfrancisco-pixel/maximielfrancisco-pixel_Francisco-Maximiel-Anton-V.--PA-4

------
### 1)  Problem 1: ECE BOARD EXAM PROBLEM
```python    
 # 1.a - FILTERING INSTRUMENTATION STUDENTS FROM LUZON WITH ELECTRONICS > 70
Instru = ECE.loc[
    (ECE['Track'] == 'Instrumentation') &
    (ECE['Hometown'] == 'Luzon') &
    (ECE['Electronics'] > 70),
    ['Name', 'GEAS', 'Electronics']
]
Instru

# 1.b - COMPUTE AVERAGE GRADES AND FILTER MINDAANAO FEMALE STUDENTS
subjects = ['Math', 'Electronics', 'GEAS', 'Communication']
ECE['Average'] = ECE[subjects].mean(axis=1)

Mindy = ECE.loc[
    (ECE['Hometown'] == 'Mindanao') &
    (ECE['Gender'] == 'Female') &
    (ECE['Average'] >= 55),
    ['Name', 'Track', 'Electronics', 'Average']
]
Mindy
```
##### Step-by-Step Procedure of Functions:
#### a. Instru = [“Name”, “GEAS”, “Electronics >70”]
- `_.loc[]` → use to filter rows, it also selects specified columns and rows from the data

Only the Name, GEAS, and Electronics columns are displayed.
#### b. Mindy = [ “Name”, “Track”, “Electronics”, “Average >=55”]
- `subjects = ['']` → this code gathers and defines a list of subjects.
- `ECE[subjects].mean(axis=1)` → Function computes the row-wise average across these subjects

Outcome:
- A table of Instrumentation students from Luzon with Electronics > 70.
- A table of Female Mindanao students with average ≥ 55.
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
- ECE.groupby('Gender')['Average'].mean() calculates the mean average grade per gender. A bar chart is plotted showing average grades by gender.
- ECE.groupby('Hometown')['Average'].mean() calculates mean averages per geographical division. Another bar chart compares average grades by hometown.
- ECE.groupby('Track')['Average'].mean() calculates mean averages per student track.A final bar chart compares average grades by track.
- `gaverage1 = ECE.groupby('Gender/Hometown/Track')['Average'].mean()` → This code groups the dataset by whats needed and calculates the mean of the Average column for each group.
- `plt.figure()` → Creates the size of the length by width
- `plt.bar()` → This Code plots a bar chart with its designated axis, .index for x axis and .values for y axis
- `plt.title()` → This creates the title for the plotted graph
- `plt.xlabel()` → Labeling the x axis to your liking
- `plt.ylabel()` → Labeling the y axis to your liking
- `plt.show()` → Command that tells python to display the graph created
  
Outcome:
- A bar graph by Gender showing the average grades of male vs. female students.
- A bar graph by Hometown showing average grades across Luzon, Visayas, and Mindanao.
- A bar graph by Track showing average grades for different ECE tracks (Instrumentation, Electronics, Communication, etc.).
-------
VER 2 READ ME
