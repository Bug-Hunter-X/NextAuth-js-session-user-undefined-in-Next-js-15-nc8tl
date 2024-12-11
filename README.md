# NextAuth.js session.user undefined in Next.js 15

This repository demonstrates a bug where the `session.user` object is undefined in a Next.js 15 application using NextAuth.js, even when a user is logged in.  The issue arises when accessing `session.user.email` on the About page.

## Steps to Reproduce

1. Clone this repository.
2. Install dependencies: `npm install`
3. Run the development server: `npm run dev`
4. Log in using the NextAuth.js provider (e.g., credentials).
5. Navigate to the `/about` page.
6. Observe the error: 'TypeError: Cannot read properties of undefined (reading 'user')'.

## Potential Causes

The root cause seems to be related to the asynchronous nature of `getServerSideProps` and how it interacts with NextAuth.js session handling in Next.js 15.  Further investigation is needed to pin down the exact reason.