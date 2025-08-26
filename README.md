# Porto Seguro’s Safe Driver Prediction

## Our Task

- Company:         Porto Seguro (insurance)
- Task:            Predict whether a driver will file an insurance claim in the next year
- Target Variable: Binary (target = 0 or 1)
- Why good:        Large insurance dataset, real business case, tabular only
- Link:            [Porto Seguro Safe Driver]("https://www.kaggle.com/competitions/porto-seguro-safe-driver-prediction/overview")


---

## Optional To-Do: Add workflows

Workflows can help you keep your kanban board automatically on track. 

Select the project created in the steps above.  

Click on the 3 dots to the far right of the board (...)

Select workflow as the first option. 

Activate the ones you feel necessary to your project

Go back to your project repository (fraud detection)

## Set up your Environment



### **`macOS`** type the following commands : 

- For installing the virtual environment you can either use the [Makefile](Makefile) and run `make setup` or install it manually with the following commands:

     ```BASH
    make setup
    ```
    After that active your environment by following commands:
    ```BASH
    source .venv/bin/activate
    ```
Or ....
- Install the virtual environment and the required packages by following commands:

    ```BASH
    pyenv local 3.11.3
    python -m venv .venv
    source .venv/bin/activate
    pip install --upgrade pip
    pip install -r requirements.txt
    ```
    
### **`WindowsOS`** type the following commands :

- Install the virtual environment and the required packages by following commands.

   For `PowerShell` CLI :

    ```PowerShell
    pyenv local 3.11.3
    python -m venv .venv
    .venv\Scripts\Activate.ps1
    python -m pip install --upgrade pip
    pip install -r requirements.txt
    ```

    For `Git-bash` CLI :
  
    ```BASH
    pyenv local 3.11.3
    python -m venv .venv
    source .venv/Scripts/activate
    python -m pip install --upgrade pip
    pip install -r requirements.txt
    ```

    **`Note:`**
    If you encounter an error when trying to run `pip install --upgrade pip`, try using the following command:
    ```Bash
    python.exe -m pip install --upgrade pip
    ```

## Data

This [kaggle]("https://www.kaggle.com/competitions/porto-seguro-safe-driver-prediction/overview") data is used for the project. Please download it and unpack it in the data folder. 

   
## Usage

In order to train the model and store test data in the data folder and the model in models run:

**`Note`**: Make sure your environment is activated.

```bash
python example_files/train.py  
```

In order to test that predict works on a test set you created run:

```bash
python example_files/predict.py models/linear_regression_model.sav data/X_test.csv data/y_test.csv
```

## Limitations

Development libraries are part of the production environment, normally these would be separate as the production code should be as slim as possible.


