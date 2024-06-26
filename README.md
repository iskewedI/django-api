# Django-API Learning Project

Welcome to the Django-API Learning Project! This project was created as a part of a learning exercise after completing a small course on Django. It demonstrates how to set up a basic API using Django, including creating and querying records for two entities: `Question` and `Choice`.

## Table of Contents

- [Getting Started](#getting-started)
- [Installation](#installation)
- [Usage](#usage)
- [Entities](#entities)
  - [Question](#question)
  - [Choice](#choice)
- [Documentation](#documentation)

## Getting Started

These instructions will help you set up and run the project on your local machine for development and testing purposes.

### Prerequisites

- Python 3.x
- Django
- Django REST framework

### Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/yourusername/django-api-learning-project.git
   cd django-api-learning-project
   ```
2. **Create a virtual environment:**
  ```bash
  python -m venv venv
  source venv/bin/activate  # On Windows use `venv\Scripts\activate`
  ```
3. **Install the dependencies:**
  ```bash
  pip install -r requirements.txt
  ```
3. **Apply the migrations:**
  ```bash
  python manage.py migrate
  ```
4. **Run the server:**
  ```bash
  python manage.py runserver
  ```

## Usage

Once the server is running, you can access the API at `http://127.0.0.1:8000/`. Use tools like `curl` or Postman to interact with the API.

### Creating a Question

To create a `Question`, send a POST request to `http://127.0.0.1:8000/questions/` with the following payload:

```json
{
  "question_text": "What is your favorite programming language?",
  "pub_date": "2023-06-26T12:00:00Z"
}
```
### Creating a Choice

To create a `Choice`, send a POST request to `http://127.0.0.1:8000/choices/` with the following payload:

```json
{
  "question": 1,
  "choice_text": "Python",
  "votes": 0
}
```

## Entities

### Question

A `Question` entity represents a question that can have multiple choices.

- `question_text`: The text of the question.
- `pub_date`: The publication date of the question.

### Choice

A `Choice` entity represents a possible answer to a question.

- `question`: The ID of the related question.
- `choice_text`: The text of the choice.
- `votes`: The number of votes this choice has received.

## Documentation

Detailed explanations and documentation are provided in the `/docs` directory.

- **General Explanations:** `/docs`
- **Database Queries:** `/docs/db.md`
