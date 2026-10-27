# Medical Chatbot with Retrieval-Augmented Generation

An INFO 629 Applied AI course project by Christine Ikponmwonba at Drexel University, separate from doctoral research.

This notebook compares an original-prompt LLM baseline, an improved prompt without retrieval, and the improved prompt with RAG. It uses GPT-4o-mini, sentence-transformer embeddings, and FAISS retrieval over 50,000 doctor responses from the HealthCareMagic dataset.

## Evaluation

The project compares the same 20 questions using LLM-as-judge scores and ROUGE; a manual HCI rubric evaluates 10 responses per configuration. The improved prompt scored highest on the LLM-judge evaluation, while RAG scored highest on the manual HCI rubric. The small sample and single non-clinical evaluator limit interpretation. This is an educational prototype, not a clinically validated tool or medical service.

## Run locally

1. Create a Python environment and install `requirements.txt`.
2. Set `CHATBOT_API_KEY` in your environment. Never paste credentials into the notebook or commit them.
3. Open `medical-chatbot-rag.ipynb` in Jupyter and run cells in order.

Running the notebook downloads the dataset and embedding model, computes embeddings, and makes paid OpenAI API calls for generation and evaluation. Review the cells before running. Gradio's `share=True` creates a temporary public demo; it is not permanent hosting.

Dataset: https://huggingface.co/datasets/wangrongsheng/HealthCareMagic-100k-en

The dataset, embeddings, generated responses, API credentials, and saved notebook outputs are excluded from this repository. Source notebook outputs were cleared and credential assignments replaced with environment-variable access. Dependencies and end-to-end execution have not been tested in this preparation environment.

## Portfolio

https://ikchristine.github.io/

No working permanent demo URL is currently available.
