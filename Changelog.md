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

## v1.1.6 [!badge variant="info" text="LATEST"]

Released: August 19, 2024

+++ New
- [x] New Staffing Request Form
    - Sends an e-mail to VATCAR5 as well as a Discord message
- [x] Added Tier 2 Endorsement on Roster for TNCF and TJZS


+++ Updated
- [x] Added TNCM to San Juan's approach list for accurate display of online facilities
- [x] Remove visitor flag automatically when transferred into academy
- [x] Resolved entry exam not being assigned due to user being in academy
- [x] List paginations updated so it is easier to navigate
- [x] Division Staff can now see all event rosters
- [x] Event roster only shows positions that are assigned within the facility
- [x] Front page carousel pictures randomly chosen between 9 options
- [x] Training Notes member dropdown shows all controllers for VATCAR Division Staff
- [x] Minor security updates and code cleanup for efficiency
+++

---

## v1.1.5

Released: July 22, 2024

+++ New
- [x] New Partners Page
- [x] Event roster system implemented
    - Enhancements are still a work in progress, this is just the basic working progress
    - Positions can be added from the event edit menu, NOT event create menu
    - Any home/visiting controller can see roster and sign up/remove themselves
    - Facility Staff, Event Coordinators, and Division Staff can force remove individuals

+++ Updated
- [x] Premature solo certifications being deleted resolved
- [x] Visitor flag removed once accepted into VATCAR
- [x] Random documents being deleted resolved
- [x] Entry exam no longer automatically assigns everyone into VATCAR (breaks transfer page)
- [x] Appropriate notifications for division staff regarding tickets
- [x] Rating upgrade button removed
- [x] Caribbean tech page removed
+++

---

## v1.1.4

Released: July 10, 2024

+++ New
- [x] Added partners page
+++ Updated
- [x] Feedback page accessible only when logged in
- [x] Training notes character limit is now 4000
+++

---

## v1.1.3

Released: July 9, 2024

+++ New
- [x] Mentors can now be assigned to students
    - They have access to My Students page now
- [x] Document page now have multiple sub-categories
    - Standard Operating Procedures (SOPs)
    - Letters of Agreement (LOAs)
    - Training Documents
    - Policies
    - Reference Documents
    - Files
- [x] Controller Feedback page added
+++ Updated
- [x] Endorsement page is now visible by Air Traffic Managers (typo that was resolved)
- [x] Attempt to DM users that have their Discord DMs closed will no longer cause a fatal error
- [x] Document categories appropriately aligned
- [x] Event discord notification fixed
- [x] Entry exam minor issues fixed 
- [x] Edit and uploading documents limit increased to 50mb
+++

---

## v1.1.2

Released: July 4, 2024

+++ Updated
- [x] Endorsements appropriately updated for each facility
- [x] Discord event notifications fixed so that it only alerts facility controllers
- [x] Caribbean FSS changed to Caribbean Super Centers with appropriate endorsement names
- [x] Email and Discord Notifications for division transfer requests
- [x] OTS marking sheets now viewable
- [x] Disabled standalone OTS system - use training notes instead
- [x] CBT modules now automatically refresh the page when exitting
- [x] Delete button hidden on tickets except for division staff
- [x] Facility webmasters no longer have access to welcome email settings
- [x] Transfers from academy, non-members, and inactive facility do not count towards the 90 day transfer requirement
- [x] Activity page fixed - hours are now accurate for the last 90 days
+++

---

## v1.1.1

Released: July 1, 2024

+++ Updated
- [x] Added entry exam requirement for visitors
- [x] Event endorsement removed
- [x] Activity page fixed
- [x] Visitors are shown better on top controllers
- [x] Updated acceptance email formatting
- [x] Piarco Control changed to Piarco Radar on map
- [x] Top Controllers and Facilities Stats fixed
- [x] Changed transfer requirement from S1 to OBS
- [x] Hid unnecessary endorsements to applicable facilities
- [x] Updated facility images
+++ New
- [x] Weather data API (internal)
+++

---

## v1.1.0

Released: June 27, 2024

**Released to the Public**

+++ New
- [x] Opened for public release
- [x] Added Policy
- [x] New Division API (internal)
+++ Updated
- [x] Flight Track Map is Light Mode
- [x] Map shows callsign of online center facility
+++

---

## v1.0.6

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