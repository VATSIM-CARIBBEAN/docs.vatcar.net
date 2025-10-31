---
label: "Facility"
icon: briefcase
order: 90
---

# Facility API

## Roster

```
https://vatcar.net/api/v2/facility/roster
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

---

## Events

```
https://vatcar.net/api/v2/facility/events
```

==- Request [!badge corners="round" variant="success" text="GET"] 

==- Response
- success
- data
===

---

## Documents

```
https://vatcar.net/api/v2/facility/documents
```

!!!danger
Documents are no longer hosted locally, thus this endpoint is currently unavailable.
!!!

==- Request [!badge corners="round" variant="success" text="GET"] 

==- Response
- success
- data
===