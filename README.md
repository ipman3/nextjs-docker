# nextjs-docker

Minimal Next.js App Router starter with TypeScript and Docker.

## Local development

```bash
npm install
npm run dev
```

Open `http://localhost:3000`.

## Docker

```bash
docker compose up --build
```

## GitHub Actions to redeploy Coolify

This repo includes `.github/workflows/coolify-redeploy.yml`. On pushes to `main`, GitHub Actions will:

1. Install dependencies
2. Run `npm run lint`
3. Run `npm run build`
4. Trigger a Coolify redeploy through the deploy webhook

Configure these GitHub repository secrets before enabling it:

- `COOLIFY_WEBHOOK`: the Deploy Webhook URL from your Coolify resource
- `COOLIFY_TOKEN`: a Coolify API token with deploy permission
