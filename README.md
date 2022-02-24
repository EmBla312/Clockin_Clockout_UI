# Clockin_Clockout_UI
Workforce.com Junior Product Designer code challenge submission

# Design Process
## Assumptions
* The user could stay clocked in indefinitely
* rendering map view is not necessary to still retrieve user's geolocation and save to db
  * the map view might actually be more useful for a manager's view
* User can view their past shifts in the past week.
  * The current design assumes that this user has longer shifts where they do 1 shift per day 
    ** (I realized afterward that the layout of these components probably doesn't consider all scenarios, e.g. users could have multiple shifts on a single day.)
* User might want to submit multiple shift notes.

## Design choices
* call to action "Clock In" is made in bold pink typefont to draw user's attention
* designed what the past shift components might look like
  * considered that there may be many shifts and adding scrolling capability
* made sure that the map, clock-in button, and the clocked-in view are all non-scrollable views
  * design should make it easy to access the main call-to-action no matter what the user does on the view
  * since call-to-action "Clock Out" is placed at the bottom of the screen, I didn't want it to ever scroll off
* added "submit note" button for user to submit multiple shift notes
  * user can also visually confirm that their note is being saved
* Clocked-in Timer is based off of the current date and time. This makes it dependent on the user's device's actual internal clock rather than an arbitrary counter.
* "Clock Out" button is larger than origianl design and fixed to the bottom of the screen
  * was a better visual offset against the "submit note" button
  * also filled the screen's white space better. Larger is also easier to press.

## What I would change or improve on
* The shift components were designed with the header being the day the user worked their shift. If the user worked multiple shifts in a single day, it might be better to display either the company they worked a shift for or the shift time-range + the day (ex: Mon, 10am-2pm).
* Some HTML elements have the same utility classes used. I noticed Tailwind allows customization and building your own styling off of their library. This might be useable for minimizing redundancy of code.
* UI responsiveness for mobile views
  * UI worked on multiple forms of mobile displays (I mainly tested with iPhone XR, iPhone 12 Pro, Samsung Galaxy S20)
  * BUT, not all mobile screens worked, and some allowed scrolling the screen on top of scrolling through the shifts
