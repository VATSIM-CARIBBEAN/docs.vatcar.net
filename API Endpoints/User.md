---
label: "User"
icon: person
order: 80
---

# User API

Get information about specific users in the VATCAR system.

## Get User Information

Retrieve detailed information about a specific user by their VATSIM CID.

```
GET https://vatcar.net/api/v2/user/:user_cid
```

=== Request [!badge corners="round" variant="success" text="GET"]
- user_cid [!badge corners="pill" variant="danger" text="REQUIRED"] - The VATSIM CID of the user
==- Response
- success - String message indicating request status
- data - Object containing user information
    - cid - VATSIM CID (integer)
    - first_name - User's first name
    - last_name - User's last name
    - email - Email address associated with VATSIM account
    - email_preferences - Bitmask integer for email notification preferences
    - facility - Facility ID (integer)
    - facility_join - Date user joined their current facility (nullable)
    - rating - VATSIM ATC rating (1=OBS, 2=S1, 3=S2, 4=S3, 5=C1, etc.)
    - last_active - Timestamp of last activity
    - flag_visible - Boolean for account visibility
    - flag_basic - Boolean indicating if user completed basic requirements
    - flag_staff_assign - Boolean for staff assignment flag
    - flag_is_visitor - Boolean indicating if user is a visitor
    - flag_xferOverride - Boolean for transfer override flag
    - last_api_check - Last time VATSIM API was checked for this user
    - created_at - Account creation timestamp
    - updated_at - Last update timestamp
    - integrations - Array of third-party integrations (Discord, etc.)
    - fir - Object containing FIR details (id, name_long, name_short, etc.)
    - visiting_facilities - Array of facility objects with visit details
    - role_assignments - Array of staff role assignments (if applicable)
===

### Example Request

```bash
curl -H "api_key: your_api_key_here" \
  https://vatcar.net/api/v2/user/1234567
```

### Example Response

```json
{
  "success": "User fetched successfully.",
  "data": {
    "cid": 1234567,
    "first_name": "John",
    "last_name": "Doe",
    "email": "john.doe@example.com",
    "email_preferences": 4095,
    "facility": 8,
    "facility_join": "2024-01-15T10:30:00.000000Z",
    "rating": 3,
    "last_active": "2025-10-30 14:22:35",
    "flag_visible": 1,
    "flag_basic": 1,
    "flag_staff_assign": 0,
    "flag_is_visitor": 0,
    "flag_xferOverride": 0,
    "last_api_check": "2025-10-25 18:45:12",
    "created_at": "2023-12-01T09:15:32.000000Z",
    "updated_at": "2025-10-30T14:22:35.000000Z",
    "integrations": [
      {
        "id": 42,
        "type": 1,
        "user_cid": 1234567,
        "value": "123456789012345678",
        "created_at": "2024-03-15T08:22:11.000000Z",
        "updated_at": "2024-03-15T08:22:11.000000Z"
      }
    ],
    "fir": {
      "id": 8,
      "name_long": "San Juan CERAP",
      "name_short": "TJZS",
      "website_url": "https://sanjuan.vatcar.net/",
      "email_format": "sanjuan.vatcar.net",
      "fir_description": "San Juan CERAP",
      "is_fir": 1,
      "created_at": "2024-05-09T07:19:26.000000Z",
      "updated_at": "2024-05-11T00:21:56.000000Z"
    },
    "visiting_facilities": [
      {
        "id": 12,
        "user_cid": 1234567,
        "facility_id": 4,
        "flag_visible": 1,
        "created_at": "2024-06-10T12:15:20.000000Z",
        "updated_at": "2025-08-14T09:30:45.000000Z",
        "fir": {
          "id": 4,
          "name_long": "Nassau FIR",
          "name_short": "MYNN",
          "website_url": "https://nassau.vatcar.net/",
          "email_format": "nassau.vatcar.net",
          "fir_description": "Nassau FIR",
          "is_fir": 1,
          "created_at": "2024-05-09T07:19:26.000000Z",
          "updated_at": "2024-05-11T00:20:50.000000Z"
        }
      }
    ],
    "role_assignments": []
  }
}
```

---

## Get User Training Notes

Retrieve all training notes for a specific user.

```
GET https://vatcar.net/api/v2/user/:user_cid/notes
```

=== Request [!badge corners="round" variant="success" text="GET"]
- user_cid [!badge corners="pill" variant="danger" text="REQUIRED"] - The VATSIM CID of the user
==- Response
- success - String message indicating request status
- notes - Array of training note objects
    - id - Note ID (integer)
    - user_cid - VATSIM CID of the student
    - instructor_cid - VATSIM CID of the instructor
    - instructor_name - Instructor's full name
    - facility_id - Facility ID where training occurred
    - position_trained - Position/certification trained on
    - training_note - Detailed training notes (supports markdown)
    - session_type - Type of session (0=sweatbox, 1=live network, 2=OTS, 3=classroom)
    - marking_sheet - Filename of attached marking sheet (nullable)
    - ots_pass - Boolean indicating OTS pass/fail (0=fail/not applicable, 1=pass)
    - friendly_time - Human-readable date (Y-m-d format)
    - created_at - Creation timestamp
    - updated_at - Last update timestamp
===

### Example Request

```bash
curl -H "api_key: your_api_key_here" \
  https://vatcar.net/api/v2/user/1234567/notes
```

### Example Response

```json
{
  "success": "Notes retrieved successfully.",
  "notes": [
    {
      "id": 196,
      "user_cid": 1234567,
      "instructor_cid": 7654321,
      "instructor_name": "John Doe",
      "facility_id": 8,
      "position_trained": "SJU_2_CTR",
      "training_note": "C1 OTS Evaluation see notes contained in PDF",
      "session_type": 2,
      "marking_sheet": "1234567-ms-13030.pdf",
      "ots_pass": 1,
      "friendly_time": "2025-01-13",
      "created_at": "2025-01-13T08:18:39.000000Z",
      "updated_at": "2025-01-13T08:18:39.000000Z"
    },
    {
      "id": 177,
      "user_cid": 1234567,
      "instructor_cid": 7654321,
      "instructor_name": "Jane Doe",
      "facility_id": 8,
      "position_trained": "SJU_2_CTR",
      "training_note": "Training Note Here",
      "session_type": 0,
      "marking_sheet": null,
      "ots_pass": 0,
      "friendly_time": "2024-12-09",
      "created_at": "2024-12-09T04:31:49.000000Z",
      "updated_at": "2024-12-09T04:31:49.000000Z"
    }
  ]
}
```

### Error Response

If your API key does not have permission to access the requested user's training notes:

```json
{
  "error": "You do not have permission to view this controllers notes."
}
```

!!!warning Permission Requirements
Training notes can only be accessed if the user belongs to your facility or if your API key has division-level access. Attempting to access notes for users outside your facility scope will result in a permission error.
!!!