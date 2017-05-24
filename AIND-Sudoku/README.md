# Artificial Intelligence Nanodegree
## Introductory Project: Diagonal Sudoku Solver

# Question 1 (Naked Twins)
Q: How do we use constraint propagation to solve the naked twins problem?  
A: Constraint propagation is a technique that uses restrictions of a given puzzle i.e. row, column and box requirments in sudoku to contatin only one instance of a digit from 1 to 9. In our instances CP is used recursively to decrease the number of possibilities for a given box. Now given a naked twins problem and the strategy behind, we use naked twins to reduce possibilities even further by removing the twins' digits from peers of both twins. Since naked twins has been added into recusrsion now, the next run of `reduce_puzzle()` might be able to expose further possibility reduction and problem may thus be solved.  

# Question 2 (Diagonal Sudoku)
Q: How do we use constraint propagation to solve the diagonal sudoku problem?  
A: All diagonal sudoku does, in comparison to an unmodified version of the game, is it adds another constraint, whereby besides normal constraints, digits have to abide to diagonal restraints i.e. a single instance of a 1-9 digit. Constraint propagation is not used in any different way in comparison to an unmodified puzzle. However, we do add diagonal units to our `unitlist`, such that `unitlist = row_units + column_units + square_units + diagonal_units`. New unitlist variable makes an algorith assume this new constraint to solve diagonal sudoku. 

### Install

This project requires **Python 3**.

We recommend students install [Anaconda](https://www.continuum.io/downloads), a pre-packaged Python distribution that contains all of the necessary libraries and software for this project. 
Please try using the environment we provided in the Anaconda lesson of the Nanodegree.

##### Optional: Pygame

Optionally, you can also install pygame if you want to see your visualization. If you've followed our instructions for setting up our conda environment, you should be all set.

If not, please see how to download pygame [here](http://www.pygame.org/download.shtml).

### Code

* `solution.py` - You'll fill this in as part of your solution.
* `solution_test.py` - Do not modify this. You can test your solution by running `python solution_test.py`.
* `PySudoku.py` - Do not modify this. This is code for visualizing your solution.
* `visualize.py` - Do not modify this. This is code for visualizing your solution.

### Visualizing

To visualize your solution, please only assign values to the values_dict using the ```assign_values``` function provided in solution.py

### Submission
Before submitting your solution to a reviewer, you are required to submit your project to Udacity's Project Assistant, which will provide some initial feedback.  

The setup is simple.  If you have not installed the client tool already, then you may do so with the command `pip install udacity-pa`.  

To submit your code to the project assistant, run `udacity submit` from within the top-level directory of this project.  You will be prompted for a username and password.  If you login using google or facebook, visit [this link](https://project-assistant.udacity.com/auth_tokens/jwt_login for alternate login instructions.

This process will create a zipfile in your top-level directory named sudoku-<id>.zip.  This is the file that you should submit to the Udacity reviews system.

