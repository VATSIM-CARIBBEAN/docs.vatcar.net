---
label: "Facility"
icon: book
order: 100
---

# Facility API

## Authentication

API Key

## Roster

```
[!badge corners="round" variant="success" text="GET"] https://vatcar.net/public/api/v2/facility/roster
```

=== Request

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
[!badge corners="round" variant="success" text="GET"] https://vatcar.net/public/api/v2/facility/events
```

=== Request

==- Response
- success
- data
===