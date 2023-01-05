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





