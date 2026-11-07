# Commune Connect – Technical Specifications

## MVP Stack
- **Frontend**: React Native (Expo)
- **Backend**: Node.js + Express
- **Database**: PostgreSQL (hosted via Supabase)
- **Auth**: Firebase Auth or Supabase Auth
- **Hosting**: Vercel (frontend), Railway or Fly.io (backend)

---

## Core Data Models

### User
- `id`
- `name`
- `bio`
- `location`
- `commune_status` (e.g., "seeking", "hosting", "building")
- `values` (JSON)
- `skills` (JSON)
- `availability`
- `verified` (boolean)

### Commune
- `id`
- `name`
- `description`
- `location`
- `philosophy`
- `members` (array of user ids)
- `open_to_visits` (boolean)

### Review
- `id`
- `reviewer_id`
- `target_id` (user or commune)
- `type` ("user" or "commune")
- `rating`
- `text`

### Intention
- `id`
- `user_id`
- `title`
- `description`
- `preferred_region`
- `collaboration_type` ("cofound", "visit", etc.)

---

## Alternatives
- **Auth**: Clerk.dev, Auth0
- **Database**: Firebase Firestore or MongoDB Atlas
- **Realtime & Messaging**: Ably, Socket.IO, or Firebase
