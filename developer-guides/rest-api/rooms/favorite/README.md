# Rooms Favorite/Unfavorite

Favorite or unfavorite room.

| URL | Requires Auth | HTTP Method |
| :--- | :--- | :--- |
| `/api/v1/rooms.favorite/:roomId` | `yes` | `POST` |

## Payload

| `roomId`   | `GENERAL`    | Required | Room ID where to favorite or unfavorite.            |
| `favorite` | `true/false` | Required | The value to favorite(true)/unfavorite(false) room. |

## Example Call

```bash
curl -H "X-Auth-Token: 9HqLlyZOugoStsXCUfD_0YdwnNnunAJF8V47U3QHXSq" \
     -H "X-User-Id: aobEdbYhXfu5hkeqG" \
     http://localhost:3000/api/v1/rooms.favorite/GENERAL  \
     -d '{ "favorite": true }'
```

## Example Result

```json
{
  "success": true
}
```

## Change Log

| Version | Description |
| :--- | :--- |
| 0.64.0 | Added |