# TrinityVerseAI 🕊️
### Multilingual Spiritual Conversational Intelligence System

**TrinityVerseAI** is an AI-powered spiritual conversational system designed to help users explore teachings from the **Bhagavad Gita, Quran, and Bible**. It combines semantic search, large language models, emotion detection, multilingual translation, text-to-speech, and mood-based music recommendations in a single interactive application.

The project aims to make spiritual knowledge more accessible through natural-language questions, relevant scripture retrieval, and AI-generated explanations.

---

## 📖 About the Project

In today's digital world, artificial intelligence can help people explore information, understand complex concepts, and interact with knowledge in a more accessible way.

TrinityVerseAI applies these capabilities to spiritual texts from three major religious traditions:

- **Bhagavad Gita** — explores philosophical teachings and guidance.
- **Quran** — supports the exploration of Quranic verses and their meanings.
- **Bible** — helps users find relevant biblical passages and explanations.

Users can enter questions or describe their concerns. The system searches for relevant textual content using semantic similarity and uses a language model to generate explanations. Additional capabilities include emotion detection, translation, audio output, and mood-based music recommendations.

TrinityVerseAI is an educational and exploratory project. It is not intended to replace religious scholars, spiritual leaders, or professional mental health support.

---

## 🎯 Objectives

- Develop an interactive AI-powered spiritual assistance application.
- Retrieve relevant scripture passages using semantic search.
- Generate contextual explanations with a large language model.
- Support multilingual interactions through translation.
- Identify user emotions using AI-based text classification.
- Provide text-to-speech functionality for audio accessibility.
- Recommend music based on the user's detected mood.
- Integrate multiple AI technologies into one user-friendly interface.

---

## ✨ Features

### 1. Multi-Religious Scripture Search

Searches relevant content from the Bhagavad Gita, Quran, and Bible based on the user's input.

### 2. Semantic Search

Uses Sentence Transformers to convert text into vector embeddings and FAISS to retrieve semantically similar content.

### 3. AI-Generated Explanations

Uses the Groq API with a supported LLM to generate explanations based on the user's query and retrieved information.

### 4. Emotion Detection

Analyzes user text to identify an emotion or emotional state and uses that information to support the interaction.

### 5. Multilingual Translation

Includes translation functionality intended to make the content accessible to users who prefer different languages.

### 6. Text-to-Speech

Uses Google Text-to-Speech (gTTS) to convert supported text into audio.

### 7. Mood-Based Music Recommendations

Uses a music dataset to recommend music according to the detected mood.

### 8. Interactive Web Interface

Uses Gradio to provide a simple interface through which users can interact with the application.

### 9. Machine Learning Workflow

Includes a TF-IDF and Random Forest workflow for text-based emotion classification experiments.

---

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| Sentence Transformers | Text embeddings |
| FAISS | Similarity search |
| Groq API | Large language model inference |
| Llama model | AI-generated responses |
| Gradio | Interactive user interface |
| gTTS | Text-to-speech conversion |
| Pandas | Dataset handling |
| NumPy | Numerical operations |
| Scikit-learn | TF-IDF and Random Forest |
| Google Colab | Cloud-based development and execution |
| Spotify embed | Music playback integration |

---

## 🏗️ System Architecture

The application follows this general workflow:

1. The user enters a question or message.
2. The system processes the input.
3. The query is converted into an embedding.
4. FAISS searches for semantically relevant text.
5. The retrieved content and query are passed to the language model.
6. The system generates a response.
7. Optional translation, emotion detection, or audio functionality is applied.
8. Mood-based music recommendations may be displayed.
9. The result is presented through the Gradio interface.

### Workflow Diagram

```text
           User Input
                |
                v
       Text Preprocessing
                |
                v
       Sentence Embeddings
                |
                v
       FAISS Similarity Search
                |
                v
     Relevant Scripture Content
                |
                v
         Groq LLM API
                |
                v
       AI-Generated Response
                |
       +--------+---------+
       |        |         |
       v        v         v
   Translation Emotion   Text-to-
              Detection  Speech
       |
       v
 Mood-Based Music
 Recommendations
       |
       v
   Gradio Interface
```

*The diagram represents the intended high-level workflow; the exact execution path depends on the implementation.*

---

**Note:** Dataset files are not included in this repository because of their size. Add the required datasets to the corresponding folders before running the project.

---

## 📦 Requirements

- Python 3.10 or a compatible version supported by the installed libraries.
- Internet connection for API requests and downloading model resources.
- A Groq API key.
- Required datasets in the appropriate directories.
- Google Colab or a compatible local Python environment.

### Python Libraries

```bash
pip install sentence-transformers faiss-cpu groq gradio gTTS pandas numpy scikit-learn
```

Depending on your notebook and environment, additional libraries may be required.

---

## 🚀 Installation and Setup

### Step 1: Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/TrinityVerseAI.git
```

Replace `YOUR_USERNAME` with your GitHub username.

### Step 2: Open the Project

```bash
cd TrinityVerseAI
```

### Step 3: Install Dependencies

```bash
pip install sentence-transformers faiss-cpu groq gradio gTTS pandas numpy scikit-learn
```

### Step 4: Add the Required Datasets

Place the required dataset files in the directories expected by the code:

- `gitadata`
- `qurandata`
- `bibledata`
- `musicdata`

Check the notebook for the exact filenames and paths it expects.

### Step 5: Configure the API Key

Set up your Groq API key using an environment variable or a secure secret manager before running the application.

---

## 🔑 Groq API Configuration

TrinityVerseAI uses the Groq API to access a language model for response generation.

### Google Colab

1. Open your notebook in Google Colab.
2. Open the Secrets panel.
3. Add a secret named `GROQ_API_KEY`.
4. Enter your API key and enable notebook access to the secret.
5. Retrieve the key in your code:

```python
from google.colab import userdata
import os

os.environ["GROQ_API_KEY"] = userdata.get("GROQ_API_KEY")
```

### Local Environment

Set the environment variable before running the application.

**Windows PowerShell:**

```powershell
$env:GROQ_API_KEY="your_api_key_here"
```

**Python:**

```python
import os
from groq import Groq

api_key = os.environ.get("GROQ_API_KEY")

if not api_key:
    raise ValueError("Please configure the GROQ_API_KEY environment variable.")

client = Groq(api_key=api_key)
```

Use the configured client in the relevant parts of your application.

**Important:** Never publish your actual API key in a notebook, source file, screenshot, or public GitHub repository. If a real key has already been exposed, revoke it and generate a new one.

The model identifier in the code may need to be updated if the selected model is no longer available through Groq.

---

### Output
<img width="976" height="630" alt="image" src="https://github.com/user-attachments/assets/490916af-6ec7-4126-9a8f-4c01f9a5daaa" />

---

## ▶️ How to Run

### Using Google Colab

1. Open the project notebook.
2. Mount Google Drive if the datasets are stored there.
3. Install the required dependencies.
4. Configure the Groq API key securely.
5. Verify the dataset paths.
6. Run the notebook cells in order.
7. Launch the Gradio interface.
8. Open the generated interface link and interact with the application.

### Using a Local Environment

1. Clone the repository.
2. Install the dependencies.
3. Add the required datasets.
4. Configure the API key.
5. Update any dataset paths that refer to Google Drive.
6. Run the notebook or Python entry-point file.
7. Open the Gradio URL displayed in the terminal.

**Note:** The current implementation may need small adjustments before it can run locally. In particular, check the dataset paths and confirm that every referenced helper function is defined.

---

## 💡 Applications

- Exploring religious and philosophical texts.
- Educational demonstrations of semantic search and language models.
- Natural-language retrieval from text datasets.
- Multilingual information access.
- Text-based emotion classification experiments.
- Audio accessibility through text-to-speech.
- Mood-based music recommendation demonstrations.
- Academic projects involving AI and natural language processing.

---

## ⚠️ Limitations

- AI-generated responses may contain inaccuracies or misinterpret religious texts.
- Semantic search quality depends on the available data and embedding model.
- Translation accuracy may vary by language.
- Emotion detection cannot reliably determine a person's full emotional state from text alone.
- Music recommendations depend on the quality and organization of the available dataset.
- API access requires an internet connection and may be subject to usage limits.
- Dataset paths and dependencies may require configuration for different environments.
- Some helper functions referenced in the notebook may need to be implemented or verified before execution.

---

## 🔮 Future Enhancements

- Improve scripture retrieval accuracy and relevance ranking.
- Add additional languages and improve translation quality.
- Provide source references for retrieved passages and generated explanations.
- Add more robust error handling and input validation.
- Improve the user interface and mobile responsiveness.
- Expand the music recommendation system.
- Add automated tests for key components.
- Provide clearer setup instructions for local deployment.
- Improve privacy controls and secure API configuration.
- Evaluate response quality using structured test questions.

---

## 🔐 Privacy and Security

- Do not hardcode API keys in public source code.
- Store secrets in environment variables or a secure secrets manager.
- Avoid entering sensitive personal information into the application.
- Review the data handling practices of any external API before submitting user content.
- Verify the permissions and terms associated with external services and datasets.

---

## 🤝 Contributing

Contributions, suggestions, and improvements are welcome.

To contribute:

1. Fork the repository.
2. Create a new branch.
3. Make your changes.
4. Test your changes.
5. Submit a pull request describing your improvements.

Please keep contributions focused, document significant changes, and avoid committing API keys or private data.

---

## 📄 License

A license has not yet been specified for this repository.
Before publishing, choose an appropriate license and add a `LICENSE` file. Make sure the chosen license is compatible with the code and any third-party materials you redistribute.

---

## 🙏 Acknowledgements

This project uses open-source software and AI tools, including Python, Sentence Transformers, FAISS, Groq, Gradio, gTTS, Pandas, NumPy, and Scikit-learn.
Thanks to the developers and communities who maintain these tools and make AI experimentation more accessible.

---

## 👩‍💻 Author

**Project:** TrinityVerseAI

**GitHub:** [Add your GitHub repository URL here.](https://github.com/pallaamulya/TrinityVerseAI)

---

*TrinityVerseAI — Exploring spiritual knowledge through artificial intelligence.* 🕊️
