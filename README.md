# A SaaS AI Conversation Platform Built with Next.js 13, React, Tailwind, Prisma, Stripe 
I developed an AI companion web app that allows users to create and chat with personalized chatbots modeled after famous personalities.

Built using Next.js and includes both a responsive frontend written with React and TailwindCSS along with a Node.js/Express backend. Users can sign up for an account to access the ability to custom build their own AI companion.
The main feature is the intuitive bot creation flow that lets you pick an avatar, name, description and define the personality of your AI bot by providing details about their background and an example conversation. The bots are powered by OpenAI's natural language processing models to generate responses that mimic their given persona.
Each AI companion has persistent memory and personality powered by vector embeddings stored in Pinecone's real-time database. This gives them continuity across conversations instead of just turn-by-turn responses.
Additional features I implemented include categorization and filtering of bot types, free-text search, light/dark modes, ability to edit/delete bots, and historical conversation logs for each user.
The app is monetized via a Stripe subscription model where users have to purchase a plan to access the full custom chatbot creation features. Rate limiting and basic free bots provide a limited experience for non-paying users

Have a good little chat with your Idols.
Check out the video for more information.


## Features

- Beautiful and responsive UI designed with Tailwind CSS animations and effects
- Authentication via Clerk with email, Google, and 9+ social providers 
- Client-side form validation using react-hook-form
- Global error handling using react-query
- AI-generated images via OpenAI 
- AI-generated videos via Replicate AI
- AI-generated text conversations via OpenAI
- AI-generated music via Replicate AI
- Loading state management  
- Stripe subscriptions for paid plans
- Free tier with API rate limiting
- CRUD REST API routes built with Next.js app directory
- Direct database access from API routes without endpoints 
- Reusable page layouts and UI components
- Optimal folder structure following Next.js 13 conventions

## Tech Stack

- **Framework**: Next.js 13
- **Styling**: Tailwind CSS
- **Authentication**: Clerk 
- **Database**: MongoDB
- **Deployments**: Vercel 

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `pages/index.js`. The page auto-updates as you edit the file.

## Learn More

To learn more about the tech stack and architecture patterns used, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Tailwind Documentation](https://tailwindcss.com/docs) - learn how to customize Tailwind for your project.
- [Clerk Documentation](https://docs.clerk.dev) - learn how to integrate Clerk authentication.
- [MongoDB Documentation](https://docs.mongodb.com) - get started with MongoDB

Let me know if you would like me to modify or expand this README overview!

### Prerequisites

**Node version 18.x.x**

### Cloning the repository

Top Right

### Install packages

```shell
npm i
```

### Setup .env file


```js
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=
CLERK_SECRET_KEY=

NEXT_PUBLIC_CLERK_SIGN_IN_URL=/sign-in
NEXT_PUBLIC_CLERK_SIGN_UP_URL=/sign-up
NEXT_PUBLIC_CLERK_AFTER_SIGN_IN_URL=/dashboard
NEXT_PUBLIC_CLERK_AFTER_SIGN_UP_URL=/dashboard

OPENAI_API_KEY=
REPLICATE_API_TOKEN=

PINECONE_API_KEY=
PINECONE_ENVIRONMENT=
PINECONE_INDEX=

UPSTASH_REDIS_REST_URL=
UPSTASH_REDIS_REST_TOKEN=

NEXT_PUBLIC_CLOUDINARY_CLOUD_NAME=

DATABASE_URL=

STRIPE_API_KEY=
STRIPE_WEBHOOK_SECRET=

NEXT_PUBLIC_APP_URL="http://localhost:3000"
```

### Setup Prisma

Add MySQL Database (I used PlanetScale)

```shell
npx prisma db push

```

Seed categories:
```shell
node scripts/seed.ts
```

### Start the app

```shell
npm run dev
```

## Available commands

Running commands with npm `npm run [command]`

| command         | description                              |
| :-------------- | :--------------------------------------- |
| `dev`           | Starts a development instance of the app |
