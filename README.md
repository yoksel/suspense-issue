# React Suspense component issue

We use `Suspense` component in NextJs project to catch server side errors in components and to prevent ruining the whole page as <a href="https://react.dev/reference/react/Suspense#providing-a-fallback-for-server-errors-and-client-only-content">recommended here</a>.

In React <b>19.1</b> <code>Suspense</code> just renders children on page rendered on server side without JS. So if user without JS opens page, he gets regular page with the content.

In React <b>19.2</b> <code>Suspense</code> renders fallback and never renders children on page rendered on server side without JS. So now if user without JS opens page, he gets blank page.

Run project locally to see the live demo with the issue


This is a [Next.js](https://nextjs.org) project bootstrapped with [`create-next-app`](https://nextjs.org/docs/pages/api-reference/create-next-app).

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/pages/building-your-application/deploying) for more details.
