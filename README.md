# StoryWeaver AI 🧠✨

StoryWeaver AI is your creative co-pilot, helping you transform fledgling ideas into fully-formed stories. Generate unique characters, sculpt immersive worlds, and weave compelling plots with our intelligent storycrafting assistant. Built with Next.js, Tailwind CSS, shadcn/ui, and powered by Gaia's LLM API.

## Features

*   **Idea to Story:** Input your core story idea, genre, desired length, and optional details like protagonist, conflict, world vibe, and tone.
*   **AI-Powered Generation:** Leverages a Large Language Model (via Gaia's OpenAI-compatible API) to craft unique stories.
*   **Markdown Support:** Displays generated stories with rich text formatting.
*   **Download as Image:** Save your favorite stories as PNG images.
*   **Social Sharing:** Quickly share links to your app (users can attach their downloaded story image) on X (Twitter), LinkedIn, and Facebook.
*   **Sleek UI:** Modern and responsive interface built with shadcn/ui and Tailwind CSS.

## Tech Stack

*   **Framework:** [Next.js](https://nextjs.org/) (App Router)
*   **Language:** [TypeScript](https://www.typescriptlang.org/)
*   **Styling:** [Tailwind CSS](https://tailwindcss.com/)
*   **UI Components:** [shadcn/ui](https://ui.shadcn.com/)
*   **Form Management:** [React Hook Form](https://react-hook-form.com/) & [Zod](https://zod.dev/)
*   **LLM Integration:** `openai` npm package configured for [Gaia's API](https://docs.gaianet.ai)
*   **Markdown Rendering:** `react-markdown`
*   **HTML to Image:** `dom-to-image-more`
*   **Icons:** `lucide-react`

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

*   [Node.js](https://nodejs.org/) (v18.x or later recommended)
*   [npm](https://www.npmjs.com/) or [yarn](https://yarnpkg.com/)
*   A Gaia API Key ([Get one here](https://docs.gaianet.ai/getting-started/authentication))

### Setup & Installation

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/harishkotra/story-weaver-ai.git
    cd story-weaver-ai
    ```

2.  **Install dependencies:**
    ```bash
    npm install
    # or
    yarn install
    ```

3.  **Set up Environment Variables:**
    Create a `.env.local` file in the root of the project. This file is ignored by Git and is used for local environment configuration.
    ```bash
    cp .env.example .env.local
    ```
    Now, open `.env.local` and add your API key:

    ```env
    # .env.local

    # Required: Your API Key for the Gaia LLM service (or other OpenAI-compatible API)
    GAIA_API_KEY="your_actual_gaia_api_key_here"

    # Optional: If Gaia changes their endpoint or you use a different compatible service
    # Default is 'https://llama70b.gaia.domains/v1' if not set
    GAIA_API_ENDPOINT="https://your-custom-openai-compatible-endpoint/v1"
    GAIA_API_MODEL="llama70b"
    ```
    **Important:** Replace `"your_actual_gaia_api_key_here"` with your real API key. ([Get one here](https://docs.gaianet.ai/getting-started/authentication))

4.  **Initialize shadcn/ui (if you need to add more components):**
    While the project is set up, if you intend to add more shadcn/ui components later, you might need to run init (though it should be configured already):
    ```bash
    npx shadcn@latest init
    ```
    Follow the prompts, accepting the defaults or aligning with existing project configuration (`src/app/globals.css`, `tailwind.config.ts`, aliases `@/components` and `@/lib/utils`).

### Running the Application Locally

1.  **Start the development server:**
    ```bash
    npm run dev
    # or
    yarn dev
    ```

2.  **Open your browser:**
    Navigate to `http://localhost:3000`.

You should now see the StoryWeaver AI application running!

## Contributing

We welcome contributions to StoryWeaver AI! Whether it's fixing a bug, adding a new feature, or improving documentation, your help is appreciated.

### Contribution Guidelines

1.  **Fork the Repository:** Create your own fork of the project on GitHub.
2.  **Clone Your Fork:** Clone your forked repository to your local machine.
    ```bash
    git clone https://github.com/harishkotra/story-weaver-ai.git
    cd story-weaver-ai
    ```
3.  **Create a New Branch:** Make your changes in a new git branch.
    ```bash
    git checkout -b my-feature-branch
    ```
    *   Use a descriptive branch name (e.g., `feat/add-new-genre-options`, `fix/image-download-bug`).
4.  **Make Your Changes:** Implement your feature or bug fix.
    *   Follow the existing code style and conventions.
    *   Ensure your code is well-commented, especially for complex logic.
    *   Update documentation if you're changing how something works or adding new functionality.
5.  **Test Your Changes:** Make sure your changes work as expected and don't introduce new issues.
    *   Run the application locally (`npm run dev`).
    *   Test thoroughly the areas you've modified.
6.  **Commit Your Changes:** Commit your changes with a clear and descriptive commit message. Follow Conventional Commits if possible (e.g., `feat: Add support for dark mode`, `fix: Resolve issue with story text overflow`).
    ```bash
    git add .
    git commit -m "feat: Describe your feature or fix"
    ```
7.  **Push to Your Fork:** Push your changes to your forked repository on GitHub.
    ```bash
    git push origin my-feature-branch
    ```
8.  **Open a Pull Request (PR):**
    *   Go to the original `story-weaver-ai` repository on GitHub.
    *   Click on "Pull requests" and then "New pull request".
    *   Choose your fork and branch to compare with the main branch of the original repository.
    *   Provide a clear title and description for your PR, explaining the changes you've made and why.
    *   Reference any related issues (e.g., "Closes #123").
9.  **Code Review:** Project maintainers will review your PR. Be prepared to discuss your changes and make further modifications if requested.
10. **Merge:** Once approved, your PR will be merged into the main project. Congratulations! 🎉

### Reporting Bugs

*   Use the GitHub Issues section of the repository.
*   Provide a clear and descriptive title.
*   Include steps to reproduce the bug.
*   Specify your environment (OS, browser, Node.js version).
*   Include screenshots or error messages if applicable.

### Suggesting Enhancements

*   Use the GitHub Issues section with a label like "enhancement" or "feature request".
*   Clearly describe the enhancement and its potential benefits.