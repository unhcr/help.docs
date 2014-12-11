# Javascripts

There are not too many javascript files in the project, but some of the logic is a bit script-monkey-esque.

`js/help.js`

This file initializes all the accordions on the page and most other event based javascript.

`js/changeLandingLanguage.js`

This is probably the craziest js file of the bunch but currently works. It's responsbille for changing the language of the landing page without refreshing the whole page when someone changes the language. It does this by ajax requesting the changed language, parsing that document with jquery and updating the appropriate strings.

`js/languages.js`

This handles the rendering of dropdowns when a user changes countries or languages on the landing page.

`js/map/js`

Handles changing and initializing the map on the `contacts.php` page template
