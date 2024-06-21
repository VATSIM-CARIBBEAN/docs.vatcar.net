---
label: "Facility"
icon: book
order: 90
---

# Facility API

## Authentication

API Key

## Roster

```
https://vatcar.net/public/api/v2/facility/roster
```

==- Request [!badge corners="round" variant="success" text="GET"] 

==- Response
- success
- data
    - facility
    - staff
        - atm
        - datm
        - ta
        - ec
        - fe
        - wm
    - controllers
    - visitors
===

## Events

```
https://vatcar.net/public/api/v2/facility/events
```

==- Request [!badge corners="round" variant="success" text="GET"] 

==- Response
- success
- data
===