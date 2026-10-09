---
layout: essay
type: essay
title: "Bootstrap 5: Rough Start, Strong Finish"
# All dates must be YYYY-MM-DD format!
date: 2026-10-08
published: true
labels:
  - Software Engineering
  - HTML
  - CSS
  - Bootstrap 5
  - UI Frameworks
---

UI frameworks can seem like they create as many problems as they solve. When I first started using Bootstrap 5, I expected it to make building websites faster and easier. Instead, I had to learn a large number of class names, understand Bootstrap’s layout system, and figure out why some of my CSS was no longer working. At times, learning Bootstrap felt similar to learning a new programming language.

However, after using Bootstrap to redesign web pages, I began to understand why developers invest time in UI frameworks. Bootstrap does not replace HTML or CSS. Instead, it provides reusable tools that help developers create organized, consistent, and responsive websites without building every component from the beginning.

## My First Experience With Bootstrap 5

My first experiences with Bootstrap involved rebuilding websites such as a browser-history page and the Island Snow website. Before Bootstrap, I used regular HTML elements and wrote CSS rules to control their appearance. For example, I used properties such as display: flex, float, width, and margin to position content.

When I converted the browser-history page to Bootstrap, I had to replace some of my custom layout classes with Bootstrap classes. To place the three browser descriptions into columns, I used Bootstrap’s grid system:

```html
<div class="row">
  <section class="col">Internet Explorer content</section>
  <section class="col">Firefox content</section>
  <section class="col">Chrome content</section>
</div>
```

The row class creates a horizontal row, while each col class creates an equal-width column inside it. The result only required a few classes, but understanding why they worked took time. 

I also used Bootstrap’s float-start class to place each browser logo beside its description:

```html
<img class="float-start" src="firefox-logo.png" alt="Firefox logo" width="100">
```

## When Convenient Classes Become Confusing

One of Bootstrap’s strengths is its large collection of utility classes, but that was also one of the most confusing parts for me. Classes such as mt-5, pt-5, px-0, float-start, and justify-content-end are convenient once their meanings are understood. At first, however, they can look like random abbreviations.

For example, mt-5 adds margin to the top of an element, while pt-5 adds padding to the top. The class px-0 removes horizontal padding, and justify-content-end moves content toward the end of a flex container. Learning these patterns eventually made Bootstrap easier to use, but I often had to check the documentation while working.

I also experienced situations where Bootstrap changed the appearance of elements that I had already styled in my CSS. This happened because Bootstrap comes with its own style rules. I learned that the order of the stylesheet links matters. Placing my stylesheet after Bootstrap allows my custom rules to override Bootstrap when both styles have equal specificity:

```html
  <link href="bootstrap.min.css" rel="stylesheet">
  <link href="style.css" rel="stylesheet">
```

This taught me that frameworks do not remove the need to understand CSS. A developer still needs to understand the cascade, specificity, inheritance, margins, padding, and other CSS concepts to use Bootstrap successfully.

## Using Both HTML and CSS

Raw HTML and CSS provide complete control over a website. For a small page, writing custom CSS may be easier than learning an entire framework. A simple personal profile, article, or restaurant menu may not need Bootstrap at all. The challenge appears when a website becomes larger. Developers may repeatedly create the same buttons, navigation bars, columns, forms, dropdowns, and spacing rules. They also need to ensure that these components work on different screen sizes. Writing and testing all these styles manually takes time. Bootstrap provides reusable solutions for many of these common problems. For example, its navbar component already includes classes for alignment, colors, expansion, and responsive behavior. Its dropdown component provides the necessary structure for a working menu. Instead of creating everything from the beginning, developers can start with a tested component and customize it.

During the Island Snow assignment, I used Bootstrap Icons and a dropdown to create a top navigation bar containing social-media links, account controls, and a shopping cart:

```html
<li class="nav-item dropdown p-1">
  <a
    class="nav-link dropdown-toggle"
    href="#"
    data-bs-toggle="dropdown"
  >
    <i class="bi bi-cart"></i>
    My Cart
  </a>

  <ul class="dropdown-menu">
    <li>
      <span class="dropdown-item-text">
        Your cart is currently empty.
      </span>
    </li>
  </ul>
</li>
```
Creating this feature with only HTML and CSS would require more styling and possibly custom JavaScript. Bootstrap supplied most of the behavior, allowing me to focus on the page’s content and overall design.

## Software Engineering Benefits

UI frameworks also provide software engineering benefits beyond appearance. One of the most important benefits is consistency. When developers use the same button, navbar, grid, and spacing classes, the website follows a shared visual system. This becomes especially valuable when several developers work on the same project. Without a framework, one developer might create a button using padding and margins that are completely different from another developer’s button. Bootstrap gives the team a common vocabulary. If someone uses btn btn-dark, another developer can quickly understand the component’s basic appearance and purpose.

Frameworks also reduce repeated code. Instead of creating a new CSS rule for every element, developers can reuse existing classes. This makes the project easier to update because fewer custom rules need to be maintained. Bootstrap’s documentation is another advantage. A new developer joining a project can look up a component and understand how it is expected to work. The developer does not have to reverse-engineer every style created by the original team. However, Bootstrap can also make HTML crowded with class names. Developers may depend too heavily on the framework or create websites that look similar to every other Bootstrap site. A framework is most useful when developers understand it as a foundation rather than a replacement for design decisions.

## Finding the Right Balance

I do not believe Bootstrap should be used for every website. If a page is very small or requires a unique design, custom HTML and CSS may be the better choice. A framework introduces extra files, conventions, and styles that may not be necessary for a simple project. For websites containing repeated components, responsive layouts, or multiple developers, Bootstrap becomes much more valuable. The initial learning process can be frustrating, but the time spent learning it can save time on later projects. The best approach is often to combine Bootstrap with custom CSS. Bootstrap can manage the grid, navigation bar, spacing, buttons, and responsive behavior. Custom CSS can then provide the colors, fonts, and other details that give the website its own identity.

## Conclusion

My experience with Bootstrap 5 has been both frustrating and useful. At first, the class names and component structures felt like extra rules that made HTML more complicated. I sometimes wondered whether writing regular CSS would be faster. As I continued using Bootstrap, its organization started to make more sense. Classes such as container, row, col, float-start, and justify-content-end allowed me to create layouts with less custom CSS. Building the browser-history columns and Island Snow navigation bar showed me how reusable components can speed up development. UI frameworks require an investment of time, but they provide consistency, responsive design, reusable components, team-wide conventions, and less repeated code in return. Bootstrap does not eliminate the need to learn HTML and CSS. In fact, understanding those technologies makes Bootstrap easier to use correctly. I would not say that Bootstrap makes web development simple. Instead, it makes common web-development problems more manageable. The frustration comes from learning the framework, but the benefit comes when the same knowledge can be reused across many future projects.
