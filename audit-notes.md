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
