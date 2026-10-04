## Run one automated check and record what it finds

axe-core 4.10.3, 3 Oct 2026, local practice page. Three violations.

Submit button has no name. Rule is button-name. Impact is critical. The control is `<button type="submit"></button>`.

Heading level goes from h1 to h3. Rule is heading-order. Impact is moderate. The hero has `<h1>Community Tech Day</h1>`, then `<h3>Free workshops for neighbors learning practical web skills.</h3>`.

Name and email have no label. Rule is label. Impact is critical. Name sits beside `<span>Name *</span>`. Email sits beside `<label>Email</label>`, and that label has no for attribute.

## Test keyboard navigation and visible focus manually

Chrome, Tab and Shift+Tab, 3 Oct 2026, local practice page.

Tab order is Sessions, Register, Schedule, Start, More, More, More, the name field, the email field, then the submit button. The next Tab returns to Sessions. Shift+Tab reverses that order. Nothing traps focus.

Each focused link, field, and the submit button computes to `outline-style: none` and `box-shadow: none`. Start was focused and showed no ring.

Start is a link. Enter moves to `#register` and focus lands on the body. Space leaves focus on Start.

The submit button is in the tab order and has no text.

## Test keyboard navigation and visible focus manually

3 Oct 2026, local practice page. Focus moved through 10 controls in page order: Sessions, Register, Schedule, Start, More, More, More, name, email, submit.

Each focused link, input, and the submit button has outline-style none and box-shadow none. Background, border, color, and underline match the unfocused control.

Header links and Start have text-decoration none while focused. The three More links stay underlined, same as unfocused.

## Check landmarks, headings, links, buttons, and image alternatives

Accessibility tree, 3 Oct 2026, local practice page.

Landmarks in the tree: banner, navigation, main. Each has no name. There is no contentinfo. The form is not a landmark. Three article elements are in the tree with no name.

Headings: h1 Community Tech Day, h3 Free workshops for neighbors learning practical web skills, h2 Featured sessions, h3 Safer Passwords, h3 Accessible Forms, h3 Responsive Layouts, h2 Register interest, h2 Workshop schedule.

Links: Sessions goes to #sessions. Register goes to #register. Schedule goes to #schedule. Start goes to #register. Three links are named More and the href on each is #.

The only button is the submit button. Its name is empty.

All three images use workshop.svg. The file is a gold and maroon graphic with three figure shapes. The first image name is poster. The second has alt="" and is not in the tree. The third image name is People attending a workshop.
