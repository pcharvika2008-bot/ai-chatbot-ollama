🤖 Ollama AI Chatbot

A simple AI chatbot built with Python, Streamlit, and Ollama using the Gemma 3 1B language model.

The chatbot provides an interactive web-based interface where users can have conversations with a locally running AI model.

✨ Features

🤖 AI chatbot powered by Ollama

🧠 Uses the gemma3:1b model

💬 Interactive chat interface

📝 Maintains conversation history during the session

⚡ Lightweight and easy to run

🔒 Runs the AI model locally

🎨 Simple Streamlit interface

🛠️ Technologies

Python

Streamlit

Ollama

Gemma 3 1B

📁 Project Structure
ollama-ai-chatbot/
│
├── app.py
├── requirements.txt
├── .gitignore
└── README.md

📋 Prerequisites

Before running this project, make sure you have:

Python 3.9 or later

Ollama installed

Gemma 3 1B model downloaded

🚀 Installation
1. Clone the repository
git clone https://github.com/YOUR-USERNAME/ollama-ai-chatbot.git
cd ollama-ai-chatbot


Replace YOUR-USERNAME with your GitHub username.

2. Create a virtual environment
Windows
python -m venv venv
venv\Scripts\activate

macOS / Linux
python3 -m venv venv
source venv/bin/activate

3. Install dependencies
pip install -r requirements.txt

🦙 Setup Ollama

Install Ollama on your computer.

Then download the Gemma 3 1B model:

ollama pull gemma3:1b


Verify that the model is installed:

ollama list


You should see:

gemma3:1b


You can also test the model:

ollama run gemma3:1b

▶️ Run the Chatbot

Start the Streamlit application:

streamlit run app.py


After running the command, Streamlit will provide a local URL.

Open:

http://localhost:8501


in your browser.

💡 How It Works

The application uses Streamlit's session state to store the conversation:

if "messages" not in st.session_state:
    st.session_state.messages = []


When the user enters a message, it is added to the conversation history.

The conversation is then sent to Ollama:

response = ollama.chat(
    model="gemma3:1b",
    messages=st.session_state.messages
)


Ollama generates an AI response using the Gemma 3 1B model.

The response is displayed in the Streamlit interface and saved to the conversation history.

🖥️ Application Flow
User
  ↓
Streamlit Chat Interface
  ↓
User Message
  ↓
Conversation History
  ↓
Ollama
  ↓
Gemma 3 1B
  ↓
AI Response
  ↓
Streamlit Chat Interface

📦 Dependencies

The project uses the following Python packages:

streamlit
ollama


Install them using:

pip install -r requirements.txt

🔧 Change the AI Model

The current model is:

model="gemma3:1b"


You can change it to another model supported by your Ollama installation.

For example:

model="llama3.2"


Then download the model:

ollama pull llama3.2

🐛 Troubleshooting
Ollama connection error

Make sure Ollama is installed and running.

Check available models:

ollama list

Gemma model not found

Run:

ollama pull gemma3:1b

Streamlit command not found

Install Streamlit:

pip install streamlit


Then run:

streamlit run app.py

🔐 Privacy

This chatbot is designed to use Ollama locally. Your conversations are processed by the locally running model rather than requiring a cloud-based AI API.

🚧 Future Improvements

Some possible improvements for this project:

🗑️ Clear chat button

🎨 Custom themes

🤖 Model selection

💾 Save conversations

📤 Export chats

📄 PDF/document chat

🎤 Voice input

🌐 Deploy the application

⚙️ Chatbot configuration options

📄 License

This project is open source and available for educational and personal use.

👨‍💻 Author

Created using Python + Streamlit + Ollama + Gemma 3.

If you found this project useful, consider ⭐ starring the repository!
