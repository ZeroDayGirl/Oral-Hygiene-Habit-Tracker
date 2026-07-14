# Architecture

## Overview

This app is built and deployed through [Lovable](https://lovable.dev), an AI-assisted full-stack development platform. It is not designed to be run as a fully self-hosted, standalone project — it depends on several provisioned backend services that must be configured before the app will function locally or in any other environment.

## Stack

- **Frontend:** React, Tailwind CSS
- **Backend / Database:** Supabase (auth, data storage)
- **Payments:** Paddle
- **AI Gateway:** Lovable AI Gateway (used for any AI-assisted in-app functionality)
- **Hosting:** Lovable-managed deployment

*(Update any of the above if your actual configuration differs.)*

## Required Services

To run this project outside of Lovable, you'll need accounts and API credentials for:

1. **Supabase** — provides the database and user authentication. Create a project at [supabase.com](https://supabase.com) and configure the connection URL/keys.
2. **Paddle** — handles payment/subscription processing. Requires a Paddle account and API keys.
3. **Lovable AI Gateway** — routes AI-related requests used within the app.

Environment variables for each of these must be set before the app can start; see `.env.example` *(add this file to the repo if it doesn't already exist)* for the required keys.

## Data Flow (high level)

1. User actions (session timers, manual logs) are captured in the frontend
2. State is persisted to Supabase
3. Streak/reward logic evaluates on each completion event and triggers the appropriate UI feedback
4. Payment-gated features (future phases) route through Paddle before unlocking access

## Local Development

Because this project depends on provisioned cloud services rather than a fully local stack, local development requires:

1. Cloning the repo
2. Creating your own Supabase project and Paddle sandbox account
3. Populating environment variables with your own credentials
4. Running the frontend against those provisioned services

A fully turnkey `npm install && npm run dev` setup is not currently supported, since core functionality depends on these external services being configured first.

## Notes

This document reflects the current architecture as of this project's early development phase and will be updated as the app evolves, particularly once Phase 2 (commerce) and Phase 3 (professional access) features are built out.
