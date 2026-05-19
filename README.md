# Final Project

A Flask web application that uses the IBM Watson NLP Library to detect emotions from text input. The application analyzes text and returns scores for five emotions: anger, disgust, fear, joy, and sadness, along with the dominant emotion.

## Purpose

This project was built as a final project for the IBM AI Application Development course on Coursera. It demonstrates how to integrate a Watson NLP API into a Python web application with error handling, unit testing, and static code analysis.

## Features

- Detects five emotions from any text input: **anger**, **disgust**, **fear**, **joy**, and **sadness**
- Identifies the **dominant emotion** (highest score)
- Handles blank/invalid input with a user-friendly error message
- Web interface accessible via browser at `localhost:5000`
- REST endpoint at `/emotionDetector?textToAnalyze=<your text>`

## Project Structure

```
final_project/
├── EmotionDetection/
│   ├── __init__.py
│   └── emotion_detection.py
├── static/
│   └── mywebscript.js
├── templates/
│   └── index.html
├── server.py
├── test_emotion_detection.py
└── README.md
```

## Requirements

- Python 3.x
- Flask
- Requests

Install dependencies:

```bash
pip install flask requests
```

## How to Run

1. Clone the repository:

```bash
git clone https://github.com/pabloquiroz/final_project.git
cd final_project
```

2. Start the Flask server:

```bash
python3 server.py
```

3. Open your browser and go to:

```
http://localhost:5000
```

4. Enter any text in the input field and click **Run Sentiment Analysis** to see the emotion scores and dominant emotion.

## API Usage

You can also call the endpoint directly:

```bash
curl "http://localhost:5000/emotionDetector?textToAnalyze=I love this new technology"
```

Example response:

```
For the given statement, the system response is 'anger': 0.006274985, 'disgust': 0.0025598293, 'fear': 0.009251528, 'joy': 0.9680386 and 'sadness': 0.049744144. The dominant emotion is joy.
```

## Running Unit Tests

```bash
python3 -m unittest test_emotion_detection.py -v
```

The test suite covers all five dominant emotions with predefined statements.

## Error Handling

If the input is blank or invalid, the application returns:

```
Invalid text! Please try again.
```

## Static Code Analysis

The code achieves a **10/10 PyLint score**:

```bash
pylint server.py
```
