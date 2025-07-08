# AI Travel Agent Setup

This notebook sets up and runs the **AI Travel Agent** application in Google Colab. The AI Travel Agent is designed to assist with travel planning by integrating flight and hotel information and offering recommendations via an interactive interface.

## Features:
- **Flight Search**: Finds flight details including airlines, departure/arrival information, and prices using **SerpAPI**.
- **Hotel Search**: Retrieves hotel recommendations, including price, ratings, and links to booking sites using **SerpAPI**.
- **Email Notifications**: Sends travel-related information directly to users' emails via **SendGrid**.
- **Gradio Interface**: Allows users to input travel queries and get instant results on a web interface.

## Requirements:
Before running the notebook, make sure you have the following:
- **Google Colab** for easy setup and cloud execution.
- **SerpAPI** and **SendGrid** accounts to use their APIs.
- **Python 3.x** installed.

## Setup Instructions

### Step 1: Install Dependencies
To install the necessary libraries, run the following command in your terminal or within a notebook:

Step 2: Set Up Environment Variables
Create a .env file in the root directory of your project and add the following keys:

SERPAPI_API_KEY=your_serpapi_api_key
SENDGRID_API_KEY=your_sendgrid_api_key
Replace your_serpapi_api_key with your SerpAPI key and your_sendgrid_api_key with your SendGrid API key.

### Step 3: Write the travel_app.py Script to Disk
Once the dependencies are installed, you can write the necessary Python script (travel_app.py) using the following code:

# Code to write the travel app Python script to disk goes here
Step 4: Launch the Streamlit App
Run the Streamlit app by executing this command:
streamlit run travel_app.py
This will start the app and provide you with a public URL that you can open in any browser.

## Workflow

The **AI Travel Agent** works by interacting with the following tools:

### Flights Finder:
- Takes the departure and arrival airport codes, dates, and passenger details.
- Uses **SerpAPI** to search Google Flights for available options.

### Hotels Finder:
- Takes the location, check-in/check-out dates, and number of rooms and guests.
- Uses **SerpAPI** to search Google Hotels for suitable hotels.

### Email Sender:
- Sends the travel details to the provided recipient's email via **SendGrid**.

### Gradio Interface:
- Accepts user input for travel queries (e.g., “Flights from New York to London June 10–15, and 4-star hotels”).
- Displays the results on a **Gradio** interface, where users can interactively query and get travel details.


### Use Cases
- Flight and Hotel Search: Quickly find detailed information for flights and hotels based on travel queries.

- Personalized Travel Recommendations: Get customized travel recommendations based on user preferences.

- Email Notifications: Receive travel information directly to your inbox for future reference.

### Project Benefits
- Automation: Automates the process of gathering flight and hotel information.

- Convenience: Easy-to-use web interface for quick travel planning.

- Personalization: Provides tailored travel suggestions and recommendations.

- Email Notifications: Results are sent directly to the user's email.

### Future Work
- Integration with Other Travel APIs: Add support for more travel service providers to improve functionality.

- Improved User Interface: Enhance the Gradio interface for better user experience and additional features.
```bash
pip install gradio serpapi sendgrid python-dotenv langchain langgraph
