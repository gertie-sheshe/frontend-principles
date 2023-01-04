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
