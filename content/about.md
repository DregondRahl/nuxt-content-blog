---
title: About
---

With **Nuxt.js version 2.13**, the full-static mode has been introduced. In addition, a new command nuxt export was added to pre-render your pages without triggering a webpack build with the goal to separate the rendering and build process. The only issue was that most Nuxt.js users weren't able to unleash the full potential of the separation... until now.

    Introduction
    Faster Static Deployments
    Generate time: cache vs full webpack build
    Using in your projects
        Excluding Files from Cache
        Module Authors
    How it works
        Back to old school commands
    What to do next

Faster Static Deployments

With v2.14, nuxt generate will automagically skip webpack build step when no code has been changed and use the previous build using cache. This will help to drastically improve static deployments time by avoiding unnecessary builds which is usually the most time-consuming part of generation process. Cache support is platform-agnostic and works on Netlify, Vercel, or any other CI/CD setup that is caching node_modules.
Generate time: cache vs full webpack build

See the comparison in seconds between two nuxt generate:

    Build is when a webpack build is required
    Cache is only when the content has changed (webpack build skipped)
