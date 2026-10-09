# Changelog

The version appears in InnovaTime's nav bar. Versions 1.3.0 and 1.4.0 were
assigned afterwards to group the changes made while the label still read
v1.2.1; 1.5.0 is the first release to show its own number.

## v2.6.0 — 2026-10-09
- New Entry: a running day total for the picked date, in a blue box next
  to the "Your entry will show here" strip above Save (the strip keeps the
  left half, the day total takes the right half; on a phone they stack).
  It reads e.g. **4.5 h** logged on Fri, 10/2, updates when you change the
  date, and as you type hours the second line shows the new total, e.g.
  **6 h** with this one. Edit Entry is unchanged.
  - Counts all of that person's time on the date (any client or activity);
    parts aren't counted
  - When an admin adds time for someone else, it shows that person's total

## v2.5.1 — 2026-10-09
- Hertzfeld Poultry Farms (HPF): LAB time is now capped at 4 hours per
  month, shared by all techs — the same as RMH and TNEC (5 hours each).
  Going over offers the same split: the part that fits as LAB, the rest as
  OOCH.

## v2.5.0 — 2026-10-08
- Client Detail Report Print (one client or several selected) and Download
  PDF no longer show CON hours or the date range anywhere — not in the
  header, the Billed heading or the footer. The screen still shows both.
  - The PDF file name still carries the month, e.g. AJDoor102026.pdf
- Both now end with a Total Time for the outstanding entries:
  - Print: a Total Time box under the table (with entries ticked, it
    totals just those)
  - PDF: a TOTAL TIME row closing the table
- Print no longer spits out a blank last page when the report ends near
  the bottom of a page

## v2.4.0 — 2026-10-08
- Client Detail Report: with 2 or more entries ticked, a **Remove (n)**
  button now sits at the top next to Mark Billed and Hold, so you can take
  several entries out of the client's report at once. Like the single
  Remove, they stay on each employee's own hours, Print Slip and User
  Reports, and show under Removed From Report where they can be restored.
- Client Detail Report: the title row with the Mark Billed, Hold, Remove,
  Print and Download PDF buttons now stays pinned at the top of the screen
  as you scroll down the entries, like it does on Client Reports
- When the buttons don't all fit on one line, they now wrap to the right
  and the client name drops under the title as a whole instead of breaking
  mid-name

## v2.3.0 — 2026-10-07
- New Entry and Edit Entry look livelier. Entering time works exactly the
  same — same fields, same pickers, same Tab/Enter flow.
  - A soft blue-to-lime light travels around the edge of the form, with
    faint glows behind it (light and dark mode)
  - A green check pops into Client Code and Activity Code once picked
  - The box you're typing in glows blue; hours show bigger and bolder
  - A strip above Save reads the entry back as you fill it in, e.g.
    USI · LAB · 1.5 hours on Wed 10/7, and turns green when it's complete
  - Save shines on hover and pulses gently once the entry is ready
  - A small burst of confetti after "Time entry added"
- Fixed: the client list sometimes popped open while New Entry was still
  sliding in (or didn't open at all). It now waits for the page to settle,
  then unrolls down from the box with its rows following one after another.
  The activity list opens the same way.
- Animations are skipped for anyone whose computer is set to reduce motion

## v2.2.0 — 2026-10-07
- RMH and TNEC: going over the 5 LAB hours a month no longer just blocks
  the entry. InnovaTime offers to split it instead:
  - A card shows how many LAB hours are already logged, how much of this
    entry still fits as LAB, and how much goes over the cap as OOCH
  - **Save as 2 entries** saves the part that fits as LAB and the rest as
    OOCH (same date, notes and project)
  - **Only log the X h of LAB** saves just the part that fits
  - Once the month's 5 hours are used up, the button reads **Save it as
    OOCH**
  - Works on Edit Entry too: the entry keeps the LAB hours that fit and a
    new OOCH entry is added for the rest
  - If there's no active OOCH activity code, it falls back to the old
    message and doesn't save

## v2.1.0 — 2026-10-07
- Ronald McDonald (RMH) and The National Exchange Club (TNEC): LAB time is
  capped at 5 hours per month, shared by all techs
  - The month is the entry's date, not today's date. All LAB entries for that
    month count, billed or not.
  - Saving a LAB entry that would go over 5 hours is blocked with a message
    like "The National Exchange Club currently has 3.5 hours logged, please
    log 1.5 hours and any additional will be put under OOCH". Re-enter up to
    the remaining hours as LAB and log the rest as OOCH.
  - Other activity codes (OOCH, PRT, DT, …) are not capped
  - Applies to New Entry and Edit Entry. Editing an existing entry doesn't
    count that entry's old hours against itself.

## v2.0.0 — 2026-10-05
- New look ("Studio Light") across every page, with the new InnovaTime logo
  - The menu moves to a sidebar on the left, with an icon for each page
  - Brighter cards, bigger page titles and blue-to-green totals
  - On tablets and phones the sidebar becomes a bar across the top
  - Printouts and PDFs are unchanged
- New Settings button (gear) at the bottom of the sidebar, next to Log out
  - Appearance: Light, Dark, or Auto (follows the computer's setting)
  - Finding clients when entering time: Default (as before) or Codes —
    codes come first, so typing USI + Tab picks Upword Solutions (USI)
    instead of a client whose name contains "usi". Clients that only match
    by name are listed below under "Also matches by name". Applies to New
    Entry and Edit Entry.
  - Settings are saved to each person's login, so they stick every time
    they log in, on any computer. Everyone starts on Light + Default.
  - The database gets two new settings columns automatically the first
    time the updated app starts — nothing to do by hand

## v1.13.0 — 2026-10-05
- Client Detail Report, Print and multi-client print: the TOTAL line of the
  Outstanding and Billed tables now shows Labor (hours and $) and Parts ($)
  subtotals to the left of TOTAL, e.g.
  LABOR 1.75 hrs $262.50   PARTS $149.00   TOTAL 1.75 $411.50
  - Printing with entries ticked recalculates the subtotals for just those
    entries
- Fixed: v1.12.1 accidentally put back an older copy of the Client Detail
  Report page (Month/Year links, Mark Billed using month/year, dates not in
  month/day/year). The v1.12.0 From/To version is restored.

## v1.12.1 — 2026-10-05
- Client Detail Report, Print, multi-client print and Download PDF: the CON
  Hours box now shows all CON hours used for that client in the From/To
  range — outstanding and billed, held entries included. It used to skip
  held entries, so it could read 0.00 under a page full of CON work.
  - It always shows the whole range's CON total, even when printing or
    downloading just the ticked entries

## v1.12.0 — 2026-10-05
- Client Reports: the Month and Year boxes are replaced by From Date and
  To Date (like User Reports), so you can pick any range of days. It starts
  on the 1st of this month through today.
  - Unbilled and Billed show only entries dated within the range. Unbilled
    work from before the From date no longer carries forward on its own,
    so set the From date back to catch anything older.
  - Mark Billed and Unmark apply only to that client's entries within the
    range
  - The Client Detail Report, Print, multi-client print and Download PDF
    use the same From/To dates. A whole month still reads "October 2026"
    (and the PDF is still named e.g. AJDoor102026.pdf); any other range
    shows both dates, e.g. 10/01/2026 – 10/15/2026

## v1.11.0 — 2026-10-02
- Client Reports: the title row with the Mark Billed, Print and Back buttons
  now stays pinned at the top of the screen as you scroll down the client
  list

## v1.10.0 — 2026-10-01
- Client Reports: non-chargeable time (Non-Billable, Drive Time, … — any
  activity marked Chargeable: NO) no longer shows on client reports or counts
  toward a client's unbilled hours and dollars. Parts always show.
  - Applies to the Client Detail Report, Print, Download PDF, the
    multi-client print and the Client Reports totals
- Client Detail Report, Print and PDF:
  - Parts are listed at the bottom; everything else stays in date order
  - Dates read month/day/year, e.g. 09/22/2026
  - The Client box shows the client's name first, with the code underneath
- Admin → Users: new Edit button to change a user's name, code or username
  (e.g. Andrew Towers' code to ATT). Their past entries show the new code.

## v1.9.2 — 2026-09-28
- Client Detail PDF: redesigned in InnovaTek's colors
  - InnovaTek logo at the top, with blue-and-green accents to match it
  - The client's code is no longer shown — just their name
  - CON Hours Used stands out in its own box, and the table has a blue
    header row with alternating row shading
  - Later pages repeat a smaller logo and the column headings

## v1.9.1 — 2026-09-28
- User Reports: each person's totals line now shows Non-Chargeable Hours next
  to Chargeable Hours

## v1.9.0 — 2026-09-28
- Client Detail Report: Download PDF button next to Print
  - The PDF shows the CON hours used, then each outstanding entry's Date,
    Employee, Activity, Hours and Notes, in the same order as the report
  - Named client + month + year, e.g. AJ Door for September 2026 downloads
    as AJDoor092026.pdf
  - With entries ticked, the PDF holds just those (like Print)
  - Built into the app — nothing new to install on the server

## v1.8.1 — 2026-09-25
- Client Reports: Mark Billed (single or bulk) and Unmark keep you on the same
  tab instead of jumping to Billed/Unbilled
- Buttons that refresh the page (Mark Billed, Hold, …) keep your scroll
  position, and the client search text is kept

## v1.8.0 — 2026-09-25
- Client Detail Report: checkboxes on outstanding entries
  - Print with entries ticked prints just those entries, with totals for them
  - With 2 or more ticked, Mark Billed, Hold and Unhold buttons appear next to
    Print to act on all ticked entries at once

## v1.7.0 — 2026-09-25
- Client Reports: search box to filter clients by code or name as you type
  (Esc clears it); the select-all checkbox only picks the clients shown

## v1.6.0 — 2026-09-25
- Client Reports: when 2 or more unbilled clients are checked, a Mark Billed
  button appears next to Print to mark them all billed at once

## v1.5.0 — 2026-09-24
- Print Slip: Delete button next to Edit (users delete their own time, admins anyone's)
- Animations throughout: page entrances, gliding nav highlight and tab underline,
  count-up stats, pop-up messages (toasts), button spinners, animated admin dialogs
- Fixed the login error showing twice and the unstyled Logout button
- Client Reports: checkboxes to print selected clients' details
- Client Reports: Delete now only removes an entry from the report
- Admin → Clients: edit a client's code and name
- Simpler printed client detail report; narrower printed Notes column

## v1.4.0 — 2026-09-21
- Bill individual time entries; unbilled work rolls forward to the next month
- Admins can add and edit time for other users from Print Slip
- Admin page stays on the active tab after add/edit/delete
- Database updates now run automatically on startup

## v1.3.0 — 2026-09-16
- User Reports: everyone's hours for a From/To date range
- User Reports print view: chargeable vs. non-chargeable breakdown with % totals
  (USI/ISI time is never chargeable)
- New Entry: Client Code is focused on open, Tab skips the calendar icon, and
  the page stays open after saving
- Client Detail Report columns reordered to Activity, Employee, Date
- Lighter color theme

## v1.2.1 — 2026-09-04
- Starting point (first upload to GitHub)
