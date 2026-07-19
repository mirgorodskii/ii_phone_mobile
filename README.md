# II Phone Mobile

Mobile browser version of The Phone, using OpenAI Realtime through short-lived ephemeral keys.

## Railway deployment

1. Create a Railway service from this GitHub repository.
2. Keep the root directory set to `/` and the deployment branch set to `main`.
3. Generate a public domain in Railway service settings.

Railway serves `index.html` as a static site. No OpenAI API key belongs in this repository or in browser storage; `auth.html` requests a temporary client secret from the existing authentication service.

## Local preview

Serve the directory over HTTP so microphone permissions and the auth iframe behave like production:

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000/`. The authentication service allows this local development origin.
