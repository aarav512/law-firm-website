# Required GitHub Repository Secrets for Cloudflare Deployment

The `deploy-cloudflare.yml` workflow needs these three secrets added under
**Settings > Secrets and variables > Actions > New repository secret**.

## 1. CLOUDFLARE_API_TOKEN

A Cloudflare API token with permission to deploy Pages projects.

**How to create it:**
1. Go to https://dash.cloudflare.com/profile/api-tokens
2. Click **Create Token** > **Edit Cloudflare Workers** template (or create custom)
3. Required permission: **Account > Cloudflare Pages > Edit**
4. Copy the token and add it as `CLOUDFLARE_API_TOKEN`.

## 2. CLOUDFLARE_ACCOUNT_ID

Your Cloudflare account ID.

**Where to find it:**
1. Go to https://dash.cloudflare.com
2. Open any site in your account, or check the account overview page
3. The Account ID is shown in the right sidebar (a 32-char hex string)
4. Add it as `CLOUDFLARE_ACCOUNT_ID`.

## 3. CLOUDFLARE_PROJECT_NAME

The name of your Cloudflare Pages project (created in the Cloudflare dashboard).

**How to create the project if it doesn't exist:**
1. Go to https://dash.cloudflare.com > **Workers & Pages**
2. Click **Create application** > **Pages** > **Upload assets**
3. Name the project (e.g. `saurav-sharma-law`) and create it
4. Add that exact name as `CLOUDFLARE_PROJECT_NAME`.

---

## Verification

After adding all three secrets, push any change to `main` (or run the workflow
manually via **Actions > Deploy to Cloudflare Pages > Run workflow**). The
workflow will upload the entire repo root to Cloudflare Pages and the live
site will update automatically.
