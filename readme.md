# awesome-hci-chatbot [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of chatbot projects useful for HCI research


## Contents

- [ChatGPT](#chatgpt)
<!-- - [Another Section](#another-section) -->


## ChatGPT

ChatGPT implementations.

- [Node.js + TypeScript starter](https://github.com/tlylt/chatgpt-server-demo)
- [Node.js API server starter](https://github.com/waylaidwanderer/node-chatgpt-api)
  <details>
  <summary><strong>How to setup</strong></summary>
  
  The `node-chatgpt-api` project does provide a primitive ChatGPT API server out of the box, (simulating ChatGPT with the OpenAI's completion API using the text-davinci-003 model).

  To set it up, just need to:
  - Clone this repository: `git clone https://github.com/waylaidwanderer/node-chatgpt-api`
  - Install dependencies with `npm ci`
  - Rename `settings.example.js` to `settings.js` in the root directory
    - Fill in the OPENAI_API_KEY in line 10
    - Uncomment line 18 and update the model to "text-davinci-003"
  - Start the server: `npm start`
  - Send a JSON request with the body of {"message": "Something to ChatGPT"}to `http://localhost:3000/conversation`

  E.g. using curl:
  ```bash
  curl -i -X POST \
     -H "Content-Type:application/json" \
     -d \
  '{
      "message": "Hello, how are you today?"
  }' \
   'http://localhost:3000/conversation'
  ```

  Sample response:
  ```json
  {
      "response": "Hello there! I'm doing great today. How can I help you?",
      "conversationId": "e163b2d3-5293-4ce6-940a-3d8fd9441ff9",
      "messageId": "a65a602e-6a5e-4f41-bd48-093509d97d82",
      "details": {
          "id": "cmpl-6mhoAzDzzbUvUD7kQPw1k3UMnm2DI",
          "object": "text_completion",
          "created": 1677066162,
          "model": "text-davinci-003",
          "choices": [
              {
                  "text": "Hello there! I'm doing great today. How can I help you?",
                  "index": 0,
                  "logprobs": null,
                  "finish_reason": "stop"
              }
          ],
          "usage": {
              "prompt_tokens": 68,
              "completion_tokens": 15,
              "total_tokens": 83
          }
      }
  }
  ```
  </details>

<!-- ## Another Section

### Subsection

- [List item](http://example.com)
- [List item](http://example.com) -->


## Contribute

Contributions welcome! Read the [contribution guidelines](contributing.md) first.
