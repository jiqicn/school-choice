# Computational Modelling of Primary School Segregation (COMPASS)

[![DOI](https://zenodo.org/badge/483226861.svg)](https://zenodo.org/badge/latestdoi/483226861)

This Python implementation tries to model school choice and resulting school segregation based on the work of Schelling (1971) and Stoica & Flache (2014).

## Usage

### Install and Run
It's required to firstly install [GDAL](https://gdal.org/index.html) on your computer. 

To install the package, run `pip install compass-school`. 

To run a demo with web-based GUI, run `python run.py` from the root directory of the project. This will start a local server to automatically open your web browser and show the program as a webpage. If not seeing the webpage open, manually input `http://localhost:5004/` in the link bar. 

### Update Documentation
Install pdoc3 if you haven't already done so. Browse to the compassproject folder in your terminal and run `pdoc3 --html --force --output-dir docs compass`. The documentation should be updated now.

### Overview
The repository consists of:
* **run.py:** a script that runs the model interactively with a visualisation (browser)
* **testrun.py:** a test script (work in progress)
* **household.py:** the household class
* **student.py:** the student class
* **neighbourhood.py:** the neighbourhood class
* **school.py** the school class
* **allocator.py:** allocates the students to their school of choice
* **agents_base.py:** overarching agent used for inheritance
* **model.py:** initialises the entire system and all of its components
* **parameters.py:** contains all the parameter values for the simulation
* **scheduler.py:** takes care of the activation, sequence and placement of all agents
* **visualisation.py:** browser based visualisation
* **utils.py:** containing all measurements
* **functions.py:** containing some math functions to be used by the classes

### Simulations
Information on how to run the code here.

### Testing and development

Setup a virtualenv with the required dependencies.
```bash
$ python -m venv env
$ . env/bin/activate
$ pip install -r requirements.txt
```

Install the package locally (in developement, or editing mode):
```bash
$ pip install -e .
```

Then run the tests with:
```bash
$ pytest
```

### Profiling

Some profiling result can be found in this [notebook](https://github.com/ODISSEI-School-Choice/school-choice/blob/jisk-v2/profile.ipynb). Also, some scaling graphs can be found in this [notebook](https://github.com/ODISSEI-School-Choice/school-choice/blob/jisk-v2/scaling_graph.ipynb).
