JSON string that can be copied into the Snippets menu custom content window 
to provide snippets for initializing some of the JPSL tools.
```
{ "name":"JPSL","sub-menu":[
{
        "name" : "Algebra with Sympy",
        "sub-menu" : [
            {
                "name" : "Initialize algebra_with_sympy",
                "snippet" : [
                    "from algebra_with_sympy import *"
                ]
            },
            {
                "name" : "Documentation",
                "external-link" : "https://gutow.github.io/Algebra_with_Sympy/"
            },
           {
                "name" : "Define an equation",
                "snippet" : [
                    "? = Eqn(lhs,rhs) # Replace ? with name for equation. Replace lhs & rhs with Sympy expressions."
                ]
           }
        ]
    },
{
        "name" : "JupyterPiDAQ",
        "sub-menu" : [
            {
                "name" : "Initialize JupyterPiDAQ",
                "snippet" : [
                    "from jupyterpidaq.DAQinstance import *"
                ]
            },
            {
                "name" : "Documentation",
                "external-link" : "https://jupyterphysscilab.github.io/JupyterPiDAQ/"
            }
        ]
    },
{
        "name" : "Jupyter Pandas GUIs",
        "sub-menu" : [
            {
                "name" : "Initialize GUIs",
                "snippet" : [
                    "from pandas_GUI import *"
                ]
            },
            {
                "name" : "Documentation",
                "external-link" : "https://jupyterphysscilab.github.io/jupyter_Pandas_GUI/"
            },
            {
                "name" : "New Calculated Column GUI",
                "snippet" : [
                    "new_pandas_column_GUI()"
                ]
            },
            {
                "name" : "Plot Pandas Data GUI",
                "snippet" : [
                    "plot_pandas_GUI()"
                ]
            },
            {
                "name" : "Fit Pandas Data GUI",
                "snippet" : [
                    "fit_pandas_GUI()"
                ]
            }
        ]
    },
{ 
        "name" : "Instructor Tools", 
        "sub-menu" : 
      [
             {
              "name" : "Initialize Instructor Actions Menu", 
              "snippet" : [ "import InstructorTools"]
             }, 
           {
                "name": "Documentation",
                "external-link" : "https://github.com/JupyterPhysSciLab/jupyter-instructortools/blob/master/README.md"
            }
        ]
}
]}
```