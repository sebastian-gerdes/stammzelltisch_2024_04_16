## Companion repository for Stammzelltisch on April 16, 2024
In the Stammzelltisch on April 16, 2024, I want to present the current state of our project to develop an assistance system for the design of clinical studies using artificial intelligence techniques, running title of the app is "trialGPT". In order to make the topic more tangible, I intend to include a short hands-on session. For this part, the participants ideally install some software in advance (see section Setup). In this session, the participants are invited to take part in a short tutorial for the use of large language models (LLMs) on their local computer.

The examples are in Python, using mainly the python library langchain and the Llama2 LLM, installed on the local machine via the software Ollama. Furthermore, the langchain library is used to perform retrieval augmented generation (RAG), a technique which allow to feed the knowledge of additional documents into the LLM. Last, the tutorial contains a quick walk-through through the prototype of trialGPT.

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
#### Install miniconda (approx. 3 minutes):
* Miniconda is a software that allows to install scientific software in an easy and easily removable way
* On macOS:
```
brew install --cask miniconda
```
* Else: Follow instructions [here](https://docs.anaconda.com/free/miniconda/miniconda-install/)


### Setup Ollama (approx 4 GB will be downloaded)
* On macOS: 
```
brew install ollama
```
* Else: Follow instructions [here](https://ollama.com/download/mac)
* To download the Llama2 LLM, you need to start a local Ollama server. To do so, open a terminal and type (leave this terminal open for the rest of this tutorial):
```
ollama serve
```
* Now open a second terminal, from which you can steer the ollama model:
```
ollama pull llama2
```

### Download tutorial files
The tutorial files will be created in your home folder and can be removed at the end of the session.
```
cd ~
git clone https://github.com/sebastian-gerdes/stammzelltisch_2024_04_16.git
cd stammzelltisch_2024_04_16
```

#### Setup python environment (a few hundred MBs will be downloaded)
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
* Open the notebook `hands_on/llm_tutorial.ipynb`
* Execute the code cells from top to bottom by selecting them and then pressing <kbd>Shift</kbd> + <kbd>Enter</kbd>
* Be patient, — interaction with the LLM can take some moments.

### Removing the installed files via terminal:
* Miniconda including the created environments
```
rm -r ~/miniconda/
```
* Ollama
```
brew uninstall ollama
```
* Tutorial files
```
rm -r ~/stammzelltisch_2024_04_16
```
