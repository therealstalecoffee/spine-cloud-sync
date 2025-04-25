# Spine Cloud Sync

A lightweight Node.js + Express server for backing up and restoring virtual bookshelves for the SPINE app.

## Features

- POST `/api/syncShelf` – Save a user's shelf to the cloud
- GET `/api/shelf/:profile` – Retrieve saved shelf by profile
- No database needed — uses flat JSON files in `./data/`

## Setup

```bash
git clone https://github.com/therealstalecoffee/spine-cloud-sync.git
cd spine-cloud-sync
npm install
npm run dev
```

## Example API Calls

**Backup shelf**
```http
POST /api/syncShelf
Content-Type: application/json

{
  "profile": "Alice",
  "books": [{ "id": "1", "title": "Dune", "author": "Frank Herbert" }]
}
```

**Import shelf**
```http
GET /api/shelf/Alice
```

## Deployment

You can easily deploy this on:

- Render
- Railway
- Fly.io

## Future Plans

- User authentication
- Versioned backups
- Remote file storage

Happy reading,
**Team Spine**