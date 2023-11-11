# A SaaS AI Conversation Platform Built with Next.js 13, React, Tailwind, Prisma, Stripe 
I developed an AI companion web app that allows users to create and chat with personalized chatbots modeled after famous personalities.

Built using Next.js and includes both a responsive frontend written with React and TailwindCSS along with a Node.js/Express backend. Users can sign up for an account to access the ability to custom build their own AI companion.
The main feature is the intuitive bot creation flow that lets you pick an avatar, name, description and define the personality of your AI bot by providing details about their background and an example conversation. The bots are powered by **OpenAI's natural language processing models** to generate responses that mimic their given persona.
Each AI companion has persistent memory and personality powered by **vector embeddings** stored in **Pinecone's real-time database**. This gives them continuity across conversations instead of just turn-by-turn responses.
Additional features I implemented include categorization and filtering of bot types, free-text search, light/dark modes, ability to edit/delete bots, and historical conversation logs for each user.
The app is monetized via a Stripe **subscription model** where users have to purchase a plan to access the full custom chatbot creation features. Rate limiting and basic free bots provide a limited experience for non-paying users

Have a good little chat with your Idols.
Check out the Images for more information.
![image](https://github.com/divitcr7/Talk-To-Your-Idol/assets/67183559/100e23e4-65ab-4900-b55f-ccaa0c963932)
![image](https://github.com/divitcr7/Talk-To-Your-Idol/assets/67183559/78735a93-d270-4080-b811-2fd537f4b318)

![image](https://github.com/divitcr7/Talk-To-Your-Idol/assets/67183559/fd588547-8a8b-4523-a21e-0aded9b0b31b)
![image](https://github.com/divitcr7/Talk-To-Your-Idol/assets/67183559/7b6e60f7-f900-486c-902e-9c93b588da10)
![image](https://github.com/divitcr7/Talk-To-Your-Idol/assets/67183559/c617d9bb-b960-4615-b1dc-346ac5dd5eba)
Subscribe / Upgrade for your own Avatar
![image](https://github.com/divitcr7/Talk-To-Your-Idol/assets/67183559/3d22a985-708d-4ec1-88fe-342cbc94fd8e)

![image](https://github.com/divitcr7/Talk-To-Your-Idol/assets/67183559/4b7b3e62-449a-42f7-a0e7-d70b7f6b9197)
![image](https://github.com/divitcr7/Talk-To-Your-Idol/assets/67183559/5a438391-2213-4f6a-b5ff-787a79a15b6f)


## Features

- Beautiful and responsive UI designed with Tailwind CSS animations and effects
- Authentication via Clerk with email, Google, and 9+ social providers 
- Client-side form validation using react-hook-form
- Global error handling using react-query
- AI-generated images via OpenAI 
- AI-generated text conversations via OpenAI
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
