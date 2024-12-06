# React Router Dom Catch-all Route Issue

This repository demonstrates a common issue encountered when using the catch-all route ('*') in React Router Dom v6.  The catch-all route unintentionally overrides other defined routes, leading to the 404 component always rendering.

## Bug Description

The provided code shows a simple React app with three routes: Home, About, and a catch-all NotFound route.  Despite correctly specifying paths, the NotFound component is always displayed.

## Solution

The issue arises from the order of routes. The catch-all route ('*') needs to be placed at the end of the Routes component to allow other specific routes to be matched first.  This ensures that the NotFound component only renders when no other routes match.