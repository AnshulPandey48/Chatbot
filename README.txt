LLM Medical Chatbot

Overview
LLM Medical Chatbot is an advanced AI chatbot powered by Mistral 7B and DeepSeek 32B, 
designed to provide accurate medical responses with a seamless web UI. 
The model is highly flexible and can be adapted for different domains by simply modifying input constraints.

Features
- Multi-Model Architecture: Utilizes Mistral 7B for initial classification and DeepSeek 32B for detailed responses.
- Customizable Input Constraints: Modify the first argument in Mistral 7B to change the domain (e.g., from "medical" to any other field).
- Pipeline-Based Processing: If the input is classified as relevant ("yes"), it is passed to DeepSeek 32B for a precise answer.
- Supports API and Offline Models: Works with APIs or locally via Ollama for offline execution.
- User-Friendly Web UI: A clean and interactive interface for smooth interaction.

Setup & Installation
1. Clone the Repository
   git clone https://github.com/yourusername/llm-medical-chatbot.git
   cd llm-medical-chatbot

2. Install Dependencies
   pip install -r requirements.txt

3. Run the Chatbot
   Using Online API:
   python app.py --use_api True --api_key YOUR_API_KEY

   Using Offline Models (Ollama):
   python app.py --use_api False

How It Works
Step 1: Input Classification
- The user's query is first processed by Mistral 7B.
- The model checks if the query is related to the specified domain (e.g., "medical").
- If "yes", the query is forwarded to the next stage.

Step 2: Query Processing
- The query is passed through a pipeline to DeepSeek 32B.
- The model generates a detailed response.

Step 3: Response Generation
- The output is displayed on the web UI.
- The UI is designed for fast and interactive conversations.

Customization
To use this chatbot for other domains, change the input constraint in Mistral 7B:
   if mistral_7b_classify(input_query, "finance"):  # Change "medical" to your desired category
       response = deepseek_32b_generate(input_query)

Contact
Made by: Anshul Pandey
Email: anshul4894@gmail.com

Contributing
Pull requests are welcome! If you find a bug or have an improvement, feel free to submit an issue.

License
MIT License
