---
label: "Facility"
icon: briefcase
order: 90
---

# Facility API

Access information specific to your facility, including roster, events, and staff.

## Get Facility Roster

Retrieve the complete roster for your facility, including staff positions, home controllers, and visitors.

```
GET https://vatcar.net/api/v2/facility/roster
```

==- Request [!badge corners="round" variant="success" text="GET"]
No parameters required. Returns roster for the facility associated with your API key.
==- Response
- success - String message indicating request status
- data - Object containing roster information
    - facility - Full facility object with id, name_long, name_short, website_url, etc.
    - staff - Object containing staff positions (each includes full user object)
        - atm - Air Traffic Manager (full user object with all fields)
        - datm - Deputy Air Traffic Manager (full user object)
        - ta - Training Administrator (full user object)
        - ec - Events Coordinator (full user object or null)
        - fe - Facility Engineer (full user object or null)
        - wm - Webmaster (full user object or null)
    - controllers - Array of home controller objects (full user objects with all fields)
    - visitors - Array of visitor objects (full user objects with all fields)

Note: User objects include: cid, first_name, last_name, email, email_preferences, facility, facility_join, rating, last_active, flags, integrations, fir object, and visiting_facilities array.
===

### Example Request

```bash
curl -H "api_key: your_api_key_here" \
  https://vatcar.net/api/v2/facility/roster
```

### Example Response

```json
{
  "success": true,
  "data": {
    "facility": "TJSJ",
    "staff": {
      "atm": {
        "cid": 1234567,
        "name": "John Doe",
        "email": "atm@example.com"
      },
      "datm": {
        "cid": 2345678,
        "name": "Jane Smith",
        "email": "datm@example.com"
      },
      "ta": {
        "cid": 3456789,
        "name": "Bob Johnson",
        "email": "ta@example.com"
      },
      "ec": null,
      "fe": null,
      "wm": null
    },
    "controllers": [
      {
        "cid": 4567890,
        "first_name": "Alice",
        "last_name": "Williams",
        "rating": 3,
        "join_date": "2024-01-15T10:00:00Z"
      },
      {
        "cid": 5678901,
        "first_name": "Charlie",
        "last_name": "Brown",
        "rating": 2,
        "join_date": "2024-03-20T14:30:00Z"
      }
    ],
    "visitors": [
      {
        "cid": 6789012,
        "first_name": "David",
        "last_name": "Miller",
        "rating": 4,
        "home_facility": "MDSD",
        "visit_start": "2024-08-01T09:00:00Z"
      }
    ]
  }
}
```

---

## Get Facility Events

Retrieve all upcoming and recent events for your facility.

```
GET https://vatcar.net/api/v2/facility/events
```

==- Request [!badge corners="round" variant="success" text="GET"]
No parameters required. Returns events for the facility associated with your API key.
==- Response
- success - String message indicating request status
- data - Array of event objects for your facility (same structure as division events)
    - id - Event ID (integer)
    - name - Event name
    - description - Full event description (supports markdown/HTML)
    - image_url - URL to event banner/promotional image
    - start - Event start time (Y-m-d H:i:s format)
    - end - Event end time (Y-m-d H:i:s format)
    - airports - Object containing arrival and departure airport arrays
    - positions - Object with positions array or null
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
  https://vatcar.net/api/v2/facility/events
```

### Example Response

```json
{
  "success": "Fetched successfully.",
  "data": [
    {
      "id": 158,
      "name": "ZSU Weekly Staffup – Wednesday Style",
      "description": "Enjoy live ATC Caribbean style with weekly staffups in ZSU! Join the fun every Wednesday at TJSJ and experience vibrant island vibes and professional air traffic control coverage across the San Juan region.",
      "image_url": "https://vatcar-cdn.nyc3.cdn.digitaloceanspaces.com/events/zsu-weekly-staffup-1761760736.png",
      "start": "2025-11-05 23:00:00",
      "end": "2025-11-06 02:00:00",
      "airports": {
        "arrival": ["TJSJ"],
        "departure": ["TJSJ"]
      },
      "positions": {
        "positions": []
      },
      "forum_event_id": null,
      "facilities": 64,
      "user_cid": 1561719,
      "edit_cid": 1561719,
      "created_at": "2025-10-29T16:12:04.000000Z",
      "updated_at": "2025-10-29T17:58:57.000000Z"
    }
  ]
}
```

---

## Get Facility Documents

Retrieve all facility documents organized by category.

```
GET https://vatcar.net/api/v2/facility/documents
```

==- Request [!badge corners="round" variant="success" text="GET"]
No parameters required. Returns documents for the facility associated with your API key.
==- Response
Array of document category objects:
- name - Category name (e.g., "Policies", "Training Documents", "SOPs")
- files - Array of document file objects
    - name - Document name
    - details - Document description (nullable)
    - updated_at - Last update date (d-M-Y format)
    - url - Direct URL to the document file
===

### Example Request

```bash
curl -H "api_key: your_api_key_here" \
  https://vatcar.net/api/v2/facility/documents
```

### Example Response

```json
[
  {
    "name": "Policies",
    "files": [
      {
        "name": "General Policies & Procedures",
        "details": "Facility General Policies & Procedures",
        "updated_at": "31-Oct-2025",
        "url": "https://vatcar.net/division/document/ZSU-GEN-100.pdf"
      }
    ]
  },
  {
    "name": "Training Documents",
    "files": [
      {
        "name": "Phraseology Manual",
        "details": "Facility Phraseology Manual",
        "updated_at": "31-Oct-2025",
        "url": "https://sanjuan.vatcar.net/wp-content/uploads/2023/07/SAN-JUAN-CERAP-_-Phraseology-Manual.pdf"
      },
      {
        "name": "San Juan CERAP Training Syllabus S1",
        "details": null,
        "updated_at": "31-Oct-2025",
        "url": "https://vatcar.net/division/document/ZSU-TRG-903.pdf"
      }
    ]
  },
  {
    "name": "Standard Operating Procedures (SOPs)",
    "files": [
      {
        "name": "San Juan ATCT SOP",
        "details": null,
        "updated_at": "31-Oct-2025",
        "url": "https://vatcar.net/division/document/ZSU-SOP-TJSJ - San Juan ATCT.pdf"
      }
    ]
  }
]
```

!!!warning Authentication Required
Document URLs require authentication to access. Users must be signed in to VATCAR to download documents. Unauthenticated requests to document URLs will fail.
!!!