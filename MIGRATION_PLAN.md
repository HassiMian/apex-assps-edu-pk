# Migration Plan

## Goal

Turn `apex-assps-edu-pk` into the dedicated Apex brand and experience repository for:

- cinematic landing pages
- product storytelling
- marketing funnels
- demo and registration journeys
- Apex visual identity

## Current Status

This repository still contains both:

1. Apex experience code
2. operational app and dashboard code

That is acceptable for now because live hosting is still shared.

## Keep Here

These areas should remain in this repository long-term:

- `src/app/apex/`
- Apex visual and cinematic components
- product storytelling layers
- marketing CTA flows
- registration/demo request user journeys

## Move Out Later

These areas should eventually be removed from this repository and kept only in `api-assps-edu-pk`:

- `src/app/admin/`
- `src/app/api/`
- `src/app/dashboard/`
- `src/app/parent/`
- `src/app/student/`
- `src/app/teacher/`
- `src/app/saas-admin/`
- `src/app/super-admin/`
- operational data-management surfaces

## Shared For Now

These stay shared until infrastructure separation:

- login/session flows
- common branding/runtime config
- payment and onboarding flows that still cross both worlds

## Safe Split Sequence

1. keep `/apex` route intact
2. peel marketing-only components away from shared operational code
3. stop importing admin-focused utilities into Apex surfaces
4. validate route-by-route behavior in isolated branches
5. only then move to separate runtime and deployment target

## Non-Goals Right Now

- no live route removals
- no production host changes
- no PM2 process split yet

