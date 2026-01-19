# Assignment 2 - PAB

A repository for the second assignment of "Programação aplicada à Bioinformática".


## BacSimul
### Program Description

A Python program that simulates the growth of bacteria on a 2D grid in discrete time steps by reading a JSON file containing the necessary information about the bacteria.


### Program Objectives

The objectives of this program are:

- Receive information via command line.
- Each bacterium should be represented as an object with its own behavior.
- Create a 2D grid that simulates where bacteria live and grow, supporting different species of bacteria.
- Run using discrete time steps.
- Obtain a visual output of the generated grid at a certain printing frequency and a CSV file with bacteria data.


### Program Structure

```text
.
├──LICENSE - Program license.
├──README.md - Documentation of the Repository and Program.
└──Raquel_Procópio_2024152293-Ana_Cavaleiro_2025179696-bacterial_growth_simulation.zip - Zip file with a directory with the files of the program.
    ├──bgc.py - Main file responsible for the execution of the Program. Contains "Class Simulation", functions and argument parser.
    ├──bacteria_module.py - Module containing "Class Bacterium" representing each bacteria.
    └──grid_module.py - Module containing "Class Grid" representing the simulation space.
```

### Program Usage and Requirements

To execute this program you must have:

- *Python 3.x*

The following information must be given as command line arguments:
- `width`: Grid width
- `height`: Grid height
- `simul_steps`: Number of simulation steps
- `print_freq`: Frequency at which the grid is printed
- `JSON_path`: Path to the JSON configuration file
- `CSV_path`: Path to an output CSV file


How to execute:


First you have to unzip the zip file in this repository. **Make sure you don´t unzip it into a directory with the same name as the directory inside.**
It should be only one directory with the name: `Raquel_Procópio_2024152293-Ana_Cavaleiro_2025179696-bacterial_growth_simulation`, and inside there will be 3 files:
- `bgc.py`
- `bacteria_module.py`
- `grid_module.py`


```bash
#Go into the directory
cd Raquel_Procópio_2024152293-Ana_Cavaleiro_2025179696-bacterial_growth_simulation
#Run the simulation
python bgc.py <width> <height> <simul_steps> <print_freq> <JSON_path> <CSV_path>
#Command line arguments help:
python bgc.py -h
```
#### Example:
```bash
#Example:
python bgc.py 10 10 100 10 example.json results.csv
```

#### Output

There are two Outputs:
- Grid Visualization 
- CSV file containing the number of bacteria per specie at each simulation step


**Grid Visualization Example:**

```
Step 4
* 0 0 0 * 
0 + 0 + * 
0 0 0 + 0 
0 0 0 0 * 
+ * 0 0 + 
```

**Example of JSON file:**
```
{
"species": [
    {
      "name": "FastGrower",
      "symbol": "*",
      "growth_rate": 0.3,
      "division_threshold": 1.0,
      "initial_count": 5
    },
    {
      "name": "SlowGrower",
      "symbol": "+",
      "growth_rate": 0.2,
      "division_threshold": 1.2,
      "initial_count": 5
    }
  ]
}
```


### Authors and Support

Authors:
- *Raquel Procópio* (2024152293)
- *Ana Cavaleiro* (2025179696)

For support:
- 2024152293@estudantes.ips.pt
- 2025179696@estudantes.ips.pt


### License

*BacSimul* is licensed under the **MIT license**.
See `LICENSE` file.

