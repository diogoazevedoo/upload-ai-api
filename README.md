
# Upload AI API 🚀

Welcome to the server-side of our Upload AI project! This is where all the heavy lifting happens, from processing video uploads to generating AI-powered transcriptions and more. While the frontend might be the face of our project, this backend is the brain and the brawn.

## Tech Stack

- **Node.js and Fastify:** For crafting our server and API with speed and efficiency.
- **Prisma:** Our go-to ORM for handling database interactions smoothly.
- **Zod:** For robust validation, making sure our data is in good shape.
- **OpenAI's GPT:** Powers the AI transcriptions and interactions.

## Frontend Repo

<a href="https://github.com/diogoazevedoo/upload-ai-web">Repo</a>

## Getting Started

To get this backend up and running:

1. Clone this repo:
```bash
git clone https://github.com/diogoazevedoo/upload-ai-api
```

2. Install the dependencies (make sure you've got Node.js installed):
```bash
cd upload-ai-api
pnpm install
```

3. Create a  `.env`  file in the root of the project with the following content:
```plaintext
DATABASE_URL="file:./dev.db"
OPENAI_KEY="your_openai_api_key_here"
```
This setup uses SQLite for ease of testing, and you'll need to fill in your OpenAI API key.

4. Run the Prisma migration to set up your database schema:
```bash
pnpm prisma migrate dev
```

5. Seed your database with prompt templates:
```bash
pnpm prisma db seed
```

6. Fire up the server:
```bash
pnpm run dev
```

## API Routes Overview

Here's what you can do with our backend API:

| Route | Method | Description |
|-------|--------|-------------|
| `/videos` | POST | Upload a video file for processing. |
| `/videos/:videoId/transcription` | POST | Generate a transcription for a given video. |
| `/prompts` | GET | Retrieve all prompts/questions for AI interaction. |
| `/ai/complete` | POST | Get AI-generated responses based on video content and prompts. |

## Dive Deeper

Want to add more features or tweak the existing ones? The code's all yours! Dive into the `src` folder to explore and expand. The `routes` directory will be your roadmap to understanding and enhancing how the backend serves the frontend.

## Contributing

Your ideas and contributions are welcome! Whether it's bug fixes, new features, or improvements to the documentation, feel free to fork this repo and send over your pull requests.

## Connect

Got questions or ideas? Let's chat! Reach out to me on <a href="https://www.linkedin.com/in/idiogoazevedoo/">Linkedin</a>
