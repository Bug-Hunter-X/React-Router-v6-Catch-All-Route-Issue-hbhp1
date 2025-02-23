# React Router v6 Catch-All Route Issue

This repository demonstrates an unexpected behavior with the catch-all route (`/*`) in React Router v6.  The catch-all route is always triggered, even when other routes match. This seems to be particularly sensitive to the order of routes defined in the `Routes` component.

## Problem

When the `/*` route is placed *before* more specific routes, it intercepts all requests and prevents the specific routes from being matched.

## Solution

The `/*` route should always be placed *last* within the `Routes` component. This ensures that it only matches when no other routes are matched.  The solution demonstrates the proper order to avoid this issue.
