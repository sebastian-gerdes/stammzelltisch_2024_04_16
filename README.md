## Companion repository for Stammzelltisch on April 9, 2024
In the Stammzelltisch on April 9, 2024, I want to present the current state of our project to develop an assistance system for the design of clinical studies using artificial intelligence techniques, running title of the app is "trialGPT". In order to make the topic more tangible, I intend to include a short hands-on session. For this part, the participants ideally install some software in advance (see section Setup). In this session, the participants are invited to take part in a short tutorial for the use of large language models (LLMs) on their local computer.

The examples are in Python, using mainly the library langchain and the Llama2 LLM. Furthermore, the langchain library is used to perform retrieval augmented generation (RAG), a technique which allow to feed the knowledge of additional documents into the LLM. Last, the tutorial contains a quick walk-through through the prototype of trialGPT.

In this readme-file, the steps to install the required software are described. Furthermore, instructions how to (hopefully) completely remove the installed software after the tutorial are provided.

## Setup - to be done ideally in advance
### What you need:
* Laptop with at least 8 Gb of Ram (tutorial tested mainly on Apple silicon)
* Ideally macOS with [Homebrew](https://brew.sh/)
    * For other operating systems a little more action is required on the user side, but in most cases everything should work fine as well
* Terminal
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