# Next.js Infinite Redirect Loop Bug

This repository demonstrates a common bug in Next.js applications: infinite redirect loops.  The bug occurs when attempting to navigate to a route that is already active using `router.push()`. This can happen if your component re-renders frequently without properly checking if the route is already the active one.

## Steps to Reproduce
1. Clone this repository.
2. Run `npm install`.
3. Run `npm run dev`.
4. Click the button.  You'll observe the browser's address bar continuously changing, reflecting an infinite redirect loop.

## Solution
The solution involves checking if the current route matches the target route before attempting to redirect. This avoids unnecessary redirects and prevents the infinite loop.
