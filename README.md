
AI Symptom Classifier for Hospital Triage

📖 Overview
This project is an intelligent AI agent designed to act as a preliminary point of contact at a hospital. It takes a patient's self-described symptoms as input and classifies them into one of three categories: General, Emergency, or Mental Health. Based on this classification, it directs the patient to the appropriate hospital ward.

This system is built using Python, the Gemini 1.5 Flash model, and the LangGraph library to create a robust, stateful AI agent.

✨ Key Features
Symptom Intake: A user-friendly prompt to gather the patient's symptoms.

AI-Powered Classification: Utilizes the Gemini 1.5 Flash model to accurately categorize the symptoms.

Stateful Routing: Built with LangGraph to create a logical flow, ensuring the patient's query is routed to the correct node based on its classification.

Clear Patient Direction: Provides a final, clear output directing the patient to the appropriate ward (General, Emergency, or Mental Health).

🛠️ Technology Stack
Python: The core programming language.

Google Gemini 1.5 Flash: The Large Language Model (LLM) used for symptom classification.

LangGraph: A library for building stateful, multi-actor applications with LLMs.

LangChain: For core abstractions and integrations.

Google Colab / Jupyter Notebook: For development and execution.

🚀 How It Works
The project is structured as a state machine (a "graph") where each step is a "node." The flow is as follows:

1. Get Symptom: The graph starts at this node, prompting the user to enter their symptom.

2. Classify Symptom: The user's input is passed to the Gemini LLM with a specialized prompt, asking it to classify the symptom into one of the three predefined categories.

3. Route Symptom: Based on the LLM's classification, a conditional router directs the flow to one of three final nodes.

4. Final Output: The corresponding node (General, Emergency, or Mental Health) generates a message directing the patient to the correct ward, and the graph execution ends.



⚙️ Setup and Installation
 To run this project, follow these steps:

1. Clone the repository:

    Bash

    git clone https://github.com/your-username/your-repository-name.git
    cd your-repository-name

2. Install dependencies:
   The project uses several Python libraries. You can install them using pip:

    Bash

    pip install -qU google-generativeai langgraph langchain langchain-google-genai

3. Set up your API Key:
    You will need a Google Gemini API key. The script will securely prompt you to enter your key when you run it.

    You can get your API key from Google AI Studio.



▶️ How to Run
Open the .ipynb file in Google Colab or a local Jupyter Notebook environment.

Run the cells in sequential order.

When prompted, enter your Gemini API key.

When prompted by the "Welcome to XYZ hospital" message, enter a symptom (e.g., "I have a high fever" or "I am feeling very anxious and sad").

The AI agent will process the input and print the final output with the appropriate ward direction.

📝 Future Improvements
Integration with Hospital Systems: Connect the agent to a real hospital database to book appointments.

Multi-language Support: Add functionality to process symptoms in different languages.

More Granular Categories: Expand the classification to include more specific departments like Cardiology, Pediatrics, etc.

Web Interface: Build a simple web UI using a framework like Flask or Streamlit to make the agent more accessible.

![Hospital Logo](images/hospital.png)
