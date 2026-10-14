# Nikah invitation · Vercel setup

## Public invitation
Deploy the project to Vercel. The invitation is served from `/`.

## Database
Create a Neon/Postgres database and add this Vercel environment variable:

- `DATABASE_URL` — Neon/Postgres connection string

The API creates the `rsvps` and `wishes` tables automatically on first request.

## Admin dashboard
Open:

`https://YOUR-DOMAIN.vercel.app/admin`

Set this Vercel environment variable:

- `ADMIN_KEY` — use a long random secret; do not put it in HTML or JavaScript.

The admin dashboard provides:

- Login screen
- Live RSVP statistics
- Guest search
- Attending / not attending status
- Guest counts
- RSVP timestamps
- RSVP deletion
- CSV export
- Wishes/messages
- Automatic refresh every 15 seconds

The admin key is only sent to the backend over the request body/header and is kept in sessionStorage only for the current browser tab session.

## Local
Set `ADMIN_KEY` in your shell if you want protected local admin access. If it is not set, the local server uses `change-me` as the default key.

Then double-click `START_NIKAH.bat` and open `http://localhost:3000/admin`.
