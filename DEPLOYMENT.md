# Deployment Notes

## Production Mapping

- Domain: `apex.assps.edu.pk`
- Runtime: Next.js app behind Nginx
- Proxy target: `127.0.0.1:3000`
- PM2 process: `apex-connect`

## Current Behavior

- `/` returns a redirect to `/apex`
- shared app runtime with `api.assps.edu.pk`

## Safety

- This repo is separate in GitHub, but production is still shared with `api.assps.edu.pk`
- Infrastructure separation would be needed for fully isolated live deployments

