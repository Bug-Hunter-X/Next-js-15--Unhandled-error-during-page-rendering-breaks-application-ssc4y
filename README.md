# Next.js 15 Unhandled Error During Page Rendering

This repository demonstrates a subtle bug in Next.js 15 where errors thrown during page rendering can break the entire application, even with error boundaries in place.  The issue is particularly noticeable when dealing with dynamic imports.

## Reproduction Steps

1. Clone this repository.
2. Run `npm install`.
3. Run `npm run dev`.
4. Navigate to `/about`.

You'll observe that the entire application crashes and displays a generic Next.js error page rather than an error boundary.

## Solution

The solution involves using the `next/error` component within a custom error boundary to gracefully handle rendering errors, or careful error handling within each page component.

## Additional Notes

This issue has been observed in Next.js 15, and may have been addressed in later versions.