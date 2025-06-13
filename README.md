# EventPulse - Modern Event Monitoring & Alerting Platform

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A production-grade SaaS for monitoring application events with real-time alerts. Built with Next.js App Router, Postgres, TypeScript, Tailwind & Clerk.

## Features

- 🛠️ Complete SaaS built in modern Next.js
- 💻 Beautiful landing page included
- 🎨 Custom artworks made by a professional illustrator
- ✉️ Real-time event messages via Discord
- 🖥️ Clean & intuitive event monitoring dashboard
- 💳 Secure payments using Stripe
- 🛍️ Customers can purchase your PRO plan
- 🌟 Clean, modern UI on top of shadcn-ui
- 🔑 Authentication using Clerk
- ⌨️ 100% written in TypeScript
- 🎁 ...much more

## Getting Started

### Prerequisites
- Node.js 18+
- Stripe account
- Clerk account
- neon account
- Discord/Slack webhook URL

### Installation
```bash
git clone https://github.com/ArmanPayandeh/EventPulse.git
cd EventPulse
cp .env.example .env
```

Configure required environment variables in `.env`:
```env
# Clerk Authentication
NEXT_PUBLIC_APP_URL=

# DATABASE - Neon Postgres (neon.tech)
DATABASE_URL=

# AUTH - These come from clerk (https://link.joshtriedcoding.com/clerk)
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=
CLERK_SECRET_KEY=

# DISCORD - This comes from discord as shown in video
DISCORD_BOT_TOKEN=

# PAYMENTS - This comes from stripe as shown in video
STRIPE_SECRET_KEY=

```

Install dependencies and setup database:
```bash
npm install
npm run dev
npx prisma migrate dev 

```
```bash
yarn install
yarn dev
npx prisma migrate dev --name "init"
```
## Deployment


### Deployment Options
1. **Vercel** (Recommended):
   ```bash
   vercel deploy --prod
   ```
2. **Docker Container**:
   ```dockerfile
   FROM node:18-alpine
   WORKDIR /app
   COPY . .
   RUN npm ci --only=production
   CMD ["npm", "start"]
   ```

## Support & Troubleshooting

### Common Issues
- **"Invalid Clerk Keys"**: Verify secret keys match between .env and Clerk dashboard
- **Database Connection Failures**: Ensure PostgreSQL is running and connection string is correct
- **Stripe Webhook Errors**: Verify endpoint signing secret matches Stripe dashboard

### Getting Help
- 🐛 [Open a GitHub Issue](https://github.com/ArmanPayandeh/EventPulse/issues)
- 📧 Enterprise Support: arman.payandeh.2025@gmail.com


## License
Distributed under the MIT License. See `LICENSE` for more information.

## Acknowledgements
- Authentication by [Clerk](https://clerk.dev)
- Authentication by [Neon](https://neon.com/)
- Payment processing by [Stripe](https://stripe.com)
- UI components from [shadcn/ui](https://ui.shadcn.com)
- Illustrations by [Undraw](https://undraw.co)
