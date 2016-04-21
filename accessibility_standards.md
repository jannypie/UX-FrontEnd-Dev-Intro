- Visual Impairment
    - Low vision
    - Colorblindness
    - Dyslexia

Use these tools https://www.w3.org/WAI/ER/tools/

Use the accessibility audit dev tools



https://css-tricks.com/accessibility-basics-testing-your-page-for-color-blindness/


http://www.ssbbartgroup.com/blog/how-not-to-misuse-aria-states-properties-and-roles/

Generally ARIA should not be added to HTML content that already has the desired implied semantics. More importantly, ARIA markup should never be added that conflicts with the strong native semantics between HTML and ARIA. Refer to the default implied HTML semantics and strong native semantics found in the vocabulary and associated APIs for HTML and XHTML document for additional information. 

aria-haspopup

This attribute seems useful for indicating controls such as dialogs and rollover content, however, the ARIA specification indicates it is only to be used for indicating popup menus or sub-level menus even though it can be used with elements of any role. In fact some screen readers will announce “has menu” instead of “haspopup” enforcing the idea that this state should be used with menus.
