## Introduction

Jupyter notebook provides a web-based application for developing, documenting and executing code.

The main features of Jupyter notebooks are:
- In-browser code editing
- Displaying of the results of computations in-line
- In-browser editing for rich text using the Markdown markup language
- LaTeX syntax integration

## Installation
To install jupyter in your virtual environment, activate it and type:
```sh
pip install jupyter
```

## Running Jupyter

### Locally
To run Jupyter on your local machine, go to a folder you want to create your notebook in and type:
```sh
jupyter notebook
```
This will open a new tab in your browser and display the so-called Notebook Dashboard, where you can manage existing notebooks:
![Notebook Dashboard](https://github.com/text-machine-lab/uml_nlp_class_2019/blob/master/screenshots/dashboard.png "Notebook Dashboard")
The Dashboard will only let you see and edit files located only within your startup directory, so make sure to start Jupyter in the correct folder.

### Remotely
Because Jupyter is a server-client-based web application, it is possible to launch it on a remote machine. 
By default, a notebook server starts locally on port `8888` using the same command:
```sh
jupyter notebook
```
You can change the port specifying the `-p` flag as follows:
```sh
jupyter notebook --port <port_number>
```
Once the Jupyter Notebook application is started, you can use SSH tunneling to connect to it.
To establish your own SSH tunnel, run the following command:
```sh
ssh -L 8000:localhost:8888 your_login@your_server_ip
```
Here `8000` is the port on your local machine and `8888` is the port on the remote server where you are running Jupyter.
If one of your local applications is already using the port `8000`, feel free to change it to a different one. 
Once you have forwarded the port, you can copy the URL from your remote server's terminal output and paste it into your browser's address bar.
At this step you should be able to see the Notebook Dashboard.

## Getting started
To create a new notebook, click __New__->__Python 3__ at the top right of the Dashboard as in the screenshot:
![New notebook](https://github.com/text-machine-lab/uml_nlp_class_2019/blob/master/screenshots/new_notebook.png "New notebook")

## Interface
The interface of the jupyter notebook is pretty self-explanatory; however, we will cover the main functionality here.
In general, there are two modes of the notebook operation, _Command Mode_ and _Edit Mode_. The former is used for navigation between cells (see below), changing their order or type, and running the notebook while the latter is used for modification of a given cell's content.
The notebook consists of compuеational units called cells, every single cell has either a `Code` or a `Markdown` type. You can switch between the two types by going to `Cell Type` under the `Cell` menu:
![Cell types](https://github.com/text-machine-lab/uml_nlp_class_2019/blob/master/screenshots/cell_types.png "Cell types")
You can select, copy, insert, delete, move, execute and edit cells using the toolbar at the top or using shortcuts (see below).

To execute a single cell, press `Ctrl+Enter`. To edit a cell, press `Enter`.
If you are editing a markdown cell, you should see how the markdown content is rendered after the execution (lists, formulas, headers, etc.):
![Markdown cell](https://github.com/text-machine-lab/uml_nlp_class_2019/blob/master/screenshots/markdown_cell.png "Markdown cell execution")

If you are editing a code cell, you can see the output that your code produces right after you execute the cell:
![Code cell](https://github.com/text-machine-lab/uml_nlp_class_2019/blob/master/screenshots/code_cell.png "Code cell execution")

## Shortcuts
Perhaps the easiest and fastest way to edit jupyter notebooks is to use various shortcuts. 
We will list the most commonly used ones. If you want to quickly look a shortcut up, press `H` when in Command Mode to see a full table of shortcuts.

Command Mode shortcuts:
- Enter the Edit Mode: `Enter`
- Change the cell mode to markdown: `M`
- Change the cell mode to code: `Y`
- Add a cell below/above: `B`/`A`
- Delete a cell: press `D` two times

Edit Mode shortcuts:
- Enable the Command Mode: `Esc`
- Run a cell: `Ctrl+Enter`
- Run a cell and insert another one below: `Shift+Enter`
- Fetch a docstring of a python function: `Shift+Tab`
- Comment: `Ctrl+/`
- Indent/dedent: `Ctrl+]`/ `Ctrl+[`
- Delete the whole line: `Ctrl+D`
- To hide the output of the cell, double-click on it

For the full documentation please refer to [https://jupyter-notebook.readthedocs.io/en/stable/](https://jupyter-notebook.readthedocs.io/en/stable/)
