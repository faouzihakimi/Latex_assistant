# Local LaTeX Writing Assistant 🖋️  

**Local LaTeX Writing Assistant** is a Streamlit application designed to streamline LaTeX document creation and enhancement. The app provides three core functionalities, each implemented in separate Python modules within the `utils` directory, and supports deployment via Docker.  


## Features  
**1. BibTeX Conversion** (`utils/bibtex_converter.py`)  
- Convert BibTeX entries to formatted citations  
- Validate and clean BibTeX data  
- Export citations in multiple styles  

**2. Markdown ↔ LaTeX Conversion** (`utils/md_latex_converter.py`)  
- Convert Markdown documents to LaTeX syntax  
- Translate LaTeX to Markdown for simplified editing  
- Preserve mathematical expressions during conversion  

**3. Text Improvement** (`utils/text_improver.py`)  
- Grammar and style suggestions for LaTeX content  
- Vocabulary enhancement for academic writing  
- Context-aware rephrasing of technical text  


## Installation  
```
# Clone repository  
git clone https://github.com/yourusername/latex-writing-assistant.git  
cd latex-writing-assistant  

# Install ollama
More information here : [Ollama](https://ollama.com/)

# Install dependencies  
pip install -r requirements.txt  
```  

## Usage  
Run the Streamlit app:  
```
streamlit run app.py  
```  
Access to the app with this link: http://localhost:8501/

## Installation with docker and docker-compose

First run the following command in a terminal (docker must be installed):

```
docker compose up --build #if it is the first run
docker compose up #otherwise
``` 
In another terminal (the other one must stay open), run the following command:

```
docker compose exec ollama ollama pull gemma3:1b
```
Access to the app with this link: http://localhost:8501/

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
├── LICENCE           # The MIT licence 
└── README.md            # This documentation  
```  


## License  
This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.  

*Disclaimer: This app processes text locally - no data leaves your machine.*  
