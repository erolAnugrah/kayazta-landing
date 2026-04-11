# Kayazta Landing Page

This project was generated using Stitch design output and implemented as a Vite project for optimal performance and easy deployment.

## Tech Stack
- **Vite**: Build tool and dev server
- **Tailwind CSS**: Styling (via CDN in index.html)
- **Google Fonts**: Inter & Material Symbols

## Local Development

```bash
npm install
npm run dev
```

## Deployment to Railway

### Method 1: Git (Recommended)
1. Push this repository to GitHub.
2. Connect your GitHub repository to [Railway](https://railway.app).
3. Railway will automatically detect the `package.json`, run `npm install`, `npm run build`, and then `npm run start`.

### Method 2: Railway CLI
If you have the Railway CLI installed, run:
```bash
railway up
```

## Railway Configuration
The project is configured to serve the `dist` directory using the `serve` package on the port provided by Railway (`$PORT`).
