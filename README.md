# apex.assps.edu.pk

Apex experience / marketing portal repository.

## Domain

- Production: `https://apex.assps.edu.pk`

## Local Snapshot Source

- Original workspace source: `c:\projects\My SAas\super-app`

## Live Server Mapping

- App runs through Next.js / PM2
- Reverse proxy target: `127.0.0.1:3000`

## Useful Commands

- `npm run dev`
- `npm run build`
- `npm run start`
- `npm run lint`
- `npm run seed:demo`

## Important Architecture Note

- `apex.assps.edu.pk` currently shares the same live codebase and PM2 process as `api.assps.edu.pk`
- Root currently redirects to `/apex`

## Boundary Guide

- Apex brand experience: yes
- landing and story surfaces: yes
- demo and onboarding journeys: yes
- operational dashboards: currently present, but should move out over time

See [ARCHITECTURE.md](ARCHITECTURE.md).

## Repository Shape

- product code lives under `src/`
- database and schema helpers live under `prisma/`
- older patch helpers are kept under `ops/legacy/`

## Safety

- GitHub pushes do not deploy automatically.
