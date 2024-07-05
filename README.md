# GraphRAG: Enhanced Retrieval-Augmented Generation

## Introduction

GraphRAG is an innovative approach to Retrieval-Augmented Generation (RAG) developed by Microsoft Research. It addresses the limitations of traditional RAG methods by employing advanced techniques for processing and retrieving information from complex documents.

### Why use GraphRAG?

1. **Improved Accuracy**: GraphRAG excels at linking related information across different documents, enhancing the accuracy of responses to complex queries.

2. **Better Summarization**: It captures the overall essence of lengthy documents more effectively than baseline RAG methods.

3. **Hierarchical Understanding**: GraphRAG organizes information into a community hierarchy, allowing for more nuanced and context-aware retrieval.

4. **Comprehensive Insights**: By combining global searches with local entity networks, GraphRAG provides more thorough and relevant answers.

## Getting Started
Follow these steps to set up and run GraphRAG:

### 1. Installation

Install GraphRAG using pip:

```bash
pip install graphrag
```

### 2. Set up API Key

Export your OpenAI API key as an environment variable:
```bash
export GRAPHRAG_API_KEY="$OPENAI_API_KEY"
```

### 3. Prepare Input Data

Create an input folder and insert the text file you want to analyze. You can find sample text files in this repository.

### 4. Initialize GraphRAG

Run the following command to initialize GraphRAG in your current directory:
```bash
python -m graphrag.index --init --root .
```
### 5. Index Your Data

Index the data in your input folder:
```bash
python -m graphrag.index --root .
```

### 6. Query Your Data
   
Now you can query your indexed data. For example:
```bash
python -m graphrag.query --root . --method local "what is the gross profit of this year for FORD?"
```

Replace the query text with your own question as needed.
