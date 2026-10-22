# CircleLogo 3.5 Deployment Guide
### Free Hosting on Cloudflare Pages | Delta Digitech Internal Utility

This document outlines the zero-cost deployment procedure for CircleLogo 3.5.

## Architecture
- **Architecture**: 100% Client-Side Single Page Application (SPA).
- **Backend / Database**: None required.
- **Third-party APIs**: None required.
- **Hosting Tier**: Free Cloudflare Pages plan (Unlimited bandwidth, 500 builds/month, free SSL certificate).

## Deployment Methods

### Method 1: Cloudflare Pages Direct Folder Upload (Simplest, 2 minutes)
1. Download `circlelogo-3.5-production.zip` and extract it to your local machine.
2. Sign in to your [Cloudflare Dashboard](https://dash.cloudflare.com/).
3. Navigate to **Workers & Pages** in the left sidebar.
4. Click **Create Application**, switch to the **Pages** tab, and click **Upload Assets**.
5. Give the project a name (e.g., `deltadigitech-circlelogo`).
6. Drag and drop the extracted `circlelogo-3.5-production` folder into the dropzone.
7. Click **Deploy site**.
8. Cloudflare will publish the application to `https://deltadigitech-circlelogo.pages.dev`.

### Method 2: Git-Integrated Continuous Deployment
1. Push the contents of `circlelogo-3.5-production` to a company GitHub or GitLab repository.
2. In Cloudflare Pages, click **Connect to Git**.
3. Select the repository and the `main` branch.
4. Build configuration:
   - Framework preset: `None`
   - Build command: *(leave empty)*
   - Build output directory: `.`
5. Click **Save and Deploy**. Any future commit will trigger an automatic free production build.

## Securing with Cloudflare Access (Zero Trust Free Tier)
Cloudflare Zero Trust provides free authentication for up to 50 employees:
1. In Cloudflare Dashboard, navigate to **Zero Trust > Access > Applications**.
2. Add an application > **Self-hosted**.
3. Domain: `deltadigitech-circlelogo.pages.dev`.
4. Configure an Identity Provider (One-Time PIN via email or Google Workspace).
5. Define Policy:
   - Rule Action: `Allow`
   - Include: `Email ending in @deltadigitech.com`
6. Now, only authenticated Delta Digitech team members can load the workspace.
