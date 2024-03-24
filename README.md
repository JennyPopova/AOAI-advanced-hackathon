# Azure OpenAI advanced features workshop

In this technical workshop, you will learn how to use new capabilities of Azure OpenAI service. You will try differen approaches do deal with the folowing features:
- Speect to text
- Text to speech
- Grounding and Assistants 
- Image creation

This workshop is based on practical hans-on labs where you can try different services and compare them to see when to use what. Moreover, you will explore best practices for prototyping your projects.


## Workshop agenda

### 🌅 Morning (9:00 – 11:30)

> *Fokus: Introduction and first steps*

* 📣 Intro (60 min)
  * Into Workshop (15 min)
  * Intro Azure AI Speech Services (30 min)
  * Intro to Azure Whisper (15 min)
* 🧑🏼‍💻 Environment setup, workshop labs walkthrough (90mins)

### 🌆 Afternoon (12:30 – 16:00)

> *Focus: Hands-on labs*
* 📣Azure Avatar Service demo (30 min)
* 🧑🏼‍💻 Hands-on labs execution: (180 min)
  * Lab 1: Transform spoken words from podcasts into written text utilizing Open Whisper model or Speech to Text service
  * Lab 2: Pass in the transcribed text from the MP3 audio file and extract the podcast guest name using GPT model
  * Lab 3: Use Assistants API and Bing Search for grounding 
  * Lab 4: Use GPT model for generating social media post summary
  * Lab 5: Generate an image for the social media post using Dall-E model
  * Lab 6: Generate an audio file from of the post using Text to Speech service of Azure OpenAI or Azure Speech services
* Wrap-up (15 min)

<sup>
📣 Presentation, 🧑🏼‍💻 Hands-on lab
</sup>

-------------------

## Preparation

### Azure Services
#### Azure OpenAI Service subscription and deployments
Participants should have access to the Azure OpenAI Service subscription and the required deployments. The information needed:
* Azure OpenAI API endpoint and access key
* Deployments for "gpt-4", "whisper", "dall-e-3", "tts" models

Alternatively, grant the participants access to Azure OpenAI Service service be assigning the `Cognitive Service OpenAI user`. If the participant is a `Cognitive Service OpenAI contributor`, they can create the following deployments themselves.

#### Azure AI Speech Services
Participants should have access to the Azure AI Service The information needed:
* Deployment region (for example "swedencentral")
* Access key

#### Azure Bing Search Service
Participants should have access to the Azure Bing Search service The information needed:
* Access key


### Codespace environment

The labs are ment to be run on Github Codespaces. Alternatively, you can bring your own environment (Anaconda). Building the environment can take a few minutes, so please start early.

#### Codespaces

> 🌟 Highly recommended: *Best option if you already have a Github account. You can develop on local VSCode or in a browser window.*

##### 1. Start Codespace and update .env
* Go to Github repository and click on `Code` button. Start your Codespace.
* Create and edit the `.env` file in the `/Lab` folder and fill in with information about Azure services. Save the file!.
##### 2. Python environment: 
In the Terminal install python libraries by running:
```
pip install -r Labs/requirements.txt
```

##### 3. Audio libraries: 
In the Terminal install librries for audio processing. 
* 2.1. Copy and run the following commans in the Terminal, to install `ffmpeg` note that you need to press 'Y' when asked to preseed: 
```sh
sudo add-apt-repository ppa:mc3man/trusty-media
sudo apt-get update
sudo apt-get install ffmpeg
```
  
* 2.2 Copy and run the following commans in the Terminal, to install `gstreamer` note that you need to press 'Y' when asked to preseed: 
```sh
sudo apt install libgstreamer1.0-0 \
gstreamer1.0-plugins-base \
gstreamer1.0-plugins-good \
gstreamer1.0-plugins-bad \
gstreamer1.0-plugins-ugly
```

> *If you closed your Terminal, go Menu-Terminal-New Terminal*



#### Bring your own environment

> *If you already have a Python environment with Jupyter Notebook and the Azure CLI installed.*

Make sure you have the requirements installed in your Python environment using `pip install -r requirements.txt`.
Besides, install the libraries needed for audio processing

-------------------

## Content of the repository

* [Test your environment setup](Labs/0_setup_test.ipynb)

## Exercises

* [1. Transform spoken words from podcasts into written text utilizing Open Whisper model](Labs/1_Podcast_transcription.ipynb)
* [1.1. Transform spoken words from podcasts into written text utilizing Speech to Text service](Labs/1.1_Azure_AI_Services_STT.ipynb) - additional lab
* [2. Pass in the transcribed text from the MP3 audio file and extract the podcast guest name using GPT model](Labs/2_Extract_guest_name.ipynb) 
* [3. Use Azure OpenAI tools and function to get more information from the Internet](Labs/3_Bing_grounding.ipynb)
* [3.1. Build Azure OpenAI Assistants that retrieves information from the Internet](Labs/3.1_Assistants_function_calling_with_bing_search.ipynb) - additional lab
* [4. Use GPT model for generating social media post](Labs/4_Create_post.ipynb)
* [5. Generate an image for the social media post using Dall-E model](Labs/5_Create_post-image.ipynb)
* [6. Generate an audio file from of the post using Azure OpenAI Text to Speech service](Labs/6_Create_post-audio.ipynb)
* [6.1. Generate an audio file from of the post using Azure AI Speech service](Labs/6.1_Azure_AI_Services_TTS.ipynb) - additional lab



## Usefull links

- Azure OpenAI: https://learn.microsoft.com/en-us/azure/ai-services/openai/overview
- Azure Bing Search: https://learn.microsoft.com/en-us/bing/search-apis/bing-web-search/overview
- Azure AI Speech Services: https://azure.microsoft.com/en-us/products/ai-services/ai-speech