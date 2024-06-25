# Google Generative AI Client with Node.js

This project demonstrates how to set up a client to interact with Google's Generative AI models using Node.js. The implementation leverages the `@google/generative-ai` package to make API calls and query the AI model for content generation.

## Tech Stack

- Node.js
- Google Generative AI API
- Google Cloud Platform

## Project Highlights

- **Environment Setup**: Initialized a Node.js project and configured it to use Google Cloud's generative AI services.
- **API Integration**: Utilized the `@google-cloud/aiplatform` library to interact with AI models.
- **Model Querying**: Successfully queried the AI model to generate content like the top 10 programming languages in 2022.

## Getting Started

Follow these steps to get the project up and running on your local machine.

### Prerequisites

- Node.js installed on your machine.
- A Google Cloud project with the necessary APIs enabled.
- Service account credentials downloaded as a JSON file.

### Installation

1. **Clone the repository**:
    ```bash
    git clone https://github.com/your-username/google-generative-ai-client.git
    cd google-generative-ai-client
    ```

2. **Install dependencies**:
    ```bash
    npm install
    ```

3. **Set up authentication**:
    - Ensure the `GOOGLE_APPLICATION_CREDENTIALS` environment variable is set to the path of your service account JSON file.
    ```bash
    export GOOGLE_APPLICATION_CREDENTIALS="/path/to/your/service-account-file.json"
    ```

4. **Update `package.json`**:
    - Add `"type": "module"` to your `package.json` file.

    ```json
    {
      "name": "google-generative-ai-client",
      "version": "1.0.0",
      "description": "",
      "main": "index.js",
      "type": "module",
      "scripts": {
        "start": "node index.js"
      },
      "author": "",
      "license": "ISC",
      "dependencies": {
        "@google/generative-ai": "^1.0.0"
      }
    }
    ```

5. **Create `index.js`**:
    ```javascript
    import { GoogleGenerativeAI } from "@google/generative-ai";

    const genai = new GoogleGenerativeAI("YOUR_API_KEY");

    const model = genai.getGenerativeModel({
        model: "gemini-1.5-pro"
    });

    async function main() {
        const response = await model.generateContent("top 10 programming languages in 2022");
        console.log(response);
    }

    main();
    ```

### Running the Project

1. **Run the application**:
    ```bash
    npm start
    ```

## Contributing

If you would like to contribute to this project, please fork the repository and submit a pull request. For major changes, please open an issue first to discuss what you would like to change.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

### Contact

If you have any questions or suggestions, feel free to reach out.

---

#AI #MachineLearning #NodeJS #GoogleCloud #GenerativeAI #Programming #Tech
