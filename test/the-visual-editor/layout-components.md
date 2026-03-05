# Layout Components Guide

This guide demonstrates several layout components available in the editor.
These components help structure content into interactive and visually organized sections.

***

# Accordion

Accordions allow you to **collapse and expand content sections**.
They are useful when you want to hide details until the learner chooses to view them.

**Best Uses**

* FAQs
* Explanations or hints
* Optional deep-dive material
* Breaking large content into sections

**Notes**

* Each accordion item must use `accordionContent`
* The `title` property defines the clickable header
* Content inside can contain **text, images, lists, or other components**

::::accordion{style="margin: 4px;"}
:::accordionContent{title="Accordion 1 Title"}
Accordion 1 Content Goes Here

You can include:

* Bullet lists
* Images
* Code snippets
* Other markdown
:::

:::accordionContent{title="Accordion 2 Title"}
Accordion 2 Content Goes Here

Accordions help keep pages **clean and readable** when there is a lot of optional information.
:::

:::accordionContent{title="Accordion 3 Title"}
Accordion 3 Content Goes Here

Try to keep titles short and descriptive.
:::
::::

***

# Grid

Grids allow you to create **multi-column layouts**.

This is useful for:

* Side-by-side comparisons
* Highlighting key ideas
* Displaying cards or summaries

**Notes**

* Each `grid` block becomes a column
* Columns automatically distribute space
* Styling such as `textAlign` can be applied

::::gridContainer{style="margin: 4px;"}
:::grid
### Column 1

Grid with multiple columns.

You can place:

* paragraphs
* lists
* images
* code
:::

:::grid{textAlign="center"}
### Column 2

This column is **center aligned**.

Useful for:

* diagrams
* figures
* key messages
:::

:::grid
### Column 3

Grid Content Goes Here.

Grids are great for **visual balance** in documentation.
:::
::::

***

# Stepper

Steppers guide the reader through a **sequence of steps**.

These are ideal for:

* Tutorials
* Procedures
* Walkthroughs
* Labs or exercises

**Notes**

* Steps appear in numbered order
* Each step uses `stepContent`
* Titles should describe the action

::::steps{style="margin: 4px;"}
:::stepContent{title="Step 1 — Setup"}
Prepare your environment and gather required tools.
:::

:::stepContent{title="Step 2 — Configure"}
Update configuration files and verify connectivity.
:::

:::stepContent{title="Step 3 — Run"}
Execute the process and validate results.
:::
::::

***

# Table

Tables help present **structured information** clearly.

Common use cases:

* comparisons
* feature lists
* configuration references

**Notes**

* Tables support standard HTML styling
* Keep cells concise for readability

<table class="rc5-table"><thead><tr><th style="background-color: transparent">Feature</th><th style="background-color: transparent">Description</th><th style="background-color: transparent">Example</th></tr></thead><tbody><tr><td style="background-color: transparent">Accordion</td><td style="background-color: transparent">Expandable content sections</td><td style="background-color: transparent">FAQs</td></tr><tr><td style="background-color: transparent">Grid</td><td style="background-color: transparent">Multi-column layout</td><td style="background-color: transparent">Comparisons</td></tr></tbody></table>

***

# Tabs

Tabs allow you to **switch between related sections without scrolling**.

They are great for:

* Showing variations of content
* Language examples
* Platform differences (Windows / Linux / Mac)

**Notes**

* Each tab must use `tabContent`
* Tabs should have concise titles
* Avoid placing extremely long content in tabs

::::::tabs{style="margin: 4px;"}
:::::tabContent{title="Overview"}
Tab 1 Content Goes Here

* Use this tab to display introductory information.
* You can also next objects within these constructs

::::gridContainer{style="margin: 4px;"}
:::grid
**A grid in tabs!**

<img alt="ChatGPT Image Mar 5, 2026, 09_30_59 AM" id="20260305094951-54bbce3c-bc39-4f17-a3e7-8a2b5db79e95" src="./Assets/Images/ChatGPT Image Mar 5, 2026, 09_30_59 AM.png" />
:::

:::grid{textAlign="center"}
**RangeOS - Is the best**

<img alt="RangeOS_Logo (1)" id="20260305095016-a2fdba26-d95c-4740-be81-7795b5d1c546" src="./Assets/Images/RangeOS_Logo (1).png" />
:::

:::grid{textAlign="center"}
***Another image***

<img width="225" height="327" alt="1" id="20260305095138-d8b4a48b-2a16-4c60-95e3-b30ecd897ec4" src="./Assets/Images/1.png" />
:::
::::
:::::

::::tabContent{title="Example"}
Tab 2 Content Goes Here

Examples help reinforce concepts.

:::tip{title="Tip" collapse="closed"}
These will help keep students engaged... hopefully
:::
::::

:::tabContent{title="Details"}
Tab 3 Content Goes Here

Additional technical details can be placed here.
:::
::::::

***

# Layout Tips

### Keep layouts purposeful

Only use advanced layouts when they improve clarity.

### Avoid overloading the page

Too many components can make pages feel cluttered.

### Combine layouts carefully

For example:

* Grid inside Tabs
* Accordion inside Steps

This can create **rich interactive learning content**.

***

# Summary

<table class="rc5-table"><thead><tr><th style="background-color: transparent">Layout</th><th style="background-color: transparent">Purpose</th><th style="background-color: transparent">Best Use</th></tr></thead><tbody><tr><td style="background-color: transparent">Accordion</td><td style="background-color: transparent">Collapsible sections</td><td style="background-color: transparent">FAQs, hints</td></tr><tr><td style="background-color: transparent">Grid</td><td style="background-color: transparent">Multi-column layout</td><td style="background-color: transparent">Comparisons</td></tr><tr><td style="background-color: transparent">Steps</td><td style="background-color: transparent">Ordered workflow</td><td style="background-color: transparent">Tutorials</td></tr><tr><td style="background-color: transparent">Table</td><td style="background-color: transparent">Structured data</td><td style="background-color: transparent">References</td></tr><tr><td style="background-color: transparent">Tabs</td><td style="background-color: transparent">Switchable views</td><td style="background-color: transparent">Examples, platforms</td></tr></tbody></table>

***