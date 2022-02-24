# Clockin_Clockout_UI
Workforce.com Junior Product Designer code challenge submission

# Design Process
## Assumptions
1. The user could stay clocked in indefinitely
2. rendering map view is not necessary to still retrieve user's geolocation and save to db
  * the map view might actually be more useful for a manager's view
3. User can view their past shifts in the past week.
  * The current design assumes that this user has longer shifts where they do 1 shift per day 
  * (I realized afterward that the layout of these components probably doesn't consider all scenarios, e.g. users could have multiple shifts on a single day.)
4. User might want to submit multiple shift notes.

## Design choices
1. call to action "Clock In" is made in bold pink typefont to draw user's attention
2. designed what the past shift components might look like
  * considered that there may be many shifts and adding scrolling capability
3. made sure that the map, clock-in button, and the clocked-in view are all non-scrollable views
  * design should make it easy to access the main call-to-action no matter what the user does on the view
  * since call-to-action "Clock Out" is placed at the bottom of the screen, I didn't want it to ever scroll off
4. added "submit note" button for user to submit multiple shift notes
  * user can also visually confirm that their note is being saved
5. Clocked-in Timer is based off of the current date and time. This makes it dependent on the user's device's actual internal clock rather than an arbitrary counter.
6. "Clock Out" button is larger than origianl design and fixed to the bottom of the screen
  * was a better visual offset against the "submit note" button
  * also filled the screen's white space better. Larger is also easier to press.

## What I would change or improve on
1. The shift components were designed with the header being the day the user worked their shift. If the user worked **multiple shifts in a single day**, it might be better to display either the company they worked a shift for or the shift time-range + the day (ex: Mon, 10am-2pm).
2. Some HTML elements have the same utility classes used. I noticed Tailwind allows customization and building your own styling off of their library. This might be useful for **minimizing redundancy of code**.
3. UI **responsiveness for mobile views**
  * UI worked on multiple forms of mobile displays (I mainly tested with iPhone XR, iPhone 12 Pro, Samsung Galaxy S20)
  * BUT, not all mobile screens worked, and some allowed scrolling the screen on top of scrolling through the shifts
