---
label: "Changelog"
icon: log
order: 50
---

# Changelog

You will find all the updates that have happened on the website here.

!!!
Have a suggestion? E-mail j.swan@vatcar.net with your suggestion!
!!!

---

## v1.0.6 [!badge variant="info" text="LATEST"]

Released: June 26, 2024

+++ New
- [x] Added Division Transfer Requests and appropriate Admin Panel
    - If the member is not in VATCAR, the transfer page will show a division transfer request form
        - If the member is not in the Americas region, they will be prompted to submit a region transfer request
    - If the member is in VATCAR, the transfer page will show an FIR transfer request form
- [x] Visitor requirement is now S3
- [x] Added UTC time to the topbar
- [x] Local time is shown for events
- [x] New flight board page
    - Improved flight information and images
    - Heart is depicted on ALL caribbean airports
- [x] New flight map, shows FIR boundaries, current FIR centers online, and current Caribbean flights
- [x] Added cloudflare for better responsiveness
+++ Updated
- [x] Moved division dropdown to the right side for administrators
- [x] Removed auto-refresh (it caused issues with certain browsers)
- [x] Removed internal API
- [x] Fixed old.vatcar.net redirect message
- [x] Facility APIs updated
- [x] Top controllers and facilities were split into two different sections
- [x] FAQ page updated
- [x] Certification page shows if user is signed in or not
+++

---

## v1.0.5

Released: June 12, 2024

+++ New
- [x] Added Division Transfer Requests and appropriate Admin Panel
    - If the member is not in VATCAR, the transfer page will show a division transfer request form
        - If the member is not in the Americas region, they will be prompted to submit a region transfer request
    - If the member is in VATCAR, the transfer page will show an FIR transfer request form
- [x] Visitor requirement is now S3
+++ Updated
- [x] Discord permission scopes reduced to just identify
- [x] Ticket and event link updated appropriately
- [x] Events FIR selection works as intended now
- [x] E-mail responses have been appropriately updated
+++

---

## v1.0.4

Released: May 30, 2024

+++ New
- [x] Added Discord Integration!
    - This will allow users to receive website notifications through direct messages as well. Available notifications are as follows:
        1. New/Expired/Revoked/Extended solo certifications
        2. New response to active tickets
        3. New exam assigned
        4. Previous failed exam reassigned
        5. Visiting request update
        6. Transfer request update
- [x] New events posted on the website are now automatically posted in the VATCAR discord server
- [x] New announcements posted on the website are automatically sent in #vatcar-announcements.
+++ Updated
- [x] Removed Caribbean FSS and Hit Squad from Event Management Page
- [x] Increased maximum character size for exam questions
+++

---

## v1.0.3

Released: May 25, 2024

+++ Updated
- [x] Exam questions now randomize multiple choice questions
- [x] OTS stats on division management page display correct data
- [x] Visiting ratio data removed from profile and activity page
- [x] Announcements are restricted to logged in users only
- [x] Unauthorized login text is updated
- [x] Resolved fatal CBT bug causing no access to the modules
- [x] Academy users can now apply to visit facilities (do not have to be a home controller in VATCAR)
+++ New
- [x] Added documentation quick-link under profile
+++

---

## v1.0.2

Released: May 22, 2024

+++ Updated
- [x] Upcoming events on front page fixed
- [x] Visiting ratio displays correctly
- [x] Training notes no longer has a backdating option
- [x] Remove button on controller page now shows appropriate text
- [x] OTS exams can now be viewed by anyone that are able to manage training exams
- [x] Yellow banner on front page has a better sentence
- [x] Tickets page no longer shows non-existent closed tickets
- [x] Caribbean FSS and Hit Squad now show at the bottom of the FIR list
- [x] Updated Caribbean FSS logo
+++ New
- [x] Tickets and transfer forms show remaining characters needed
- [x] Added Hit Squad - VATCAR6 has ATM-like permissions for Hit Squad
+++

---

## v1.0.1

Released: May 21, 2024

+++ Updated
- [x] Documents page should be accessible to users not logged in anymore
- [x] FIR members page is now accessible when users are not logged in. Only management team is visible
- [x] Entry exam notification no longer pops up when it is already assigned
- [x] Temporarily removed uploading/viewing ticket images until resolved
- [x] Removed custom hyperlink formatting for warning bar as it affected the FAQ page
- [x] Ticket assignment no longer shows staff members duplicated
- [x] Fixed a fatal bug in CBT page
+++

---

## v1.0.0

Released: May 20, 2024

+++ New
- [x] Initial `v1.0.0` release
+++

---