# React Router Catch-All Route Bug

This repository demonstrates a common issue with React Router's catch-all route (`/*`).  When a catch-all route is defined, it unintentionally overrides other routes, preventing them from working correctly.

## Issue
The problem occurs when a catch-all route is placed after more specific routes.  The catch-all route's `path="/*"` will match every path, effectively overshadowing the more specific routes. This leads to the catch-all component being rendered even when a specific route should be active.

## Solution
The solution involves rearranging the order of routes.  Place the catch-all route as the *last* route in your `Routes` component. This ensures that the more specific routes are matched before the catch-all route is considered.

## How to Reproduce
1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Observe that navigating to `/about` still renders the `NotFound` component. 
5. Examine the corrected code in `AppSolution.js` to see how the route order fixes the issue.
