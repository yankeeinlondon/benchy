# Multi Autocomplete LLM Benchmark
> A tool to benchmark and compare the speed, price, and performance of multiple LLM models for a given prompt in a reactive autocomplete UI.
> Watch the walk through [video here](https://youtu.be/1ObiaSiA8BQ)

<img src="./images/pick-two.png" alt="pick-two" style="max-width: 800px;">

## Important Files
- `.env` - Environment variables for API keys
- `server/.env` - Environment variables for API keys
- `package.json` - Front end dependencies
- `server/pyproject.toml` - Server dependencies
- `src/store.ts` - Stores all front end state and prompt
- `src/api.ts` - Parallel Autocomplete API requests
- `server/server.py` - Server routes
- `server/llm_models.py` - All LLM models
- `src/components/UserInput.vue` - User input with 2s debounce and autocomplete trigger

## Setup

### Client Setup
```bash
# Install dependencies using bun (recommended)
bun install

# Or using npm
npm install

# Or using yarn
yarn install

# Start development server
bun dev  # or npm run dev / yarn dev
```

### Server Setup
```bash
# Move into server directory
cd server

# Create and activate virtual environment using uv
uv venv

# Install dependencies
uv pip sync

# Set up environment variables
cp .env.sample .env

# Edit every .env key with your API keys and settings
```
ANTHROPIC_API_KEY=
OPENAI_API_KEY=
GEMINI_API_KEY=
```

# Start server
uv run python server.py

# Run tests
uv run pytest (**beware will hit APIs and cost money**)
```

## Resources
- https://github.com/simonw/llm?tab=readme-ov-file
- https://github.com/openai/openai-python
- https://platform.openai.com/docs/guides/predicted-outputs
- https://community.openai.com/t/introducing-predicted-outputs/1004502
- https://unocss.dev/integrations/vite
- https://www.npmjs.com/package/vue-codemirror6
- https://vuejs.org/guide/scaling-up/state-management
- https://www.ag-grid.com/vue-data-grid/getting-started/
- https://www.ag-grid.com/vue-data-grid/value-formatters/
- https://llm.datasette.io/en/stable/index.html
- https://cloud.google.com/vertex-ai/generative-ai/docs/multimodal/get-token-count
- https://ai.google.dev/gemini-api/docs/tokens?lang=python
- https://ai.google.dev/pricing#1_5flash