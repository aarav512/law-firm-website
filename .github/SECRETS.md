# Required GitHub Repository Secrets for Cloudflare Deployment

Add these under Settings > Secrets and variables > Actions > New repository secret.

## 1. CLOUDFLARE_API_TOKEN
Create at https://dash.cloudflare.com/profile/api-tokens with permission:
Account > Cloudflare Pages > Edit

## 2. CLOUDFLARE_ACCOUNT_ID
Find it at https://dash.cloudflare.com (32-char hex, right sidebar)

## 3. CLOUDFLARE_PROJECT_NAME
Create a Pages project at Workers & Pages > Create, then use that exact name.
