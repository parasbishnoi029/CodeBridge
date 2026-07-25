
# CodeBridge 🌉

An AI-powered IDE extension that automatically translates legacy codebases into modern frameworks, cutting migration time in half.

---

## 💡 Inspiration
Legacy code is everywhere, and migrating it to modern frameworks is one of the most tedious, error-prone tasks a developer faces. We realized that while large language models (LLMs) are great at writing net-new code, they struggle with large-scale refactoring because they lose context. We wanted to build a tool that makes modernizing legacy systems — whether it's updating outdated Python scripts or moving from an old JavaScript framework to React — as seamless as possible without breaking the underlying logic.

## 💻 What it does
CodeBridge is an AI-powered IDE extension that automates the modernization of legacy codebases directly inside Visual Studio Code.
* **Context-Aware Translation:** Select a file or folder, and CodeBridge analyzes the code to map legacy patterns to modern equivalents securely.
* **Intelligent Refactoring:** It doesn't just translate syntax; it updates deprecated libraries, flags dead code, and breaks down monolithic functions into modular, readable components.
* **Automated Verification:** After translating a block of code, CodeBridge helps generate unit tests to verify that the external behavior and logic remain exactly the same.

## ⚙️ How we built it
* **Extension Frontend:** We built the IDE plugin using TypeScript and the VS Code Extension API to ensure a native, non-disruptive developer experience.
* **Backend Logic:** The core processing engine is written in Python. It utilizes Abstract Syntax Tree (AST) parsing to break down the structure of the legacy code before interacting with the AI.
* **AI Integration:** We integrated the OpenAI API (`gpt-4o`), relying on strict prompt engineering and lossless semantic trees to ensure the model maintains type information and structural integrity during translation.

## 🚧 Challenges we ran into
The biggest hurdle was managing context windows. Throwing a massive legacy file at an LLM often results in hallucinations, missing variables, or truncated code. We solved this by using our backend to parse the AST and break the codebase down into smaller, self-contained semantic chunks. We fed these isolated functions to the AI one by one, and then re-stitched the translated components back together.

---

## 🚀 Getting Started

### Prerequisites
* [Visual Studio Code](https://code.visualstudio.com/)
* [Node.js](https://nodejs.org/) installed on your machine
* An active [OpenAI API Key](https://platform.openai.com/)

### Installation
1. Clone this repository:
   ```bash
   git clone [https://github.com/parasbishnoi029/CodeBridge.git](https://github.com/parasbishnoi029/CodeBridge.git)
