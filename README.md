# AI Report Summarizer Assistant
An intelligent AI assistant designed to process visual reports (PNG, PDF) and generate comprehensive data summaries. The application leverages Azure AI services and OpenAI models to extract, interpret, and summarize complex charts and text automatically.

  
## Key Features & Workflow
The application demonstrates how visual documents can be seamlessly ingested and intelligently analyzed:
0. Upload: User uploads a report containing charts or text (PNG/PDF) via a clean UI.
1. Data Extraction: Utilizes Azure Computer Vision (OCR / Vision SDK) to accurately extract raw text and data points from the file.
2. Data Interpretation: Sends the extracted data to Azure OpenAI (GPT-4o Vision SDK) to deeply analyze and determine the contextual content of the file.
3. Summarization: Forwards the interpreted content to OpenAI Completions to generate a concise, actionable business summary.
4. Presentation: Displays the final results directly within the Gradio User Interface.


## Prerequisites
Active Azure subscription (with permissions to create OpenAI resources and deploy models).
Python 3.9+
Azure Functions Core Tools
Gradio (for UI generation)


## Configuration (.env)
At the root of the repository, create a .env file with the following structure. Replace the placeholders with your active Azure credentials:
# ========================================
# Azure Computer Vision (OCR processing)
# ========================================
VISION_ENDPOINT="your_vision_endpoint"
VISION_KEY="your_vision_key"

# ========================================
# Azure OpenAI (Summarizer & Interpreter)
# ========================================
AZURE_OPENAI_VERSION="your_openai_version"
AZURE_OPENAI_ENDPOINT="your_openai_endpoint"
AZURE_OPENAI_KEY="your_openai_key"
AZURE_OPENAI_DEPLOYMENT_NAME="your_deployment_name"


## Running the App Locally
0. Install required dependencies:
```bash
python -m pip install -r requirements.txt
```
1. Start the application:
```bash
python app.py
```
2. Open the provided localhost link in your browser, upload your file through the UI, and view the generated AI summary.
   
