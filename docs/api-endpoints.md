# API Endpoints

## HTML API

### Root

- `GET /` - loads React web app

## JSON API

### Users

- `GET /api/users/:id`
  - profile page shows stats of contributions for the user
- `POST /api/users`

### Session

- `POST /api/session`
- `DELETE /api/session`
- `GET /api/session`

### Albums

- `GET /api/albums`
  - index of all albums
- `GET /api/albums/:id`
  - album information
  - index of all tracks for an album

- these are just to organize the tracks
- users will not be able to add or delete albums, unless I have time

### Tracks

- `GET /api/albums/:id/tracks`
  - not planning to use this anymore
- `POST /api/tracks`
  - only if the user is signed in
- `GET /api/tracks/:id`
  - gives track data and comment index for the track
- `DELETE /api/tracks/:id`
  - only if the user is signed in and track created by user
- no updating tracks because then annotations will be messy

### Annotations

- `GET /api/annotations/:id`
  - just one annotation at a time
  - displays number of upvotes on the annotation (will retrieve with active record)
- `POST /api/annotations`
  - only if the user is signed in
- `DELETE /api/annotations/:id`
  - only if the user is signed in and annotation written by user
- `PATCH /api/annotations/:id`
  - only if the user is signed in and annotation written by user

### Comments

- `POST /api/comments`
  - only if the user is signed in
- `DELETE /api/comments/:id`
  - only if the user is signed in and comment written by user

### Upvotes

- `POST /api/upvotes`
  - only if the user is signed in
- `DELETE /api/upvotes/:id`
  - only if the user is signed in
