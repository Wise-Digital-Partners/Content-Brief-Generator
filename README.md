Content Brief Generator
=======================

This Streamlit application uses Google's Gemini Pro model to generate comprehensive content briefs for writers and content strategists. You provide the core details of your content, and the app generates a structured brief to guide the content creation process.

How to Run the Application
--------------------------

### 1\. Prerequisites

-   Python 3.7+ installed on your system.

-   A Google API key with access to the Gemini model. You can obtain one from [Google AI Studio](https://aistudio.google.com/ "null").

### 2\. Setup

**a. Clone the repository or download the files.**

**b. Create a virtual environment (recommended):**

```
python -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`

```

**c. Install the required libraries:**

```
pip install -r requirements.txt

```

**d. Set up your API Key:**

You need to set your Google API key as an environment variable.

-   **For macOS/Linux:**

    ```
    export GOOGLE_API_KEY="YOUR_API_KEY_HERE"

    ```

-   **For Windows (Command Prompt):**

    ```
    set GOOGLE_API_KEY="YOUR_API_KEY_HERE"

    ```

-   **For Windows (PowerShell):**

    ```
    $env:GOOGLE_API_KEY="YOUR_API_KEY_HERE"

    ```

    **Note:** This environment variable is only set for the current terminal session. For a permanent solution, you'll need to add it to your system's environment variables.

### 3\. Launch the App

Once the setup is complete, run the following command in your terminal:

```
streamlit run app.py

```

Your web browser should open with the application running.

How to Use the App
------------------

1.  **Fill in the form fields** on the main page with your content requirements:

    -   **Main Topic / Primary Keyword**: The central theme of your content (this is required).

    -   **Supporting Keywords**: Any secondary keywords to include.

    -   **Tone of Voice**: The desired style of writing.

    -   **Requested Word Count**: The target length of the article.

    -   **Page Type**: The format of the content (e.g., blog post, landing page).

    -   **Primary User Intent**: The main goal of the user searching for this topic.

2.  Click the "**Generate Content Brief**" button.

3.  The application will send your requirements to the Gemini model and display the generated content brief on the page.

File Structure
--------------

-   `app.py`: The main Streamlit application script. It contains the UI and logic for calling the AI model.

-   `prompts.py`: Contains the detailed prompt template sent to the Gemini model. This keeps the main application code clean.

-   `requirements.txt`: A list of Python packages required to run the application.

-   `README.md`: This file, providing setup and usage instructions.
