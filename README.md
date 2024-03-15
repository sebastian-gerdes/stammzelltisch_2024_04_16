## Companion repository for Stammzelltisch on April 9, 2024

## Setup - to be done ideally in advance
### What you need:
* Laptop with at least 8 Gb of Ram (tutorial tested mainly on Apple silicon)
* Terminal (with homebrew on Macos)
* Browser
* Optional: OpenAI account - you can create it [here](https://platform.openai.com/signup)

    

### Setup python and python environment
#### Install miniconda:
* On macOS:
```
brew install --cask miniconda
```
* Else: Follow instructions [here](https://docs.anaconda.com/free/miniconda/miniconda-install/)


### Setup Ollama
* On macOS: 
```
brew install ollama
```
* Else: Follow instructions [here](https://ollama.com/download/mac)
* Open a terminal and type:
```
ollama serve
ollama run llama2
ollama list
```

### Download tutorial files
The tutorial files will be created in your home folder and can be removed at the end of the session.
```
cd ~
git clone https://github.com/sebastian-gerdes/stammzelltisch_2024_04_09.git
cd stammzelltisch_2024_04_09
```

#### Setup python environment
```
conda env create --name stammzelltisch -f stammzelltisch.yml
conda activate stammzelltisch
```

### Open the jupyter file
* Launch jupyter notebook server:
```
jupyter notebook
```
* Open server in the browser
* Open the notebook `stammzelltisch.ipynb`

### Removing the files
* Miniconda
* Ollama
* Tutorial files