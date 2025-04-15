# Local LaTeX Writing Assistant 🖋️

**Local LaTeX Writing Assistant** is a Streamlit application designed to streamline LaTeX document creation and enhancement. The app provides three core functionalities, each implemented in separate Python modules within the `utils` directory, and supports deployment via Docker.

## Features

1. **BibTeX Conversion** (`utils/bibtex_converter.py`)
   - Convert BibTeX entries to formatted citations
   - Validate and clean BibTeX data
   - Export citations in multiple styles

2. **Markdown ↔ LaTeX Conversion** (`utils/md_latex_converter.py`)
   - Convert Markdown documents to LaTeX syntax
   - Translate LaTeX to Markdown for simplified editing
   - Preserve mathematical expressions during conversion

3. **Text Improvement** (`utils/text_improver.py`)
   - Grammar and style suggestions for LaTeX content
   - Vocabulary enhancement for academic writing
   - Context-aware rephrasing of technical text

## Installation

### Method 1: Python and Ollama

#### Prerequisites

- **Python**: Ensure Python is installed on your system. More information [here](https://www.python.org/about/gettingstarted/).
- **Ollama**: Install Ollama following the instructions [here](https://ollama.com/).

#### Steps

1. **Clone the repository**:
    ```sh
    git clone https://github.com/faouzihakimi/Local_latex_assistant.git
    cd latex-writing-assistant
    ```

2. **Install dependencies**:
    ```sh
    pip install -r requirements.txt
    ```

3. **Run the Streamlit app**:
    ```sh
    streamlit run app.py
    ```

4. **Access the app**:
    Open your browser and go to [http://localhost:8501/](http://localhost:8501/).

### Method 2: Docker and Docker Compose

#### Prerequisites

- **Docker**: Ensure Docker is installed on your system. More information [here](https://www.docker.com/get-started/).

#### Steps

1. **Clone the repository**:
    ```sh
    git clone https://github.com/faouzihakimi/Local_latex_assistant.git
    cd latex-writing-assistant
    ```

2. **Build and run the Docker containers**:
    ```sh
    docker compose up --build  # First run
    docker compose up  # Subsequent runs
    ```

3. **Pull the Ollama model**:
    In another terminal, run:
    ```sh
    docker compose exec ollama ollama pull gemma3:1b
    ```

4. **Access the app**:
    Open your browser and go to [http://localhost:8501/](http://localhost:8501/).

## File Structure

```
latex-writing-assistant/
├── app.py               # Main Streamlit application
├── requirements.txt     # Python dependencies
├── utils/
│   ├── __init__.py      # Package initialization
│   ├── bibtex_converter.py
│   ├── md_latex_converter.py
│   └── text_improver.py
├── LICENSE              # The MIT license
└── README.md            # This documentation
```

## Contributing

Contributions are welcome! Please open an issue or submit a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

This version includes clearer section headings, more detailed installation steps, and improved formatting for better readability.

## License  
This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.  

*Disclaimer: This app processes text locally - no data leaves your machine.*  
