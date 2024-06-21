---
label: "User"
icon: person
order: 80
---

# User API

## User

```
https://vatcar.net/public/api/v2/user/:user_cid
```

=== Request [!badge corners="round" variant="success" text="GET"] 
- user_cid [!badge corners="pill" variant="danger" text="REQUIRED"]
==- Response
- success
- data
    - cid 
    - first_name
    - last_name
    - email_preferences
    - facility
    - facility_join
    - rating
    - last_active
    - flag_basic
    - flag_is_visitor
    - flag_xferOverride
    - last_api_check
    - created_at
    - updated_at
    - fir
    - visiting_facilities
===

---

## Notes

```
https://vatcar.net/public/api/v2/user/:user_cid/notes
```

=== Request [!badge corners="round" variant="success" text="GET"] 
- user_cid [!badge corners="pill" variant="danger" text="REQUIRED"]
==- Response
- success
- notes
===