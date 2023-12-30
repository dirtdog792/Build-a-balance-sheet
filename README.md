Step 1Passed
Set up your HTML with the DOCTYPE, html indicating this document is in English, head, and body elements.

Give your head element the appropriate meta elements for the charset and viewport, a title element with an appropriate title, and a link element for your stylesheet.
Step 2
Within your body element, nest a section element within a main element.
Step 3
Within your section element, add an h1 element with a nested span element.
Step 4
Screen readers announce HTML elements based on the document flow. We will eventually want the balance sheet to have a heading of "Balance Sheet" and a subheading of "AcmeWidgetCorp". However, this order does not make sense if announced by a screen reader.

Give your existing span the class attribute set to flex, and add two span elements within it. Give the first the text AcmeWidgetCorp. Give the second the text Balance Sheet. You will use CSS to reverse the order of the text on the page, but the HTML order will make more sense for a screen reader.
Step 5
Below your h1 element, create a div element. Give it an id attribute set to years. You want this particular element to be hidden from screen readers, so give it the aria-hidden attribute set to true.
Step 6
Within your div element, add three span elements. Give each of them a class attribute set to year, and add the following text (in order): 2019, 2020, and 2021.
Step 7
Below your existing div element, add a new div element with a class set to table-wrap. This will be the container for your tables.

Within that, add three table elements. You will be using CSS to style these into a single table, but using separate tables will help screen readers understand the document flow.
Step 8
HTML tables use the caption element to describe what the table is about. The caption element should always be the first child of a table, but can be positioned with the caption-side CSS property.

Add a caption element to your first table, and give it the text Assets.
Step 9
The thead and tbody elements are used to indicate which portion of your table is the header, and which portion contains the primary data or content.

Add a thead and tbody to your first table, below the caption element.
Step 10
The tr element is used to indicate a table row. Add a tr element within your thead element. In your new tr element, add a td element, followed by three th elements.

The td element indicates a data cell, while the th element indicates a header cell.
Step 11
Within each of your new th elements, nest a span element with the class set to sr-only year. Give them the following text (in order): 2019, 2020, and 2021.

Give your third th element the class attribute set to current.

Leave the td element empty. This element exists only to ensure your table has a four-column layout and associate the headers with the correct columns.
Step 12
Within your tbody element, add four tr elements. Give the first three a class attribute set to data, and the fourth a class attribute set to total.
Step 13
In your first tr, add a th element with the text Cash This is the cash we currently have on hand.. Wrap all of that text except Cash in a span element with the class set to description.

Following that, add three td elements with the following text (in order): $25, $30, $28. Give the third td element a class attribute set to current.
Step 14
In your second tr element, add a th element with the text Checking Our primary transactional account.. Wrap that text, except for Checking , in a span element with the class attribute set to description.

Following that, add three td elements with the following text (in order): $54, $56, $53. Give the third td element a class attribute set to current.
Step 15
In your third tr element, add a th element with the text Savings Funds set aside for emergencies.. Wrap that text, except for Savings , in a span element with the class attribute set to description.

Following that, add three td elements with the following text (in order): $500, $650, $728. Give the third td element a class attribute set to current.
Step 16Passed
In your fourth tr element, add a th element with the text Total Assets. Wrap the text Assets in a span element with the class attribute set to sr-only.

Following that, add three td elements with the following text (in order): $579, $736, $809. Give the third td element a class attribute set to current.
Step 17
Time to move on to your second table. Start by giving it a caption element set to Liabilities. Then add your thead and tbody.
Step 18
Within your thead, add a tr. Inside that, add a td and three th elements.
Step 19
Give each th element a span element with the class set to sr-only and the following text, in order: 2019, 2020, and 2021.
Step 20
Within the tbody element, add four tr elements. Give the first three the class attribute set to data, and the fourth the class attribute set to total.
Step 21
Within the first tr, add a th element with the text Loans The outstanding balance on our startup loan.. Wrap that text, except for Loans , within a span element with the class set to description.

Add three td elements below that, and give them the following text, in order: $500, $250, and $0. Give the third td element a class set to current.
Step 22
Within the second tr, add a th element with the text Expenses Annual anticipated expenses, such as payroll.. Wrap that text, except for Expenses , within a span element with the class set to description.

Add three td elements below that, and give them the following text, in order: $200, $300, and $400. Give the third td element a class set to current.
Step 23
Within the third tr, add a th element with the text Credit The outstanding balance on our credit card.. Wrap that text, except for Credit , within a span element with the class set to description.

Add three td elements below that, and give them the following text, in order: $50, $50, and $75. Give the third td element a class set to current.
Step 24
In your fourth tr element, add a th element with the text Total Liabilities. Wrap the text Liabilities in a span element with the class attribute set to sr-only.

Following that, add three td elements with the following text (in order): $750, $600, $475. Give the third td element a class attribute set to current.
Step 25
For your third table, add a caption with the text Net Worth, and set up a table header and table body.
Step 26
Within your thead, create a tr element. In that, add a td and three th elements. Within each of the th elements, add a span element with the class set to sr-only and the following text, in order: 2019, 2020, and 2021.
Step 27
Within the tbody, add a tr with the class set to total. In that, add a th with the text Total Net Worth, and wrap Net Worth in a span with the class set to sr-only.

Then add three td elements, giving the third a class set to current, and giving each the following text: $-171, $136, $334.
Step 28
Time to style your table. Start by resetting the box model. Create an html selector and give it a box-sizing property set to border-box.
Step 29
Create a body selector and give it a font-family property set to sans-serif and a color set to #0a0a23.
Step 30
Before you get too far into your styling, you should make use of the sr-only class. You can use CSS to make elements with this class completely hidden from the visual page, but still be announced by screen readers.

The CSS you are about to write is a common set of properties used to ensure elements are completely hidden visually.

The span[class~="sr-only"] selector will select any span element whose class includes sr-only. Create that selector, and give it a border property set to 0.
Step 31
The CSS clip property is used to define the visible portions of an element. Set the span[class~="sr-only"] selector to have a clip property of rect(1px, 1px, 1px, 1px).

The clip-path property determines the shape the clip property should take. Set the clip-path property to the value of inset(50%), forming the clip-path into a rectangle within the element.
