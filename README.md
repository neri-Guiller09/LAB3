FastAPI API Development with JSON Handling

Overview

This repository contains an API developed using FastAPI. The API provides an endpoint that retrieves detailed posts of a specific user, including all comments per post. The implementation focuses on JSON parsing, data traversal, and conversion of Python data structures into valid JSON format.

Features

Developed using FastAPI.

Parses JSON strings and traverses nested data.

Converts Python data structures into a valid JSON format.

Retrieves user posts and associated comments using a GET request.

Provides Swagger UI for API testing.

Installation

To set up and run this FastAPI application, follow these steps:

Prerequisites

Python 3.8 or later

pip (Python package installer)

Steps

1. Clone the repository:
``` bash
git clone https://github.com/yourusername/your-repository.git
cd your-repository/lab3
```
2. Create a virtual environment (optional but recommended):
``` bash
python -m venv .venv
source .venv/bin/activate  # On macOS/Linux
.venv\Scripts\activate     # On Windows
```
3. Install dependencies:
``` bash
pip install -r requirements.txt
```
**Running the Application**

1. Start the FastAPI server:
``` bash
uvicorn main:app --reload
```
2. Open your browser or use a tool like Postman to test the API at:
``` bash
http://127.0.0.1:8000
```
**API Endpoints**
``` bash
GET /detailed_post/{userID}
```
Request:

userID: Integer value representing the user's ID.

Response:

If user exists:
``` bash
{
  "user_id": 1,
  "posts": [
    {
      "post_id": 101,
      "post_title": "Post Title",
      "comments": [
        {
          "comment_id": 201,
          "comment_text": "This is a comment."
        }
      ]
    }
  ]
}
```
If user not found:
``` bash
{
  "error": "User not found"
}
```
Dependencies

This project requires the following dependencies, listed in requirements.txt:

FastAPI

Uvicorn

Testing

You can test the API using the built-in Swagger UI provided by FastAPI:
``` bash
Open http://127.0.0.1:8000/docs in your browser.
```
Try the GET /detailed_post/{userID} endpoint.

Required Output

Updated main.py file containing the API code.

requirements.txt file listing dependencies.

Screenshot of Swagger UI.

Author

[[Guiller Neri] - Your GitHub Profile](https://github.com/neri-Guiller09)

Repository Link https://github.com/neri-Guiller09/LAB3
