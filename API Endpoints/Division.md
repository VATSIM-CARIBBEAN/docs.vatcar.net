---
label: "Division"
icon: book
order: 95
---

# Division API

Access division-wide information including events and announcements.

## Get Division Events

Retrieve all upcoming and recent events for the Caribbean Division.

```
GET https://vatcar.net/api/v2/division/events
```

==- Request [!badge corners="round" variant="success" text="GET"]
No parameters required.
==- Response
- success - String message indicating request status
- data - Array of event objects containing event details
    - id - Event ID (integer)
    - name - Event name
    - description - Full event description (supports markdown/HTML)
    - image_url - URL to event banner/promotional image
    - start - Event start time (Y-m-d H:i:s format)
    - end - Event end time (Y-m-d H:i:s format)
    - airports - Object containing arrival and departure airport arrays
    - positions - Staffed positions (nullable)
    - forum_event_id - Associated forum event ID (nullable)
    - facilities - Bitmask of participating facilities
    - user_cid - CID of user who created event
    - edit_cid - CID of user who last edited event
    - created_at - Creation timestamp
    - updated_at - Last update timestamp
===

### Example Request

```bash
curl -H "api_key: your_api_key_here" \
  https://vatcar.net/api/v2/division/events
```

### Example Response

```json
{
  "success": "Fetched successfully",
  "data": [
    {
      "id": 145,
      "name": "Caribbean Flight Night",
      "description": "Join us for a special event covering major Caribbean airports with full ATC coverage. Experience the beauty of island hopping across the Caribbean region.",
      "image_url": "https://vatcar-cdn.nyc3.cdn.digitaloceanspaces.com/public/events/caribbean-flight-night.png",
      "start": "2024-11-15 18:00:00",
      "end": "2024-11-15 22:00:00",
      "airports": {
        "arrival": ["TJSJ", "MDSD", "TNCM"],
        "departure": ["TJSJ", "MDSD", "TNCM"]
      },
      "positions": null,
      "forum_event_id": null,
      "facilities": 136,
      "user_cid": 1234567,
      "edit_cid": 1234567,
      "created_at": "2024-10-01T10:00:00.000000Z",
      "updated_at": "2024-10-15T14:30:00.000000Z"
    },
    {
      "id": 144,
      "name": "Juliana Monthly Fly-In",
      "description": "Experience the famous Maho Beach approach at Princess Juliana International Airport (TNCM). Controllers from Curacao FIR will provide top-notch ATC services.",
      "image_url": "https://vatcar-cdn.nyc3.cdn.digitaloceanspaces.com/public/events/juliana-flyin.png",
      "start": "2024-11-08 17:00:00",
      "end": "2024-11-08 20:00:00",
      "airports": {
        "arrival": ["TNCM"],
        "departure": ["TNCM"]
      },
      "positions": null,
      "forum_event_id": null,
      "facilities": 2,
      "user_cid": 7654321,
      "edit_cid": 7654321,
      "created_at": "2024-09-28T08:15:00.000000Z",
      "updated_at": "2024-10-01T12:00:00.000000Z"
    }
  ]
}
```