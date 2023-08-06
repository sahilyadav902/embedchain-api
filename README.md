# embedchain-api

## Docker Setup

- Open variables.env, and edit it to add your Open AI API Key.
- To setup your api server using docker, run the following command inside this folder using your terminal.
```bash
docker-compose up --build
```

## Usage
- Your api server is running on [http://localhost:5000/](http://localhost:5000/)
- Make an api call to the endpoints `/add` and `/query` using the formats discussed below:

### /add
- This endpoint allows you to add data sources to the chatbot. It expects a POST request with JSON data containing data_type and url_or_text fields.
- Request json format:
```json
{
  "data_type": "your_data_type_here",
  "url_or_text": "your_url_or_text_here"
}
```
- Response json format:
```json
{
  "data": "Added data_type: url_or_text"
}
```

### /query
- This endpoint allows you to query the chatbot with a question. It expects a POST request with JSON data containing a question field.
- Request json format:
```json
{
  "question": "your_question_here"
}
```
- Response json format:
```json
{
  "data": "your_answer_here"
}
```