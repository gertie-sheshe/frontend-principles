# Frontend Engineering: Best Practices, Checklists, Guidelines, Principles etc

I have created this document - to serve as a central referencing place for principles, practices and information related to frontend engineering.

My motivation for creating this is to have a central place of a collection of what I need to keep my mind on when working on projects. My brain works well with such a format - if anything, that was my main incentive. I decided to open it up in case it helps anyone else. 

The information is generic and framework agnostic, meaning that it is applicable to a wide range of projects and not tied to any specific framework.
Enjoy!

Note: This is a living document and will continue to be edited. All relevant resources and sources are included.

## Table of Contents

 * [Accessibility and Inclusion](#accessibility-and-inclusion)
   * [Accessibility Guidelines](#accessibility-guidelines)
      * [Perceivable](#perceivable)
      * [Operable](#operable)
      * [Understandable](#understandable)
      * [Robust](#robust)
   * [Accessibility Checklist](#accessibility-checklist)
      * [The A11y Project Checklist](#accessibility-checklist)
   * [Accessible Form Design Patterns](#accessible-form-design-patterns)
   * [Inclusive Design Principles](#inclusive-design-principles)
      * [Provide Comparable Experience](#provide-comparable-experience)
      * [Consider the Situation](#consider-the-situation)
      * [Be Consistent](#be-consistent)
      * [Give Control](#give-control)
      * [Offer Choice](#offer-choice)
      * [Prioritize Content](#prioritize-content)
      * [Add Value](#add-value)
   * [Inclusive Components](#inclusive-components)
 * [Architecture](#architecture)
   * [Scalability](#scalability)
      * [Scaling for user growth](#user-growth)
      * [Scaling the application](#application)
   * [Performance](#performance)
      * [Optimize Loading Sequence](#optimize-loading-sequence)
      * [Load Third Party Scripts Efficiently](#third-party-scripts)
      * [Speed Up Javascript Execution](#javascript-execution)
      * [Optimize Images](#optimize-images)
      * [Font Best Practices](#font)
   * [Maintainability](#maintainability)
      * [Code Quality](#code-quality)
      * [Refactoring](#refactoring)
      * [Testing](#testing)
      * [Clean Craftsmanship](#clean-craftsmanship)
   * [Usability](#usability)
   * [Security](#security)
      * [Privacy Patterns](#privacy-patterns)
      * [Checklists](#checklists)
   * [Resilience](#resilience)
      * [Error Handling](#error-handling)
      * [Defensive Coding](#defensive-coding)
      * [Defensive CSS](#defensive-css)
      * [Constraints - Data, Device, Network](#data-device-network)
   * [Trade Offs](#trade-offs)
 * [HTML/CSS](#html-css)
   * [Semantics](#semantics)
   * [Page Layout and Structure](#page-layout)
 * [UI/UX](#ui-ux)
   * [UX Audit Questions](#ux-audit-questions)
      * [Blank State](#blank-state)
      * [Working State](#working-state)
      * [Error State](#error-state)
   * [UX Checklist](#ux-checklist)
      * [Content](#content)
      * [Labeling](#labeling)
      * [Presentation](#presentation)
      * [Navigation](#navigation)
      * [Interaction](#interaction)
      * [Feedback](#feedback)
      * [Visual Hierarchy](#visual-hierarchy)
      * [Forms](#forms)
  * [Testing](#general-testing)
    * [Testing for Accessibility](#accessibility-testing)
    * [Testing for Constratints](#constraints-testing)
    
 ## Accessibility and Inclusion
 ### Accessibility Guidelines
 W3C provides a list of guidelines that ensure the web is accessible to everyone. These guidelines fall into four principles:
 
#### Perceivable.
Information and user interface components must be presentable to users in ways they can perceive.
1. [Text Alternatives:](https://www.w3.org/TR/WCAG22/#text-alternatives) Provide text alternatives for all non text content.
2. [Time Based Media:](https://www.w3.org/TR/WCAG22/#time-based-media) Provide alternatives for time based media.
3. [Adaptable:](https://www.w3.org/TR/WCAG22/#adaptable) Create content that can be presented in different ways without losing information or structure.
4. [Distinguishable:](https://www.w3.org/TR/WCAG22/#distinguishable) Make it easy for users to see and hear content.

#### Operable
User Interface components and navigation must be operable.

5. [Keyboard Accessible:](https://www.w3.org/TR/WCAG22/#keyboard-accessible) Make all functionality accessible via a keyboard.
6. [Enough Time:](https://www.w3.org/TR/WCAG22/#enough-time) Provides users enough time to read and use content.
7. [Seizures and Physical Reactions:](https://www.w3.org/TR/WCAG22/#seizures-and-physical-reactions) Do not design content in a way that is known to cause seizures or physical reactions.
8. [Navigable:](https://www.w3.org/TR/WCAG22/#navigable) Provide ways to help users navigate, find content and determine where they are.
9. [Input Modalities:](https://www.w3.org/TR/WCAG22/#input-modalities) Make it easy for users to operate functionality through various inputs beyond the keyboard.

#### Understandable.
Information and operation of the user interface must be understandable.

10. [Readable:](https://www.w3.org/TR/WCAG22/#readable) Make text content readable and understandable.
11. [Predictable:](https://www.w3.org/TR/WCAG22/#predictable) Make web pages appear and operate in predictable ways.
12. [Input Avoidance:](https://www.w3.org/TR/WCAG22/#input-assistance) Help users avoid and correct mistakes.

#### Robust
Content must be robust enough that it can be interpreted by a wide variety of user agents, including assistive technologies.

13. [Compatible:](https://www.w3.org/TR/WCAG22/#compatible) Maximize compatibility with current and future user agents, including assistive technologies.

-------------------------

### Accessibility Checklist
#### The A11y Project Checklist
##### Audio
- Confirm Transcripts are available

##### Appearance
- Use a simple, straightforward and consistent layout.
- Increase text size to 200% - is it still readable? 
- Make sure color isn’t the only way information is conveyed. 
- Make sure instructions are not visual or audio-only.

##### Animation
- Ensure animations are subtle and do not flash too much.
- Provide a mechanism to pause background video.

##### Content
- Use plain language and avoid figures of speech, idioms and complicated metaphors.
- Make sure that button, link and label texts/content are unique and descriptive.
- Use left-aligned text for left-to-right (LTR) languages, and right-aligned text for right-to-left (RTL) languages.

##### Color Contrast
- Check the contrast for all texts and icons.
- Check the contrasts of borders for input elements (checkboxes, radio buttons, text inputs etc)
- Check text that overlaps images or video.

##### Controls
- Use the <a/> element for links and <button/> for buttons.
- Ensure that links are recognizable as links.
- Identify links that open in a new tab/window.
- Provide a skip link and make sure that it is visible when focused.

##### Forms
- All inputs in a form are associated with a corresponding label element.
- Associate input error messaging with the input it corresponds to.
- Make sure that error, warning and success states are not visually communicated by just color.
- Use fieldset and legend elements where appropriate.

##### Headings
- Use heading elements to introduce content.
- Use only one h1 element per page or per view.
- Heading elements should be written in a logical sequence.
- Don’t skip heading levels.

##### Images
- Make sure that all img elements have an alt attribute.
- Make sure that decorative images have a null alt attribute.
- Provide a text alternative for complex images such as charts, graphs and maps.

##### Keyboard
- Make sure there is a visible focus style for interactive elements that are navigated to via keyboard input.
- Check to see that keyboard focus order matches the visual layout.
- Remove invisible focusable elements

##### Lists
- Use list elements (`ul`, `li` and `dl`) for list content

##### Media
- Make sure that media does not autoplay.
- Ensure that media controls use appropriate markup.
- Check to see that all media can be paused.

##### Mobile and Touch
- Remove horizontal scrolling.
- Check that the site can be rotated to any orientation.
- Ensure that button and link elements can be activated with ease.
- Ensure sufficient space between interactive items in order to provide a scroll area.

##### Tables
- Use the `table` element to describe tabular data.
- Use the `th` element for table headers (with appropriate scope attributes)
- Use the `caption` element to provide a title for the table.

##### Video
- Confirm the presence of captions.
- Remove seizure triggers.

#### Resources
- Checklist: https://www.a11yproject.com/checklist/
- WCAG 2.2 Guidelines: https://www.w3.org/TR/WCAG22

-------------------------

### Accessible Form Design Patterns
Currently reading the book [Form Design Patterns](https://formdesignpatterns.com/) by Adam Silver and populating my learnings here.

### Inclusive Design Principles
#### Provide Comparable Experience
Interfaces should offer a similar experience for everyone so that people can complete tasks in a way that meets their needs without compromising the quality of the content.

- Provide alternative e.g alt text, transcript, audio description, sign language, synchronized closed captions, screen reader notification

#### 1. Consider the Situation
Interfaces should provide a positive experience for users in any situation they may encounter it in.
- Color contrast. Context sensitive help. Captions on the go.

#### 2. Be Consistent
Use familiar conventions and apply them consistently.
- Consistent page architecture. Consistent buttons and controls.

#### 3. Give Control
Interfaces allow users to have control over their experience, including ability to interact with content in their preferred manner.
- Allow zoom. Scrolling control (bad for keyboard navigation). Option to stop animation.


#### 4. Offer Choice
Offer various options for users to complete tasks, particularly complex and non standard ones.
- Alternative data presentation (i.e infographics). Alternative list content view e.g grid vs list layout.

#### 5. Prioritize Content
Organize layout and content in a way that prioritizes core tasks, features and information. Help users to focus on the most important elements.

#### 6. Add Value
Evaluate feature usefulness and how they enhance user experience for various individuals.

##### Resources:
- https://inclusivedesignprinciples.org/

-------------------------

### Inclusive Components

Currently reading the book [Inclusive Components](http://book.inclusive-components.design/) by Hayden and will populate my learnings here.

#### Toggle Buttons
Examples: on/off, play/pause, active/inactive

##### Checklist
- Use checkboxes or radio buttons as on/off toggle switches, as long as you are confident that the user will not mistake them for input fields for submitting data.

- Use button elements, not links, with aria-pressed or aria-checked attributes.

- Don’t change label and state together.

- You can use aria-labelledby to provide unique labels for visual "on" and "off" text (or similar) when necessary. 

- Ensure that the contrast between the button's text and background color meets WCAG 2.0 standards


## Architecture
### Scalability
Two areas to focus on with scalability:
- Scaling for user growth.
- Scaling the application.

#### Scaling for user growth

1. **Optimize Performane (Visit the [Performance](#performance) section for more)**
This can include:
- CDN: Use a Content Delivery Network to deliver your static assets. Helps reduce load on your servers and improves application speed.
- Caching: Reduces the number of requests that need to be made to the server.
- Rendering: Optimize your applications rendering. Depending on your application, consider Server Side Rendering (SSR) to improve initial load time.
- Requests: Reducing the number of network requests being made.

2. **Monitoring and Logging**

Provides insights into performance and behavior of your application. 

Monitoring and logging help in identifying bottlenecks, detecting and diagnosing errors, monitoring resource usage.

3. **Resilience (Check the [Resilience](#resilience) section for more)**

A resilient frontend can help ensure a functioning app in the event of failures that may be caused due to increase in traffic. 

-------------------------

#### Scaling the application

1. **Modular Design**

Smaller, independent and self-contained modules can be developed and maintained independently. Makes it easier to add new features and make changes.

2. **Testing**

Testing helps to ensure your application is stable and reliable. There is more confidence to refactor with solid tests in place.

3. **Code Quality**

High quality code is generally easier to understand, maintain and modify. 

-------------------------


### Performance
#### 1. Optimize your loading sequence
- Prioritize loading of above the fold content.

- Defer the loading on non-critical resources.

- Load third party scripts (ads, social sharing buttons, analytics & metrics, widgets, trackers, video player embeds, helper libraries etc ) efficiently.

- Understand Key Metrics i.e First Input Delay (FID), First Contentful Paint (FCP), Cumulative Layout Shift (CLS), Largest Contentful Paint (LCP) etc what resources are needed for each and their optimal order e.g
  - **Time To First Byte (TTFB)** and **First Contentful Paint (FCP)** help diagnose **Largest Contentful Paint (LCP)** issues.
  
  - **Total Blocking Time (TBT)** and **Time To Interactive (TTI)** help diagnose **First Input Delay (FID)** issues.
  
  - Time To First Byte (TTFB) precedes First Contentful Paint (FCP) and Largest Contentful Paint (LCP).
  
  - **First Contentful Paint (FCP)** precedes **Largest Contentful Paint (LCP)**.
  
  - **First Contentful Paint (FCP)** and **Time To Interactive (TTI)** impact **First Input Delay (FID)**.
  
- Optimize size and number of resources.

- Understand when resources recommendations can become a constraint i.e fallback fonts improve FCP but if they cause jumping fonts it affects CLS

- Server Side Rendering (SSR) - considering trade offs.

- [Web Vitals Patterns](https://web.dev/patterns/web-vitals-patterns/) (UX Patterns optimized for Core Web Vitals)

-------------------------

#### 2. Loading Third Party Javascript Efficiently
a. **Use async or defer.** 

Applicable to: non-critical scripts.
- Use async if it’s important to have the script run earlier in the loading process i.e analytics. 
- Use defer for less critical resources i.e below the fold video player.

b. **Establish early connections to required origins using resource hints.**

Applicable to: Critical scripts, fonts, CSS, images from third party CDNs.
Initiates connections early in the life cycle.
- Dns-prefetch performs DNS lookup early, reducing latency.
- Preconnect performs TCP round trips and handles TLS negotiations.

c. **Self-host third party scripts.**

Applicable to: Javascript files, fonts

Reduce DNS or round-trip times. Improve HTTP caching headers.

Caveats:
- Scripts can go out of date.
- Scripts won’t get automatic updates due to API change.

d. **Lazy Load Below The Fold Third Party Resources.**

Applicable to: Embeds such as YouTube, Maps, Advertisements and Social Media.
Example: Serving an ad in the footer only when a user scrolls down the page.

- Use service workers to cache scripts where possible.

e. **Follow the ideal loading sequence.**

-------------------------

#### 3. Speed up Javascript Execution

#### 4. Optimize Images

#### 5. Fonts Best Practices

## UI/UX
### UX Audit
#### Blank State

What the user sees when they first login/launch the application.

Questions to strive to provide a solid answer to:
- What is this?
- Does it look credible?
- Does it look valuable?

#### Working State

What the users interact with during the normal course of use.

Questions to ask on different levels:
1. **Predictability**
- Are all icons used commonly and universally understood?
- Are calls to action explicit and clear?
- Do things that look the same, act the same?
- Are interactive elements presented to look like they are interactive?

2. **Consistency**
- Are buttons and controls placed consistently throughout the application?
- Does the UI respond to user actions consistently?
- Are fonts, images, graphics + color schemes the same at every interaction point?

3. **Progression**
- Only necessary or requested information is shown at any given time.
- Do interaction sequences progress naturally from simple to complex?
- Does the initial screen display only the core features needed first?
- Is the default level of content and interactivity simple?
- Are nav menus and toolbars relevant to the task at hand?

4. **Natural Constraints**
- The system + its UI should be designed to minimize potential user errors.
- Are rules and instructions obvious? Do users know what to do?
- Are actions simple or complex? Are instructions needed? If yes, one upfront step by step.
- Are things users should not do removed from the screen?
- Do constraints guide users to the next appropriate action?

5. **Visibility, Hierarchy + Visual Clarity**
- Are functions that are functionally/logically related grouped together visually?
- Is the information presented in the order of importance to the user? Does visual hierarchy reflect where they need to go first/next?
- Is the color scheme used consistently across the application?
- Is color use functional?(good) or merely decorative?(bad) Does the functionality of this app rely on color? How does that affect colorblind users?
- Are the fonts used easy to read on various screen sizes?

6. **Flexibility**
- Does the UI support both novices and experts?
- Does the flow of information between screens match the flow of work the user is trying to accomplish?
- Is the means of navigation appropriate for all the apps intended users?
- Is the directional flow + visual hierarchy of info familiar to users?
- Are there multiple means  of navigation? And if there aren’t, should there be?

7. **Feedback**
- Is warning feedback given when actions are incorrect, likely to cause an error or when a user’s action is potentially destructive?
- Does confirmation feedback appear when data has been changed, saved or sent successfully/unsuccessfully?
- Are feedback messages written in plain language that precisely indicates the problem/solution?
- Is feedback provided when users have to wait for a process? Is time and progress shown?
- Is the length of time between user action + on screen feedback short? (less than 0.1 seconds)


#### Error State

What users see when something goes wrong.

- Are error messages clearly visible and impossible to miss?
- Do error messages clearly communicate what’s happening + describe how the user can fix it?
- Is the error message specific as to what action or piece of info causes the error?
- If there are rules, constraints or limitations on data entry, are they clearly exposed + explained?
- Does the app, site or system reduce the work of correcting that error?

#### Credit for the above: https://learn.givegoodux.com/p/simple-way-to-conduct-ux-audit

-------------------------

### UX Checklists
#### 1. Content
a. Text Content
- Language is plain, simple and clear.
- Content is written with common language that users easily understand.
- Terms, language and tone used are consistent throughout the site.
- Language, terminology and tone used is understood by the target audience.
- Content is useful and up-to-date.
- Titles and Headings clearly describe the content of the page.
- Headings precede related paragraphs.
- Links in text are contextually related to what the user is currently doing or reading.
- Lists are used for related sub-points or sub-navigation links.
- All sentences, paragraphs, titles and headlines are left-aligned.
- Content is scannable — short paragraphs, descriptive headings, lists and images.
- There is adequate contrast between the text content and background.
- Visual content (e.g. infographic, chart) is used to illustrate complex concepts.
- Separate ideas are kept in separate sentences and paragraphs.
- Full words are used instead of cryptic abbreviations.
- Uppercase words are used only for labels or acronyms.
- Acronyms (e.g. UX) are used sparingly.

b. Non Text Content
- Alt-text exists for all non-text material.
- All multimedia content has an alternative (e.g. text content).
- Icons are real-world metaphors if possible (e.g. credit card symbols at checkout).
- Audio or video doesn’t start automatically, unless the user expects it.
- Users can control the speed of presentation (Start, Pause, etc.).

#### 2. Labeling
a. General Labels
- Label terms are familiar to the intended user and are not system-oriented terms.
- Labeling describes value when possible (e.g. “Free Trial” vs. “Register”).
- Language is consistent across label types (e.g. verb/noun, tense, tone, word count).
- Full words are used instead of cryptic abbreviations.
- Labels are visually distinct from content and/or data.

b. Page Title
- Each page title exactly matches the wording of the related navigation menu link.
- Each page title exactly matches the wording of the related breadcrumb link.
- Each page title gives the user a clear idea of the page’s content and purpose.

c. Breadcrumbs
- Breadcrumb paths match established navigation paths.
- Every breadcrumb has a counterpart in a navigation menu.
- The full navigation path is shown in the breadcrumb (e.g. “Home > Services > Annual
Reports > File an Annual Report” instead of “Home > File an Annual Report”).

d. Form and Table Labels
- Table and Form labels have less color and contrast than the content they describe
- Each form and table label is in close proximity to the item it describes.

e. Tooltip Labels(icons)
- Tooltip icons are universally recognizable (e.g. “?”).
- Tooltip icons are visually distinct from content and/or data.
- Tooltip icons have less color and contrast than the content they describe.

#### 3. Presentation
a. General
- Most common devices, browsers and screen resolutions are supported.
- There is no horizontal scrolling on any device, browser or screen resolution.
- Page layouts are consistent across the whole website.
- The order of information matches user expectations.
- Modal or pop-up windows are used only when strict focus is necessary for the user.
- There is no distracting blinking, flashing, or animation.
- Users can control layout and text size via the browser.
- Users are adequately supported according to their level of expertise (e.g. shortcuts to forms for expert users, wizards for novice users).
- Visual styles are consistent throughout the application or site.
- Frequently used tasks are readily available and well supported (e.g. shortcuts).
- Visual metaphors used will be understood by both casual and expert users.

#### 4. Navigation
a. General
- Navigation, page titling and breadcrumbs tell the user where she is, how she got here and where she can go.
- The current location is clearly indicated (e.g. breadcrumb, highlighted menu item).
- Navigation location and styling is consistent on every page.
- Navigation menus are persistent (on every screen) and consistent (items don’t disappear/reappear).
- Navigation labels are clear and obvious, readily understood by the target audience.
- Navigation structure addresses common user goals.
- Site uses friendly URLs that are descriptive and understandable.

b. Search
- Search is available on every page, not just the homepage.
- Search box is wide enough so that users can see what they’ve typed.
- Search is always the form itself, not a link to a form.
- Search results are relevant, comprehensive, precise, and well displayed.
- Search results do not return broken links.

c. Workflow
- All primary onscreen content is related to the user’s current task.
- The flow of content matches the flow of the work the user is trying to accomplish.
- Workflows with multiple steps include an overview of those steps.
- Workflows with multiple steps include a persistent progress indicator.
- Similar operations and tasks are presented and performed in similar ways.

#### 5. Interaction
a. General
- Calls to action (e.g. Register, Add, Submit) are clearly labeled and appear clickable.
- Users have control over interactive content, experiences or workflows.
- The UI (and all buttons or controls) responds consistently to user actions in terms of visual display, appropriate context and data functionality.
- Frequently used features are readily available.
- Standard browser functions (e.g. Back, Forward, Copy, Paste) are supported.

b. Controls
- Buttons or other controls are placed consistently in every screen/page.
- Interactive elements are not abstracted (e.g. buttons clearly look like buttons).
- Primary, secondary and tertiary controls are visually distinct from one another.

c. Links
- There are no broken links.
- Link text is descriptive; there are no “click here” links.
- Text links are visually distinct from other text content.
- Important links aren’t placed in moving or animated features e.g rotating carousels
