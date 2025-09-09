# Inference vs Prediction

<img src = "img/dbt_1_ingestion.jpg">

## Table of Contents

- [Project Structure](#project-structure)
- [Setup Instructions](#setup-instructions)
  - [Prerequisites](#prerequisites)
  - [Build and Run](#build-and-run)

## Project Structure

- **name_of_your_project_repo (project-root)/**
    - **.venv/**
    - **xyz/**
    - **.env**
    - **.gitignore**
    - **.python-version**
    - **requirements.txt**
    - **README.md**

## Setup Instructions

### Prerequisites

Make sure you have the following installed on your local development environment:

* **.venv - Virtual Environment**
  * Upgrade pip outside and inside of your venv to avoid problems: python.exe -m pip install --upgrade pip 
  * cd your_repo_folder
  * `python3 -m venv .venv`                            (This will create a virtual environment for the repo folder)
  * `source .venv/Scripts/activate`
  * Upgrade pip outside and inside of your venv to avoid problems: `python.exe -m pip install --upgrade pip`
  * Install everything you need for your project from the `requirements.txt` file:
    * `pip install --no-cache-dir -r requirements.txt`  (This will install things within your virtual environment)

Make sure to inclue a .gitignore file with the following information:

* .venv/         (to ignore the virtual environment stuff)
* *.pyc          (to ignore python bytecode files)
* .env           (to ignore sensitive information, such as database credentials)

### Build and Run

1. **Clone the repository:**

   ```bash
   git clone https://github.com/caiocvelasco/end-to-end-data-science-project.git
   cd end-to-end-data-science-project

2. **Activate you Virtual Environment (.venv)**

* `cd your_repo_folder`
* `source .venv/Scripts/activate`                   (This will activate your environment)

### Publish your Quarto document as a GitHub Pages (gh-pages) site

* `quarto render`
* `quarto publish gh-pages`