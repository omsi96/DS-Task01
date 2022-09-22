# Task 01 - Introduction to Pandas

For this task, we will go through a simple **Fruit Dataset** and use **Pandas** to display the different Fruit types (apple, mandarin, orange, and lemon) in our dataset.

## Import required modules


```python
!pip install pandas
```

    Requirement already satisfied: pandas in c:\programdata\anaconda3\lib\site-packages (1.3.4)
    Requirement already satisfied: pytz>=2017.3 in c:\programdata\anaconda3\lib\site-packages (from pandas) (2021.3)
    Requirement already satisfied: numpy>=1.17.3 in c:\programdata\anaconda3\lib\site-packages (from pandas) (1.20.3)
    Requirement already satisfied: python-dateutil>=2.7.3 in c:\programdata\anaconda3\lib\site-packages (from pandas) (2.8.2)
    Requirement already satisfied: six>=1.5 in c:\programdata\anaconda3\lib\site-packages (from python-dateutil>=2.7.3->pandas) (1.16.0)
    


```python
import pandas as pd
```

## First Things First: Look at Your Data

### Question 0

Using a DataFrame can help make many things easy with less code, so let's practice creating a classifier with a pandas DataFrame.

**Using `read_table`, create a dataframe and keep in mind that the dataset file `data.txt` should be in the same folder as your python file.**


```python
# creating dataframe

fruits = pd.read_table('data.txt')
```

### Question 1

How many data points (**Number of Instances**) and features (**Number of Attributes**) does the fruit dataset have?


```python
# dataframe.shape returns dimensionality (number of Instances and Attributes) 59 (instances) and 7 (attributes)

print(fruits.shape)
```

    (59, 7)
    

### Question 2
What is the class distribution? (i.e. how many instances of `apple`(encoded 1), `mandarin`(encoded 2), `orange`(encoded 3), and `lemon`(encoded 4))


```python
apple = int(fruits[fruits['fruit_label'] == 1]['fruit_label'].count())
mandarin = int(fruits[fruits['fruit_label'] == 2]['fruit_label'].count())
orange = int(fruits[fruits['fruit_label'] == 3]['fruit_label'].count())
lemon = int(fruits[fruits['fruit_label'] == 4]['fruit_label'].count())

result = pd.Series({'apple': apple, 'mandarin': mandarin, 'orange': orange, 'lemon': lemon})

print(result)
```

    apple       19
    mandarin     5
    orange      19
    lemon       16
    dtype: int64
    

### Question 3

Using `head` display the first 8 instancs of the fruit dataset.


```python
fruits.head(8)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>fruit_label</th>
      <th>fruit_name</th>
      <th>fruit_subtype</th>
      <th>mass</th>
      <th>width</th>
      <th>height</th>
      <th>color_score</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>apple</td>
      <td>granny_smith</td>
      <td>192</td>
      <td>8.4</td>
      <td>7.3</td>
      <td>0.55</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>apple</td>
      <td>granny_smith</td>
      <td>180</td>
      <td>8.0</td>
      <td>6.8</td>
      <td>0.59</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1</td>
      <td>apple</td>
      <td>granny_smith</td>
      <td>176</td>
      <td>7.4</td>
      <td>7.2</td>
      <td>0.60</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2</td>
      <td>mandarin</td>
      <td>mandarin</td>
      <td>86</td>
      <td>6.2</td>
      <td>4.7</td>
      <td>0.80</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2</td>
      <td>mandarin</td>
      <td>mandarin</td>
      <td>84</td>
      <td>6.0</td>
      <td>4.6</td>
      <td>0.79</td>
    </tr>
    <tr>
      <th>5</th>
      <td>2</td>
      <td>mandarin</td>
      <td>mandarin</td>
      <td>80</td>
      <td>5.8</td>
      <td>4.3</td>
      <td>0.77</td>
    </tr>
    <tr>
      <th>6</th>
      <td>2</td>
      <td>mandarin</td>
      <td>mandarin</td>
      <td>80</td>
      <td>5.9</td>
      <td>4.3</td>
      <td>0.81</td>
    </tr>
    <tr>
      <th>7</th>
      <td>2</td>
      <td>mandarin</td>
      <td>mandarin</td>
      <td>76</td>
      <td>5.8</td>
      <td>4.0</td>
      <td>0.81</td>
    </tr>
  </tbody>
</table>
</div>


