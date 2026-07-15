# ask-my-notes — RAG on your own notes

The exact pipeline from lab01-lab03, pointed at a personal folder of notes instead of a single PDF — course notes, saved articles, revision sheets, all queryable in plain language, with new files indexed automatically.

## What it does

- Indexes every `.md` and `.pdf` file in a notes folder on first run
- `watch.py`: a background file watcher (`watchdog`) that indexes new or changed files automatically
- `find-contradictions` mode: compares two sources on the same topic — useful for spotting conflicting explanations across papers
- Minimal Streamlit UI: search bar, history, source tags
- `ask.py`: a CLI for quick one-off questions without opening the UI

## Real usage

During the program, every course note becomes queryable. "Remind me how the reranker we built in S3 works" → instant answer, sourced from your own notes.

## Stack

Python 3.11 · LangChain · ChromaDB · watchdog · Streamlit · Mistral API
