# Lab 2: Anaconda , VS Code, and Python Practice

## 1. Anaconda virtual environment 
If you haven't already done so, create a virtual environment for our class.  The instructions below are for using conda, but you are free to use any environment managers (though the TAs and I are most familiar with conda).  Type (or copy and paste) the following commands in order (and one at a time) in the terminal or Anaconda prompt.  Type `y` when you are asked if you want to proceed after each command.

*Note: In (1.), the conda environment that I am using is called "classes24".  Feel free to use any environment name that makes the most sense for you. 

1. Create the environment

    ```conda create --name classes24 python beautifulsoup4 hdf5 html5lib ipykernel jupyter ipython matplotlib matplotlib-inline nltk notebook numpy openpyxl pandas pillow requests scikit-learn scrapy seaborn scipy statsmodels plotnine streamlit plotly```

2. Activate the environment you just created:

    ```conda activate classes24```

3. Install other packages from conda forge

    ```conda install -c conda-forge selenium pingouin webdriver-manager```  


## 2. VS Code
1. Install the following extensions.  To install an extension, click on the "Extensions" icon on the left most toolbar, search for the extension name in the search bar, and click the "Install" button.  
    * GitHub Pull Requests and Issues
    * Python (by Microsoft)
    * Jupyter (by Microsoft)
2. Sign into GitHub through VS Code by clicking on the "GitHub" icon on the left most toolbar and clicking "Sign in".
3. When you run a .ipynb file, choose the kernel (top right) to be the "classes24" environment.  When you run a .py file, you specify the kernel on the bottom right. 



## 3. Python review questions.

* When you accepted the assignment in GitHub Classroom, a repository named `lab-02` will be automatically generated for you under the "stat386-Fall2024" organization.
* Your personal repository for this homework can be found at `https://github.com/stat386-Fall2024/lab-02-your_user_name`.
* *Clone the Repository*: 
    - Open your terminal and navigate to the directory where you want to download the repository.
    - Run `git clone [your repository URL]` to clone the repository onto your local machine.
* The cloning process will create a new directory named `lab-02-your_user_name`. Ensure that you perform all your work inside this directory.
* As you work on the assignment, remember to commit your changes periodically. You can easily do this using Visual Studio Code (VS Code).
* If you've cloned the repository correctly and are working within the created directory, the remote link to your GitHub repository should already be configured.
* *File and Function Names*: 
    - Place all functions for this lab in a file named `lab2.py`.
    - Inside `lab2.py`, you'll find functions with `pass` statements. Replace `pass` with your own code.
    - It might be easier to write and test your functions using an .ipynb and then copy your working function to the `lab2.py` file when it is finished.
    - **Do not** change the names of the functions or the file.
    - You are free to include other `.py` or `.ipynb` files with your work. However, ensure that `lab2.py` only contains your final code for each function.

* *Submitting on Gradescope*: 
    - Once you've completed the assignment, go to Gradescope and select your personal homework repository (`https://github.com/stat386-Fall2024/lab-02-your_user_name`) as the source for your submission.
    

 NOTE:  
* In Problems (1) - (7), the output should be returned (that is, use a `return` statement).  The output should NOT be printed (that is, DON'T use a `print` statement.
* In Problem (8), the output should be PRINTED (use a `print` statement) and NOT returned (don't use a `return` statement).  

**1.  Write a Python function that will compute the Euclidean distance between any two points.  The function should accept as input two tuples in the form of ((x<sub>1</sub>, y<sub>1</sub>),(x<sub>2</sub>, y<sub>2</sub>)) and return the Euclidean distance.** Be sure the function *returns* the output (rather than *prints* the output).

*Example output:*

```
In [1]: euclid_dist((1,3),(7,11))
out[1]: 10
```

-----
**2. Write a Python function that computes the value of ``n + nn + nnn`` where ``n`` is an integer.  For example if,  ``n=2``, the function should return ``246`` (which is the sum of 2+22+222).**  Be sure the function *returns* the output (rather than *prints* the output).

*Example output:*

```
In [1]: sum_ns(2)
Out[1]: 246
```

-----
**3. Write a Python function that determines if ``n`` is a perfect square, where ``n`` is an integer.  The function return either "False" or "n is a perfect square of x"  (where ``n`` and ``x`` are appropriate for the input).** Be sure the function *returns* the output (rather than *prints* the output).

*Example output:*

```
In [1]: perfect_square(24)
Out[1]: False

In [2]: perfect_square(25)
Out[2]: 25 is a perfect square of 5
```

----
**4. Write a Python function that checks whether a string is a palindrome or not.  A palindrome is a word or phrase that reads the same forwards and backwards (ignoring spaces), such as "madam" or "nurses run".** Be sure the function *returns* the output (rather than *prints* the output).

*Example output:*

```
In [1]: is_palindrome('madam')
Out[1]: True

In [2]: is_palindrome('nurses run')
Out[2]: True

In [3]: is_palindrome('starlight')
Out[3]: False
```

----
**5. Write a Python function that accepts a string and calculates the number of upper case letters, the number of lower case letters, and the number of spaces.  The function should return a dictionary where the keys are "upper", "lower", and "space" and the value is the number of occurrences.  See the example output below.**    Be sure the function *returns* the output (rather than *prints* the output).
(Hint:  check out what methods are available for strings.)  

 *Example output:*

```
In [1]: count_letter_types("HELLO!! How are you today?")
Out[1]: {'upper': 6, 'lower': 13, 'space': 4}

```


----
**6. Write a Python function that accepts a string a returns a dictionary where the key word is a word length and the value is a list of all the words that are that word length.  See the example output below.**  Be sure the function *returns* the output (rather than *prints* the output).

*Example output: (note, it's okay if the keys of your dictionary are in a different order)*

```
In [1]: s = "It is a truth universally acknowledged that a single man in possession of a good fortune must be in want of a wife"

In [2]: count_word_lengths(s)

Out[2]: {1: ['a', 'a', 'a', 'a'],
         2: ['It', 'is', 'in', 'of', 'be', 'in', 'of'],
         3: ['man'],
         4: ['that', 'good', 'must', 'want', 'wife'],
         5: ['truth'],
         6: ['single'],
         7: ['fortune'],
         10: ['possession'],
         11: ['universally'],
         12: ['acknowledged']}
```


----
**7.  Write a python function that accepts an integer `n` (where 2 $\le$ `n` $\le$ 9) and returns a list of all the numbers between 0 and `n`00 that have an `n` in them AND are divisible by `n`. The function should produce the message `Invalid input: enter a number between 2 and 9` if an invalid number is used. See the example output below.**  Be sure the function *returns* the output (rather than *prints* the output).

```
In [1]: n_list(3)
Out[1]: [3,
         30,
         33,
         36,
         39,
         63,
         ...
         300]

In [2]: n_list(10)
Out[2]: "Invalid input: enter a number between 2 and 9"
```


---
**8. Write a Python function that takes a list of numbers as input and calculates the sum of all even numbers in the list. Additionally, find the maximum value among these even numbers and determine how many times it appears in the list. Finally, print both the sum and the maximum value along with its frequency. See the example output below.**  For this problem only, the output should be *PRINTED* (rather than *RETURNED*).


```
In [1]: evens_mean_max([1,2,3,4,5,6])
Out[1]: The sum of the even numbers is 12.
        The maximum of the even numbers is 6 and it appears 1 time(s) in the list.

In [2]: evens_mean_max([1,7,2,3,7,4,5,6,7,6])
Out[2]: The sum of the even numbers is 18.
        The maximum of the even numbers is 6 and it appears 2 time(s) in the list.
```




