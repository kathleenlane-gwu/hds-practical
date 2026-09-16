## Project Structure - what you will be cloning


```text
hds-practical/
├── README.md
├── .gitignore
├── Dockerfile
├── environment.yml
├── renv.lock      
├── src/
    ├── analyze.py
    ├── analyze.R
├── data/
    ├── patients.csv
    ├── patients_by_age.csv
└── AI_USAGE.md
```

## Necessary Tools/Downloads for Repository
* Terminal
* Python -- https://www.python.org/downloads/
* VS Code (optional) -- https://code.visualstudio.com/
* Miniforge for Conda/Mamba -- https://github.com/conda-forge/miniforge/releases
* Rstudio -- https://posit.co/products/open-source/rstudio
* Renv -- install.packages("renv") in Rstudio Console
* Docker -- https://www.docker.com/products/docker-desktop/

## Getting Started
Open the terminal on your computer and copy/paste the code below into the terminal. The `cd ~/Desktop` command tells the computer to work within your Desktop folder and will clone the repo there. The `git clone` command will clone the `hds-practical` repository using the GitHub URL. Then `cd hds-practical` enters the repository, and `ls` lets you view the files in the repo. You should see the same files from the project structure above.
```
cd ~/Desktop
git clone https://github.com/kathleenlane-gwu/hds-practical.git
cd hds-practical
ls 
```
## Analysis
To run `python src/analyze.py` or `Rscript src/analyze.R`, you must first recreate the necessary environments. We will begin with the python file. 

In the terminal, copy/paste the following code. `mamba env create` recreates the necessary environment from the `environment.yml` file. We then need to access the hds-practical environment which has the necessary Python and packages need to run our analyses. Once these steps are complete, we can open and run the `analyze.py` file.
```
mamba env create -f environment.yml
conda activate repro-demo
python src/analyze.py
```
For our R file, open RStudio and copy/paste the following code into the R console. `renv::restore()` recreates the R environment from the `renv.lock` file. 
```
renv::restore()
```
Return to the terminal and copy/paste the following code. Once these steps are complete, we can open and run the `analyze.R` file.
```
Rscript src/analyze.R
```
## Docker
To run check the Dockerfile, copy and paste the following into your terminal.
```
docker build -t repro-demo .
docker run --rm repro-demo
```
