
#  WhatsApp Chat Analyzer

A lightweight, efficient Python tool designed to analyze exported WhatsApp chat data. This program processes message histories to uncover communication patterns, calculate response speeds, identify behavioral archetypes, and visualize group trends using data science fundamentals.

To master both high-level data pipelines and low-level engineering logic, this analyzer was built using **two distinct implementations**:
1. **The Vectorized Pipeline:** Powered by `Pandas`, `Seaborn`, and regular expressions (`re`) for high-speed data manipulation.
2. **The Pure Logic Engine:** Built using *only* core Python concepts (built-in lists, dictionaries, loops, and conditional statements) without external data-frame dependencies.

---

##  Key Features & Archetypes

* **Behavioral Personality Matrix:** Dynamically maps group members to specific archetypes:
  * 🚀 **Spammer:** High text volume, rapid short messages.
  * 🦉 **Night Owl:** High text activity between 11 PM and 4 AM.
  * 👑 **Drama Queen:** Frequent use of expressive punctuation (`!`, `?`).
  * 📖 **Story Teller:** Writes long, paragraph-style descriptions.
  * 👻 **Ghost:** Extremely low message frequency or long silence windows.
* **True Silence Tracking:** Accurately computes the maximum time window a user goes completely silent, accounting for intervals between their own texts as well as their total time away up to the final chat timestamp.
* **Response Time Dynamics:** Tracks cross-talk reply speed between different senders while filtering out self-double-texts and long inactive gaps (>30 minutes) to keep metrics clean.
* **Smart Word Frequency Tracking:** Normalizes strings and cleans background tags or stop-words (e.g., *the, is, media omitted*) to pinpoint the group's actual favorite words.
* **Data Visualizations:** Built-in `Matplotlib` and `Seaborn` integrations to render clean, interactive distribution plots inside notebooks.

---

##  Sample Visualizations

The program auto-generates dual-plot insights to evaluate user participation metrics at a glance:

1. **Group Member Activity & Personality Distribution** — A clustered bar plot tracking total text volumes colored dynamically by assigned personality roles.
2. **Top 10 Group Chat Words** — A frequency ranking chart highlighting the group's core conversational vocabulary.

---

##  Tech Stack & Concepts Used

* **Core Programming:** Python (Lists, Nested Loops, Dictionaries, Text File I/O Parsing)
* **Data Analysis:** Pandas, NumPy
* **Data Visualization:** Matplotlib, Seaborn
* **Text Processing:** Regular Expressions (`re`), String Vectorization, Natural Language Stopwords Filtering

---

##  Getting Started

### Prerequisites
Make sure you have Python installed, along with the required libraries for graphing:
```bash
pip install pandas matplotlib seaborn
