## Overview

Local Multimodal AI Chat is an interactive project designed to teach how to create a chat application that integrates multiple types of AI models. This project focuses on combining different AI technologies to handle audio, images, and PDFs within a single chat interface. It's an excellent hands-on learning experience for those interested in AI and software development.

## Features

- **Quantized Model Integration**: This application uses "quantized models," which are optimized to work on standard consumer hardware. Typically, these models are very large and require powerful computers, but quantized versions are smaller and more efficient while maintaining performance. This allows the app to function effectively on everyday devices. For more details, see [Quantized Models from TheBloke](https://huggingface.co/TheBloke).

- **Audio Chatting with Whisper AI**: The app includes advanced audio messaging capabilities using Whisper AI, which offers robust transcription. Whisper AI accurately interprets and responds to voice inputs, providing a smooth and natural conversation experience. Learn more about the [Whisper models](https://huggingface.co/collections/openai/whisper-release-6501bba2cf999715fd953013).

- **Image Chatting with LLaVA**: For image processing, the app uses LLaVA, a fine-tuned LLaMA model that understands image embeddings created by a CLIP model. This integration enables sophisticated text and image comprehension, making interactions involving visual content more engaging. For further information, visit the [llama-cpp-python repository](https://github.com/abetlen/llama-cpp-python).

- **PDF Chatting with Chroma DB**: The app is designed for both professional and academic users, featuring Chroma DB as a vector database for efficient PDF interactions. Users can interact with their PDF files locally, whether they are reviewing business reports, academic papers, or other documents. The app uses AI to understand and respond to PDF content, offering summaries, insights, and a unique dialogue experience. See the [Chroma website](https://docs.trychroma.com/) for more details.

### Getting Started

To set up Local Multimodal AI Chat, follow these steps:

1. **Clone the Repository**: Clone the project repository to your local machine.

2. **Create a Virtual Environment**: Ensure you're using Python 3.10.12.

3. **Upgrade pip**: Run `pip install --upgrade pip`.

4. **Install Requirements**: Execute `pip install -r requirements.txt`.
   
   **Windows Users**: The installation process might differ slightly. If you encounter issues, please open an issue on GitHub.

5. **Set Up Local Models**: Download the necessary models. For image chat, use the [LLaVA model](https://huggingface.co/mys/ggml_llava-v1.5-7b/tree/main) (ggml-model-q5_k.gguf and mmproj-model-f16.gguf). For the quantized model, use the [Mistral model](https://huggingface.co/TheBloke/Mistral-7B-Instruct-v0.1-GGUF) from TheBloke (mistral-7b-instruct-v0.1.Q5_K_M.gguf).

6. **Customize Configuration File**: Modify the config file to match the models you've downloaded.

7. **Optional - Change Profile Pictures**: Replace `user_image.png` and/or `bot_image.png` in the `chat_icons` folder if desired.

8. **Run Commands in Terminal**: 
   1. Initialize the SQLite database for chat sessions with `python3 database_operations.py`.
   2. Start the application with `streamlit run app.py`.
