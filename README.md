# Assistant Chat Demo

This demo project tests out OpenAI's Assistants API, particularly the tools integration. Currently it's setup to provide answer related to the Quasar Framework, which is the framework used for the frontend:

https://github.com/jems624/assistants-poc/assets/142084868/8b0f0a66-409f-42be-8c53-e7fd2ae3b441

Although it can easily customized for other purposes.

> **Note**: This project is meant for demo purposes only. It lacks a lot of security features such as API authentication and input/output sanitization and validation . DO NOT deploy to production!

## Customization

### Preset Questions

The preset questions (the 4 questions displayed at the start) can be changed on the frontend, in the file `src/pages/IndexPage.vue`, which is where most of the code that drives the UI can be found.

### Assistant

To change the assitant. you need to update the `OPENAI_API_KEY ` and `OPENAI_ASSISTANT_ID` environment variables to point to the desired assistant.

Refer to the backend README for information.

### Tools

Currently it supports 2 tools: `download_webpage` and `get_search_results` which, as the names imply, are used to download the HTML content from a webpage and fetch the top search results given a set of keywords. For the assistant to use these tools, a corresponding function of the same name must be defined on the assistant.

You can add more tools by defining a function with the same name in `app/tools.py` on the backend. The function must also be named after the tool defined on the assistant.

See the backend README for more information.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
