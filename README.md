## Project Structure - what you will be cloning


```text
hds-practical/
├── README.md
├── .gitignore
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
To run `python src/analyze.py` or `Rscript src/analyze.R`, you must access these files from the script folder.
