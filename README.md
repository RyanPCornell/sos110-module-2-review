# SOS 110 — Module 2 Review: Ecosystem Services of Grand Canyon National Park

A four-slide web deck for the in-class hand-off of the Module 2 Review.

**Live:** https://ryanpcornell.github.io/sos110-module-2-review/

1. **Title**
2. **Announcements** — upcoming assignments, plus a live attendance roll call the
   instructor runs from the `?host` copy of the deck.
3. **The assignment**, set as a course handout — objective, the three tasks, and
   the submission guidelines.
4. **★ Module 2 SET Builder** — a drag-and-drop sandbox for building the mind map
   the assignment asks for: list the park's native plants and animals from
   official sources, map all four categories of ecosystem service, link each one
   to a concrete sustainability outcome, trace how a human pressure harms them,
   write the four-part impact analysis, then **Save as PDF** for Canvas.

Everything is self-contained — no build step, no dependencies, no media folder.
The only external requests are Google Fonts.

## Running it in class
Open the live link. Press <kbd>→</kbd> / <kbd>space</kbd> or click to advance;
<kbd>M</kbd> or the ☰ button opens the slide menu.

Add `?host` to the URL for the instructor copy, which gets the **Attendance**
button on slide 2. Pick the section from the dropdown, press **Attendance** to
open the sign-in pop-up on every student's copy, then **Submit Attendance** to
close the roll call and mail the roster.

## Built from
`_deck-builder/module2_assignment.py` + `_deck-builder/module2_set_builder.py`
(not in this repo — this is the built output).

    DECK_OUT=".../module-2-assignment-web/index.html" python3 module2_assignment.py

`firebase-config.js` holds the Firebase web config and the attendance endpoints.
Those values are not secrets — they ship in every web page that uses them, and
access is controlled by the Firestore security rules. No student data is written
to Firestore; attendance goes straight from the browser to a Google Form.
