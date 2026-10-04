## Run one automated check and record what it finds

axe-core 4.10.3. Three violations.

Submit button has no name. Rule is button-name. Impact is critical. The control is `<button type="submit"></button>`.

Heading level goes from h1 to h3. Rule is heading-order. Impact is moderate. The hero has `<h1>Community Tech Day</h1>`, then `<h3>Free workshops for neighbors learning practical web skills.</h3>`.

Name and email have no label. Rule is label. Impact is critical. Name sits beside `<span>Name *</span>`. Email sits beside `<label>Email</label>`, and that label has no for attribute.

## Test keyboard navigation and visible focus manually

Chrome, Tab and Shift+Tab.

Tab order is Sessions, Register, Schedule, Start, More, More, More, the name field, the email field, then the submit button. The next Tab returns to Sessions. Shift+Tab reverses that order. Nothing traps focus.

Each focused link, field, and the submit button computes to `outline-style: none` and `box-shadow: none`. Start was focused and showed no ring.

Start is a link. Enter moves to `#register` and focus lands on the body. Space leaves focus on Start.

The submit button is in the tab order and has no text.

## Test keyboard navigation and visible focus manually

Focus moved through 10 controls in page order: Sessions, Register, Schedule, Start, More, More, More, name, email, submit.

Each focused link, input, and the submit button has outline-style none and box-shadow none. Background, border, color, and underline match the unfocused control.

Header links and Start have text-decoration none while focused. The three More links stay underlined, same as unfocused.

## Check landmarks, headings, links, buttons, and image alternatives

Accessibility tree.

Landmarks in the tree: banner, navigation, main. Each has no name. There is no contentinfo. The form is not a landmark. Three article elements are in the tree with no name.

Headings: h1 Community Tech Day, h3 Free workshops for neighbors learning practical web skills, h2 Featured sessions, h3 Safer Passwords, h3 Accessible Forms, h3 Responsive Layouts, h2 Register interest, h2 Workshop schedule.

Links: Sessions goes to #sessions. Register goes to #register. Schedule goes to #schedule. Start goes to #register. Three links are named More and the href on each is #.

The only button is the submit button. Its name is empty.

All three images use workshop.svg. The file is a gold and maroon graphic with three figure shapes. The first image name is poster. The second has alt="" and is not in the tree. The third image name is People attending a workshop.

## Test zoom/reflow at 200% or a narrow responsive condition

Layout width 640px. That width is 200% zoom on a 1280px window.

Page scroll width is 980px. Viewport client width is 625px. A horizontal scrollbar is present.

The header min-width is 980px and the header is 980px wide. Sessions, Register, and Schedule sit past the right edge until the page is scrolled sideways.

main is width 980px. The hero sentence stops at the viewport edge. The rest of the sentence is to the right.

The cards stay in three columns, 292px 292px 292px. The third card is off the right edge.

At a 320px window the header is still 980px, main is still 980px, and the cards are still three columns. Scroll width stays 980px.

## Identify at least five issues and remediate at least three

Submit button has no name. Evidence: `<button type="submit"></button>`. Impact is critical. Priority is high. Fix: button text is Register. Retest: the button name is Register.

Name and email have no label. Evidence: Name is a span. The email label has no for. Impact is critical. Priority is high. Fix: both are labels with for. Both fields are required. The email label includes the asterisk. Retest: the name field label is Name *, and the email field label is Email *. Both are required.

Focus ring is missing. Evidence: focused links, fields, and the submit button compute to outline-style none and box-shadow none. Impact is serious. Priority is high. Fix: the outline none rule is removed. Retest: Tab through the links, the name field, the email field, and Register. Each is focus-visible, with outline-style auto, 1px, rgb(0, 95, 204).

Heading level goes from h1 to h3. Evidence: the hero has an h1, then an h3. Impact is moderate. Priority is medium. Not changed.

The page does not reflow below 980px. Evidence: at 640px and 320px the header and main stay 980px wide and the cards stay three columns. Impact is serious. Priority is high. Not changed.
