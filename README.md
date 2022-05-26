# Jupyter Physical Science Lab Suite (JPSL)
Documentation for the Jupyter Physical Science Lab Suite of Packages.

[Introduction](#introduction) | [Try It](#try-it) | [Quick
Start](#quick-start) | 
[Packages](#packages) | [Packages being 
considerd](#packages-being-considered) | 
[JPSL Project Repository](https://github.com/JupyterPhysSciLab) | 
[JPSL Documentation Repository](https://github.com/JupyterPhysSciLab/Documentation) | 
[License](#this-software-is-distributed-under-the-gnu-v3-licensehttpsgnuorglicenses)

# Introduction

The key goals of this suite of packages is to provide:

1. an open source electronic laboratory notebook that is practical in physical
   science laboratories where data is collected by hand, from instrumentation
   and sensors;
2. the ability to run on minimal hardware (things like the Raspberry Pi) to
   make it affordable for educational use;
3. adaptability, allowing for use in a variety of teaching situations;
4. GUI elements that allow students in introductory courses without programming
   experience to collect data and analyze it;
5. tools for instructors allowing them to create worksheets or more open-ended
   assignments (there is some potential feature overlap
   with [nbgrader](https://github.com/jupyter/nbgrader), but nbgrader tools are
   aimed more at math and programming assignments);
6. ability to generate compact pdf formatted "reports" for grading;
7. easy ways to have students analyze data while properly tracking units and
   what analysis was done, thus facilitating grading and trouble-shooting of
   student work.

There are two basic flavors of this suite of packages: student; and instructor.
The instructor flavor includes tools for generating content in worksheets that
students cannot edit. As well as ways to control what is displayed to the 
students and in the final version submitted for grading. The student version 
purposely leaves out the tools that
allow unlocking of locked cells in a notebook, so that the instructor can
include unchanging instructions, examples and questions.

# Try it

You can try the parts of Jupyter Physical Science lab without installing 
anything. The packages can be run in the cloud. Links to do this are 
provided on the Github pages for each package. It is recommended that you 
start with [JPSLInstructor](https://github.com/JupyterPhysSciLab/JPSLInstructor),
which includes all the supported packages.

# Quick Start

1. Install python on your machine, if necessary.
    1. Check current system python install by opening a command line 
       terminal and issuing the command `python3 --version`. If it is >= 3.
       7 you can use it. Otherwise, follow the next step to install a 
       newer version.
    2. Get the installer for your computer from [python.org](https://python.org).
   Follow the instructions for installing on your system.
2. Install a tool for managing and using virtual environments. This 
   allows you to have multiple independent sets (virtual environments)
   of python packages installed.
   1. I recommend you use this so that you can have both an "instructor"
   and "student" environment for testing.
   2. I personally like using [pipenv](https://pipenv.pypa.io/en/latest/).
   You can install it using the command `pip3 --user install pipenv`. On 
      Windows you will probably have to do `python3 -m pip --user install 
      pipenv`.
   See the website for more information.
3. Set up an instructor work environment.
   1. Create a directory to contain your virtual environment and navigate 
      into it (in *nix: `cd path-to-directory`).
   2. Create the empty virtual environment `pipenv shell` (on Windows 
      `python3 -m pipenv shell`). This will
       create the environment, activate it and leave you inside it. 
      **WARNING**: 
      on Windows I have seen it move you to another directory. If it does 
      this navigate back using the `cd` command. 
   3. Still within the environment use pip to install the [JPSLInstructor 
      pseudo package](https://github.com/JupyterPhysSciLab/JPSLInstructor)
   `pip install JPSLInstructor`. This will take a while 
      to run. There are a lot of packages to download and install.
   4. Example notebooks are not installed by pip. You should download the 
      [JPSLInstructor pseudo package](https://github.com/JupyterPhysSciLab/JPSLInstructor)
   as a zip file and extract the `Examples` folder into the directory for this
   virtual environment.
   5. To work with the software launch the jupyter notebook with the 
      command `juptyer notebook`. This will launch a local jupyter server 
      on your machine and open a page connected to it in your web browser 
      (Chrome and Firefox work best).
   6. Open an example notebook to try things.
   7. After quiting the Jupyter notebook server you can exit the virtual 
      environment with the command `exit`.
4. Set up a student work environment for testing.
   1. Create a directory to contain your virtual environment and navigate 
         into it (in *nix: `cd path-to-directory`).
   2. Create the empty virtual environment `pipenv shell`. This will
       create the environment, activate it and leave you inside it. 
   3. Still within the environment use pip to install the [JPSLStudent 
      pseudo package](https://github.com/JupyterPhysSciLab/JPSLStudent)
   `pip install JPSLStudent`. This will take a while 
      to run. There are a lot of packages to download and install.
   4. To work with the software launch the jupyter notebook with the 
      command `juptyer notebook`.
   5. Copy notebooks you want to see from a student perspective into this 
      directory.
   6. After quiting the Jupyter notebook server you can exit the virtual 
      environment with the command `exit`.

# Packages
(Currently in beta, please try and send feedback)

The packages are available from PyPi (using pip for installation) or by
installing from these repositories. The packages are broken up to allow using
only the tools necessary.

* [*jupyter-datainputtable*](https://github.com/JupyterPhysSciLab/jupyter-datainputtable)
  provides tools for generating a GUI table into which data can be typed and
  the data will survive clearing of the cell outputs from a notebook.
* [*jupyter-instructortools*](https://github.com/JupyterPhysSciLab/jupyter-instructortools)
  provides menu based tools for locking and unlocking text (Markdown) and code
  cells, inserting tables, some boilerplate language, etc.
* [*jupyter-pandas-GUI*](https://jupyterphysscilab.github.io/jupyter_Pandas_GUI/)
  provides jupyter widget based GUI code composers for tasks such as 
  calculating a new column in a Pandas DataFrame or making a scatter or line 
  plot from data in a DataFrame.
* [*JupyterPiDAQ*](https://jupyterphysscilab.github.io/JupyterPiDAQ/) provides
  menu based tools for interactive data collection using A/D boards and
  visualization of that data, presently only supports specific boards attached
  to Raspberry Pi 3B+ and above.
* *[Algebra_with_SymPy](https://gutow.github.io/Algebra_with_Sympy/)* provides
  a definition for an equation with a lhs and a rhs. This tool applies
  operations to both sides of the equation simultaneously, just as students are
  taught to do when attempting to isolate (solve for) a variable. Thus the
  statement `Equation/b` yields a new
  equation `Equation.lhs/b = Equation.rhs/b`.
* **Pseudo Packages**
    * [*JPSLInstructor*](https://github.com/JupyterPhysSciLab/JPSLInstructor) 
      contains all the packages.
    * [*JPSLStudent*](https://github.com/JupyterPhysSciLab/JPSLStudent) 
      contains everything but the InstructorTools package.

# Packages being considered
These are packages that are under development elsewhere, but might be included
if there is interest:

* [*DeltaSymbol*](https://github.com/gutow/DeltaSymbol) allows adding a symbol
  in SymPy that displays as the typeset &Delta;`X` in Jupyter notbooks. Where
  &Delta;`X` is the common abbreviation for `final(X) - initial (X)`.
* [*jupyter-wysiwyg*](https://github.com/genepattern/jupyter-wysiwyg) provides
  a what you see is what you get mode for Markdown/Richtext cells activated by
  clicking a button.
* [*snippets menu*](https://github.com/moble/jupyter_boilerplate). The JSON 
  definitions of some menu entries to initialize JPSL tools are available 
  [here](./Snippet_Menu_JSON.md).
* *WYSIWYGcell* provides what you see is what you get text edit cells in
  Jupyter notebooks, but involves significant changes to the Jupyter notebook
  code, thus will either require providing a fully custom Jupyter notebook or
  monkey patching a current installation.
* *SimpleUnits* provides symbols for standard physical units usually
  encountered at the undergraduate level in the physical sciences. This just
  defines the symbols so that they can by used in sympy expressions, the
  students are expected to worry about unit conversions themselves.

##### [This software is distributed under the GNU V3 license](https://gnu.org/licenses)
This program is free software: you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation, either version 3 of the License, or
    (at your option) any later version.
    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

Copyright - Jonathan Gutow, 2021, 2022.