# LectureMate

**LectureMate** is an AI-powered tool designed to transform lecture files (such as .txt, .pdf, or other text-based formats) into concise, easy-to-understand notes. Powered by OpenAI’s GPT API, it simplifies the process of digesting large amounts of information, making it ideal for students, professionals, and anyone looking to quickly grasp key concepts from their study or work materials.

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Example](#example)
- [API Integration](#api-integration)
- [Contributing](#contributing)
- [License](#license)

## Overview

LectureMate is a productivity tool that uses AI to extract important points from lecture materials and generates concise summaries. Whether you're a student reviewing class notes or a professional looking to quickly understand lengthy documents, LectureMate helps you save time and focus on the core concepts.

## Features

- **AI-Powered Summarization**: Uses GPT API to summarize lecture notes and documents.
- **Text Input Flexibility**: Supports various text-based file formats like `.txt` and `.pdf`.
- **Customizable Summaries**: Allows customization of summarization level based on user preference.
- **Easy-to-Use Interface**: Simple input/output workflow for generating summaries.
  
## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/LectureMate.git
    cd LectureMate
    ```

2. Install the required Python packages:
    ```bash
    pip install -r requirements.txt
    ```

3. Set up your OpenAI API key:
   - Create a `.env` file in the project root and add your API key:
     ```bash
     OPENAI_API_KEY=your_openai_api_key_here
     ```

## Usage

To use LectureMate, follow these steps:

1. Prepare your lecture files in `.txt` format (support for other formats such as `.pdf` can be added later).
2. Run the script:
   ```bash
   python lecturemate.py --file your_lecture_file.txt

### Command-Line Arguments

- `--file`: The path to your lecture file.
- `--length`: Optional parameter to adjust the length of the summary (short, medium, detailed).

### Example

Here’s an example of how LectureMate processes a `.txt` file:

**Input:**
```plaintext
Lecture Topic: Artificial Intelligence
Artificial Intelligence is the simulation of human intelligence in machines...
```

**Output:**
```
**Summary:**
- AI refers to simulating human intelligence in machines.
- Core areas include machine learning, natural language processing, and robotics.


```
### API Integration

LectureMate uses OpenAI's ChatGPT API to process text and generate summaries. The API is called within the code as follows:

```python
response = openai.ChatCompletion.create(
  model="gpt-4",
  messages=[
    {"role": "system", "content": "You are a helpful assistant."},
    {"role": "user", "content": "Summarize the following lecture..."}
  ]
)
```
Ensure you have your API key in the environment as specified above.

### Contributing

Contributions are welcome! If you'd like to contribute to LectureMate, feel free to fork the repository and submit a pull request.

**Steps to Contribute:**
1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes.
4. Commit your changes (`git commit -m 'Add some feature'`).
5. Push to the branch (`git push origin feature-branch`).
6. Open a pull request.
