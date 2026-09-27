# Flux Corp — API (backend)

Node.js + Express + MySQL API for the Flux Corp website and admin CMS.

## Setup

```bash
cp .env.example .env
# Edit DB_* and JWT_SECRET

npm install
npm run db:setup    # migrate + admin user
npm run dev         # port 5001
```

**Admin login:** username `admin` — password `admin@Flux2026` (after `seed:admin`)

## Scripts

| Command | Description |
|---------|-------------|
| `npm run dev` | API with auto-reload |
| `npm run migrate` | Create DB + run SQL migrations |
| `npm run seed:admin` | Reset super-admin password |
| `npm run db:setup` | migrate + seed:admin |

## Production

- Set `CLIENT_URL` to your Vercel frontend URL (CORS).
- Use persistent storage for `uploads/`.
- On the frontend, set `VITE_API_URL` to this API’s public URL.

## Frontend

The React app lives in a separate repository ([Flux](https://github.com/RahulKirad/Flux) or your frontend repo).
