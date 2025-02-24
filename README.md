# Unhandled Promise Rejection in Next.js 15

This repository demonstrates a subtle error that can occur in Next.js 15 applications when an unhandled promise rejection happens within a page component.  Next.js 15 has stricter error handling, and unhandled rejections will cause the application to crash, often resulting in a confusing error message.

**The Problem:**

The `about.js` file contains a promise that is intentionally rejected.  In Next.js 15, this will cause an error because the rejection is not caught.  Earlier versions might have handled this differently, leading to unexpected behavior or silent failures.

**The Solution:**

The solution involves using a `try...catch` block to handle potential errors within the component, preventing the unhandled rejection.