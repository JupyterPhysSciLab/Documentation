# Documentation
Documentation for the Jupyter Physical Science Lab Suite of Packages

# Introduction
The key goals of this suite of packages is to provide:
1. an open source electronic laboratory notebook that is practical in physical science laboratories where data is collected by hand, from instrumentation and sensors;
1. the ability to run on minimal hardware (things like the Raspberry Pi) to make it affordable for educational use;
1. adaptibility for teaching;
1. GUI elements that allow students in introductory courses without programming experience to collect data and analyze it;
1. tools for instructors allowing them to create worksheets or more open ended assignments (there is some potential feature overlap with nbgrader[https://github.com/jupyter/nbgrader], but nbgrader tools are aimed more at math and programming assignments.)
1. easy ways to have students analyze data while properly tracking units and what analysis was done, thus facilitating grading and trouble shooting of student work.

There are two basic flavors of this suite of packages: student; and instructor. The instructor flavor includes tools for generating content in worksheets that students cannot edit. The student version purposely leaves out the tools that allow editing of any cell in a notebook, so that the instructor can include unchanging instructions, examples and questions.

# Packages
The packages will eventually be available from PyPi (using pip for installation). Presently, they are only available from these repositories. The packages are broken up to allow using only the tools necessary.
* _DataTable_ provides tools for generating a GUI table into which data can by typed and the data will survive clearing of the cell outputs from a notebook.
* _InstructorTools_ provides tools for locking and unlocking text (Markdown) and code cells. The locking does not prevent clearing of cell outputs created by running a cell, just the editing of the content of these cells.
* _JupyterPiDAQ_ provides tools for interactive data collection using A/D boards, presently only supports specific boards attached to Raspberry Pi 3B+ and above.

# Packages being considered
These are packages that may be under development elsewhere, but might be included if there is interest: 
* _WYSIWYGcell_ provides what you see is what you get text edit cells in Jupyter notebooks, but involves significant changes to the Jupyter notebook code, thus will either require providing a fully custom Jupyter notebook or monkey patching a current installation.
* _SimpleUnits_ provides symbols for standard physical units usually encountered at the undergraduate level in the physical sciences. This just defines the symbols so that they can by used in sympy expression, the students are expected to worry about unit conversions themselves.
