# 📝 MCQ Master - Streamlit

A simple Streamlit application that reads MCQs from a Microsoft Word `.docx` file, displays them as an online quiz, and calculates the result.

## Files

```text
mcq-master/
├── app.py
├── requirements.txt
└── README.md
```

## Word document format

The application expects each MCQ to contain:

```text
1. What is ...?
A. Option one
B. Option two
C. Option three
D. Option four
Answer: B
```

It also accepts question formats such as `1)`, `Q1.`, and `Question 1:`.

The parser requires all four options A-D and a valid answer A-D.

## Run locally

Use Python 3.10, 3.11, or 3.12.

```bash
pip install -r requirements.txt
streamlit run app.py
```

## Deploy on Streamlit Community Cloud

1. Create a GitHub repository.
2. Put `app.py`, `requirements.txt`, and `README.md` in the repository root.
3. In Streamlit Community Cloud, create/deploy the app.
4. Select `app.py` as the main file.
5. After changing files, commit/push the changes and reboot the app if necessary.

## Important

Do not name the main file `app (5).py`. Use exactly:

```text
app.py
```

The package name in `requirements.txt` must be:

```text
python-docx==1.1.2
```

The Python import is:

```python
from docx import Document
```
