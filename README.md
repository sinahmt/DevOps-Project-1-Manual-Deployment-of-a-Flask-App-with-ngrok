# Manual Deployment of a Flask App with ngrok

## Overview

This repository documents the initial steps in learning DevOps by manually deploying a simple Flask web application and making it accessible via a temporary public URL using ngrok.

## Setup Instructions (Local Development)

1.  **Clone the Repository:**
    ```bash
    git clone https://github.com/sinahmt/DevOps-Project-1-Manual-Deployment-of-a-Flask-App-with-ngrok.git

    cd DevOps-Project-1-Manual-Deployment-of-a-Flask-App-with-ngrok
    ```

2.  **Create a Virtual Environment:**
    ```bash
    python3 -m venv venv
    ```

3.  **Activate the Virtual Environment:**
    ```bash
    source venv/bin/activate
    ```

4.  **Install Flask:**
    ```bash
    pip install Flask
    ```

5.  **Run the Flask Application:**
    ```bash
    python app.py
    ```
    This will start the Flask development server, usually accessible at `http://127.0.0.1:5000/`.

## Deployment (via ngrok for temporary public access)

This section describes how to temporarily expose the local Flask application to the internet using ngrok.

1.  **Download and Install ngrok:**
    * Follow the instructions on the official ngrok website: [https://ngrok.com/download](https://ngrok.com/download) for your operating system.

2.  **Run ngrok:**
    * Open a new terminal window (while your Flask application is still running).
    * Run the command:
        ```bash
        ngrok http 5000
        ```

3.  **Access via ngrok URL:**
    * Examine the output in the ngrok terminal. You will see "Forwarding" URLs (both `http://` and `https://`).
    * Open a web browser and navigate to one of the provided ngrok URLs to access your "Hello from Flask!" application.

**Note:** The ngrok URL is temporary and will change each time you run ngrok (unless you have a paid account with reserved domains). Keep the ngrok terminal window running as long as you want your application to be publicly accessible.

## Repository Contents

* `app.py`: The basic Flask web application code.
* `README.md`: This documentation file.
* `LICENSE`
