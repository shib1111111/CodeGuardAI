# CodeGuard AI 

CodeGuard AI  is a complete MERN stack project that leverages Google Generative AI to analyze and review your code. This tool automatically inspects code for quality, best practices, performance, and security while suggesting improvements and refactorings to help developers write clean and efficient code.

## Overview

- **AI-Driven Analysis:** Utilizes Google Generative AI to provide detailed reviews of submitted code snippets.
- **Full MERN Stack:** Combines an Express backend with a React-based frontend for a seamless development experience.
- **User-Friendly Interface:** Features a live code editor with syntax highlighting and Markdown-rendered review output.
- **Customizable Reviews:** System instructions define the reviewer as a seasoned developer with 7+ years of experience to ensure feedback is both practical and constructive.

## Tech Stack

- **Backend:** Node.js, Express
- **AI Integration:** Google Generative AI API
- **Frontend:** React, Axios, react-simple-code-editor, PrismJS, React Markdown, rehype-highlight
- **Middleware:** CORS for handling cross-origin requests

## Installation

### Backend Setup

1. **Clone the Repository**
   ```bash
   git clone https://github.com/shib1111111/AI-Powered-Code-Reviewer.git
   cd AI-Powered-Code-Reviewer
   ```

2. **Install Backend Dependencies**
   ```bash
   npm install
   ```

3. **Configure Environment Variables**

   Create a `.env` file in the root directory and add your Google Generative AI key:
   ```env
   GOOGLE_GEMINI_KEY=your_google_gemini_api_key_here
   ```

4. **Run the Backend Server**
   ```bash
   npm start
   ```
   The server will start (defaulting to port 3000) and expose the API endpoint for code reviews.

### Frontend Setup

1. **Navigate to the Frontend Directory**  
   If your frontend code is located in a separate folder (e.g., `/Frontend`), navigate there:
   ```bash
   cd Frontend
   ```

2. **Install Frontend Dependencies**
   ```bash
   npm install
   ```

3. **Run the Frontend Application**
   ```bash
   npm start
   ```
   The React application will launch in your browser, typically on [http://localhost:3000](http://localhost:3000) (or another port if configured differently).

## How It Works

### Backend

- **API Endpoint:**  
  - **POST** `/ai/get-review`  
    Receives a JSON payload containing the code snippet to review.  
    Example request body:
    ```json
    {
      "code": "function sum() { return 1 + 1 }"
    }
    ```
  - The endpoint uses the AI service to analyze the provided code and returns a detailed review.

- **AI Service Integration:**  
  The backend integrates with Google Generative AI using a detailed system instruction that frames the reviewer as a senior developer. This service:
  - Checks for code quality and adherence to best practices.
  - Detects performance issues, security risks, and maintainability concerns.
  - Provides a clear, constructive review with suggestions and example fixes.

### Frontend

- **Interactive Code Editor:**  
  The frontend features a code editor built with [react-simple-code-editor](https://www.npmjs.com/package/react-simple-code-editor) and [PrismJS](https://prismjs.com/) for syntax highlighting. Users can:
  - Write or paste code directly into the editor.
  - See syntax highlighting in real time.

- **Review Button:**  
  A "Review" button triggers an API call using Axios to send the code to the backend for analysis.

- **Markdown Rendered Feedback:**  
  The review response is rendered in Markdown using [React Markdown](https://github.com/remarkjs/react-markdown) along with [rehype-highlight](https://github.com/rehypejs/rehype-highlight) for proper code formatting. This ensures that the feedback is easy to read and understand.

- **Live Preview:**  
  The layout splits the screen into two sections:
  - The left side displays the code editor.
  - The right side shows the formatted review output in Markdown.

## Contributing

Contributions are welcome! If you have suggestions, improvements, or bug fixes, please open an issue or submit a pull request. Follow standard GitHub contribution guidelines.

## License

This project is licensed under the [MIT License](LICENSE).


<em style="color: #ff66b2; font-weight: bold;">✨ --- Designed & made by Shib Kumar Saraf ✨</em>
