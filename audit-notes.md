## Run one automated check and record what it finds

axe-core 4.10.3, 3 Oct 2026, local practice page. Three violations.

Submit button has no name. Rule is button-name. Impact is critical. The control is `<button type="submit"></button>`.

Heading level goes from h1 to h3. Rule is heading-order. Impact is moderate. The hero has `<h1>Community Tech Day</h1>`, then `<h3>Free workshops for neighbors learning practical web skills.</h3>`.

Name and email have no label. Rule is label. Impact is critical. Name sits beside `<span>Name *</span>`. Email sits beside `<label>Email</label>`, and that label has no for attribute.
