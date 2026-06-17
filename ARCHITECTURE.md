# Architecture Notes

## Purpose

This repository currently represents the experience served on:

- `https://apex.assps.edu.pk`

The live root redirects users to `/apex`, which is part of the shared Next.js application.

## Current Live Reality

- Runtime: shared Next.js app
- Proxy target: `127.0.0.1:3000`
- PM2 process: `apex-connect`
- Shared live codebase with: `https://api.assps.edu.pk`

## What Belongs Here Long-Term

Recommended long-term focus for this repository:

- Apex landing pages
- cinematic storytelling surfaces
- product marketing flows
- demo request and registration journeys
- visual brand experience

## What Is Still Shared Today

This snapshot still includes admin and application code because production is not yet isolated at infrastructure level.

Shared areas currently include:

- authenticated app routes
- API routes
- shared branding/runtime utilities
- shared login/session plumbing

## Recommended Future Split

When infrastructure separation is ready:

1. keep `/apex` and marketing/brand experience here
2. remove admin dashboards and non-marketing application surfaces from this repository
3. move operational app/API concerns fully to `api-assps-edu-pk`
4. run separate PM2 processes and separate Nginx upstream targets

## Safety Rule

Source control is separated now, but live hosting is still shared. Treat production changes as coupled until hosting is fully split.

See also [MIGRATION_PLAN.md](MIGRATION_PLAN.md).
