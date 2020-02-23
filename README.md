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

