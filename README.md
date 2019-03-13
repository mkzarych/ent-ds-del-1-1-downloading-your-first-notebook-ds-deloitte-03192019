
# Downloading Your First Jupyter Notebook - Lab


## Introduction
In this lesson, we'll practice forking and cloning a lesson and then opening and working with a Jupyter Notebook - the main tool you will be using for writing Python scripts.

## Objectives
You will be able to:
* Fork (copy) and clone (download) projects from GitHub to work on as part of this course
* Open a Jupyter Notebook from your terminal window
* Make changes to, and run the code in a Jupyter Notebook
* Save your changes and upload them to GitHub

## Working Locally
You might have noticed that the title of this lesson includes "- Lab". That means you are going to be working on this project locally - on your laptop - not just reading it via Learn in your browser online.

Remember the flow for downloading a lesson? First you need to **fork** it (make your own copy on GitHub), then you **clone** it (downloading a copy from GitHub to your local laptop). Once you have the files on your computer, you can then open the **Jupyter Notebook** file (it has a file extension of `.ipyn`) locally and start working with it. Let's go through the process together.

### Forking and Cloning the Lesson
* Start by clicking on the GitHub icon on the Learn page for this lesson
* That will take you to GitHub. Click on the "Fork" button in the top right to make your own copy of this lesson on GitHub
* Once you've forked, you need to clone the lesson (download a copy to your local computer)
* To do that, copy the URL of the repository in your browser window, then in the Git Bash terminal window, type `git clone` followed by the URL. So it should be something like `git clone https://github.com/learn-co-students/ent-ds-del-1-1-downloading-your-first-notebook-ds-deloitte-03192019`

### Opening the Jupyter Notebook
Now that you've downloaded the files, you need to be able to open the notebook.
* Change directory into the newly downloaded directory (in Git Bash, type `cd ent` followed by hitting the tab key to "tab complete" and then the enter key to run the command)
* type `jupyter notebook` into Git Bash and a browser window will pop up with a list of files
* In the browser, click on the `index.ipynb` file and congratulations, you're now running a Jupyter Notebook file locally. You're going to be doing a lot of that over the next few weeks!

### A Brief Introduction to Jupyter Notebooks
Jupyter Notebooks are a web based text editor, popular amongst data scientists for creating documents that contain code and comments - and sometimes the output from the code as well (tables, charts, etc). It turns out that they are a very convenient way for writing, exploring and documenting code for working with data.

#### Introduction to cells
Each Jupyter Notebook is comprised of a number of cells. Double click on this content to see what I mean. Once we double click on a cell, we are in **insert mode**. This means that we are able to edit the cells, just like you would if this were a word document. We can tell that we are in insert mode because of the green border around the cell.  

After entering insert mode for this cell, change some content. Don't worry about what you change as we can always undo it. We can revert our changes to a cell by making sure that we are still in insert mode and by pressing `control + z`.

To get out of insert mode and see the effect of our changes, press `shift + enter`.

#### Types of Cells

The current cell and every other cell in this lesson has been a **markdown cell**, meaning that it allows us to write and style text. For example, if you surround some text with two asterisks (`**`) on both sides, the text **becomes bold**. That's markdown.

Cells can also have a type of code. If we are writing in a cell that is for Python code, everything in that cell must be valid Python or we will see an error.


```python
This is a python cell without valid Python so we will see an error if we run it
```

So, a cell must either be of type markdown or of type code, in which case all of the contents must be valid Python.  It cannot be both. We can quickly change a cell from markdown to code with some keyboard shortcuts.

From escape mode, we change a cell to type code by pressing the letter `y`.
From escape mode, we change a cell to type markdown by pressing the letter `m`.

Anytime we create a new cell, say with the shortcut key `b`, the new cell will default to code mode.  We can switch to escape mode and press the letter `m` to change the cell from code to markdown.

**Press the key `h` while in escape mode to view the menu for all of Jupyter's shortcuts.**

### Working with Python in Jupyter

Ok, now that we know a little bit about cells, let's focus on working with Python in Jupyter.  The main takeaway is this: if we see a Python (code) cell, to run that code, we should press `shift + enter` on that cell. 

The major gotcha in working with Python code is that we must execute the cells in order for Python to register the code in them. So for example, just seeing the cell where we define `name` to `'bob'` below does not write that cell to memory.


```python
name = 'bob'
```

If we try to reference that variable later on without having executed the cell, Python will tell us that it is not defined.

To execute or run a cell, we must press `shift + enter` on that cell (or when that cell is selected). Upon running a cell, Python will show the the last line of the cell's return value underneath.  Let's run the cell below to see this:


```python
age = 14
age
```

As you can see the variable `age` is set to 14, so when the cell is run `14` is displayed underneath.


### Saving Your Changes
There are a few steps you need to remember to complete to save and back up your changes. Let's go through the process to introduce it to you.
* Firstly, make a change to this document. Double click on one of the calls, and add some new text. It doesn't matter what it says.
* To save that change to disk, in Jupyter Notebook, select the `File - Save and Checkpoint` menu option
* Now go back to your terminal window. You'll have to hit `control-z` to stop Jupyter Notebook running.
* Then type `git status -s` in the terminal window. You should see a response of `M index.ipynb` which is telling us that the index.ipynb (the Jupyter Notebook file we were working on) has been Modified.
* To save the changes into the Git version control system type `git add .` and then `git commit -m "My changes"`
* To save those changes to GitHub, you need to type `git push` to push your changes up to GitHub


## Summary

Congratulations! In this lesson, you practiced forking and cloning a repository, you learned how to open a Jupyter Notebook file from the terminal, and how to save your changes to disk, add them to Git, and upload them to GitHub so you have a backup of your work in case your laptop dies or you need to access it from another computer! 

Next up, lets learn a little more about variables . . .

