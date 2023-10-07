# Mental-Healthcare-Bot

This is a mental healthcare chatbot developed in RASA Framework, to analyse person's chances of mental illness on the basis of survey questionnaire. <br>
RASA is an open-source machine learning framework used in building contextual AI assistants and chatbots in text and voice. It is a robust platform that includes natural language understanding and open-source natural language processing. It’s a full toolset for extracting the important keywords, or entities, from user messages, as well as the meaning or intent behind those messages. Rasa NLU (Natural Language Understanding) is a tool for understanding what is being said in short pieces of text; it also happens to be my favorite chatbot platform for several reasons, such as it being open-sourced, widely used, and well documented.

# RASA Chatbot Setup and Usage Guide

This guide will walk you through the installation, setup, and usage of the RASA-based Mental Healthcare Chatbot. Follow these steps to get started with your chatbot project.

## Step 1: Install RASA

**Prerequisites:**

- [Download Anaconda Prompt](link-to-anaconda-prompt)
- [Download Microsoft Build Tools](link-to-build-tools)
- Create a directory on your system to store your Rasa project.

1. Open Anaconda Prompt.

2. Create a virtual environment using the following command:
   
   ```bash
   conda create -n rasavirtualenv python=3.6

3. Activate your environment

   ```bash
   conda activate rasavirtualenv

4. Install Rasa Open Source

   ```bash
   pip install rasa

## Step 2: Setup a Base Project

The `rasa init` command will create a new Rasa project in a local directory, which you specify by providing the directory name. It will populate the project with example training data and train the NLU and dialogue models. By default, it trains a simple assistant called "moodbot."

### Project Structure

- `__init__.py`: Initializes the directory with required packages.
- `endpoints.yml`: Defines different endpoints, including the action endpoint for custom actions and the UI.
- `domain.yml`: Defines the chatbot's boundaries, intents, entities, responses, actions, and slots.
- `credentials.yml`: Stores credentials for connected services.
- `config.yml`: Contains NLU and Core model configurations, including policies and pipelines.
- `actions.py`: Contains the main logic of the chatbot, defining its responses.
- `models/`: Stores trained models.
- `data/`: Contains training data, including `nlu.md` for natural language understanding and `stories.md` for conversation flows.

## Running Custom Actions

In the RASA stack, you can write custom actions in `actions.py`. To use custom actions in your chatbot's stories, start the actions webhook.

## Training Your RASA Bot

After adding entities, intents, actions, and stories, train your bot using the following command:

```bash
rasa train
```

## Running Your RASA Bot

To interact with your bot, follow these steps:

1. Open your terminal or command prompt.

2. Navigate to the directory where your Rasa project is located.

3. Run the chatbot using the following command:

   ```bash
   rasa shell
