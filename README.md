# React Router Dom v6 Catch-all Route Issue

This repository demonstrates a common issue encountered when using the catch-all route (`/*`) in React Router Dom v6.  The problem arises when this route is placed after other more specific routes, potentially causing the application to always render the catch-all component, regardless of the URL.

## Problem Description:

The application is expected to render the Home component when navigating to `/`, About component when navigating to `/about` and NotFound component when any other path is specified.

However, due to the placement of the `/*` route, other routes do not render properly, and the NotFound component is rendered instead, even when other routes should be shown.

## Solution:

The solution involves reordering the routes. Catch-all routes like `/*` should always be placed last in the `Routes` component to ensure that they only match URLs not matched by other more specific routes.