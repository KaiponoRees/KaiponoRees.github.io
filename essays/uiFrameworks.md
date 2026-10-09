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

When starting with UI frameworks, I felt pretty good doing the exercise from FreeCodeCamp, but as I started on other assignments during this course, I felt like more problems were showing up more frequently. When I first started using Bootstrap 5, I thought it would help make building websites faster and easier for me because of the new shortcuts you could do with it. But I instead had to learn a lot of different class names, understand Bootstrap’s new layout system, and troubleshoot why some of my CSS code stopped working. When learning Bootstrap, it felt similar to learning a whole new programming language with how many different things I had to learn, like what works and what doesn't. However, after using Bootstrap to redesign web pages, I began to understand the importance of UI frameworks because you can actively see the changes to your website as you code, which is a feature I really enjoyed. I learned during this course that Bootstrap does not replace HTML or CSS, but it provides tools that are helpful for future developers to use to create organized, polished, and responsive websites without having to build every component from the beginning.

## My First Experience With Bootstrap 5

My first experiences with Bootstrap involved rebuilding websites such as our first assignment, where we had to build a browser-history page and 5 different Navbars. Before we got started with Bootstrap, I first used regular HTML elements and wrote my own CSS rules to control their appearance, spacing, colors, and position on the page. This gave me more control over the design of the page, but it also meant that I had to create the layout from scratch. As the pages became more complex, my CSS became longer and more difficult to organize, like when I needed to create columns, navigation bars, or responsive buttons as well. For example, when I was doing it on FreeCodeCamp, I used properties such as flex, float, width, and margin to position content.

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

One of Bootstrap’s pros is that it has a large collection of utility classes, but that is also one of the reasons why if was so confusing for me at first. Classes such as mt-5, pt-5, px-0, float-start, and justify-content-end are very helpful once I started understanding their meanings and how they translated to the website. At first, they looked like random abbreviations, so it was confusing for me to figure out what each of them did. For example, mt-5 adds margin to the top of an element, while pt-5 adds padding to the top. The class px-0 removes horizontal padding, and justify-content-end moves content toward the end of a flex container like a Navbar or footer. Learning the distinction of these patterns made Bootstrap way easier for me to use for assignments, but I had to go back to resources for this course to check what they did while I was coding.

I also experienced times where Bootstrap changed the appearance of elements that I had already styled in my CSS. This happened because Bootstrap comes with its own style rules, so I quickly learned that the order of the stylesheet links matters. Placing my stylesheet after Bootstrap allows my custom rules to override Bootstrap when both styles have equal parameters:

```html
  <link href="bootstrap.min.css" rel="stylesheet">
  <link href="style.css" rel="stylesheet">
```

This taught me that frameworks do not remove the need to understand CSS and that I still have to understand specificity, inheritance, margins, padding, and other CSS concepts to use Bootstrap and CSS both successfully.

## Using Both HTML and CSS

HTML and CSS code do provide complete control over a website and the contents that you add to the website. For a small page, writing custom CSS is easier than learning Bootstrap or a whole framework. A simple personal profile, article, or restaurant menu may not need Bootstrap at all. The challenges I faced during this course were when I had to create a larger website like IslandSnow or create a whole website through Bootstrap 5. Something I faced when doing this was repeatedly creating the same buttons, navigation bars, columns, forms, dropdowns, and spacing rules. Which caused my websites to look very cluttered and completely wrong when compared to how it actually supposed to look. I also need to ensure that these components work on different screen sizes, like when a user condenses the website. Coding and testing all these styles manually takes a lot of time when you're trying to finish an assignment. But Bootstrap helps provide reusable solutions for many of these common problems that I was facing before. For example, its navbar component already includes classes for alignment, colors, expansion, and behavior. Its dropdown component provides the necessary structure for a working menu with different places it takes you when your using a website. Instead of creating everything from the beginning, I was able to start with a tested component and customize it to better fit how I wanted my final website to turn out.

During the IslandSnow assignment, I used Bootstrap Icons and a dropdown to create a top navigation bar containing social-media links, account controls, and a shopping cart:

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
Creating this feature with only HTML and CSS would require way more coding, styling, and custom scripts depending on how complex it is. Bootstrap supplied most of the behavior, parameters, and rules, which allowed me to focus on the page’s content and overall design.

## Software Engineering Benefits

UI frameworks also provide software engineering benefits beyond just appearance it also helps you be consistent when coding. When you can use the same button, navbar, grid, and spacing classes, the website follows a shared visual system which makes it easier to replicate or create your own websites. This becomes especially valuable when multiple people work on the same project because without a framework, one developer might create a button using padding and margins that are completely different from another developer’s button. This is why Bootstrap is so useful: it gives a team a common vocabulary and coding language to follow when coding together. If someone uses btn btn-dark, another developer can quickly understand the component’s basic appearance and purpose, which can allow them to add more or change it depending on how the group wants it to look.

Frameworks also reduce the use of repeated code because instead of creating a new CSS rule for every element, developers can reuse existing classes to make it easier to classify. This makes the project easier to update because fewer custom rules need to be maintained or followed. Bootstrap’s documentation and resources are another advantage of this framework. A new group member joining a project that has work done to it can look up a component and understand how it is expected to work with its documentation. I also made the distinction that a developer does not have to reverse-engineer every style created by the original team. But Bootstrap does have flaws, like it can make HTML files more crowded with class names, making it harder for a developer to find what they want to fix, but a quick solution to this is just commenting on your code for the different sections. Another flaw is that someone may depend too heavily on the framework, which can cause the user to create websites that look similar to every other Bootstrap site. A framework is most useful when developers can understand it as a blueprint rather than a replacement for how they make design decisions.

## Finding the Right Balance

In my opinion, I don't think that Bootstrap should be used to create every website. Also, if a page is very small or requires a unique design, custom HTML and CSS may be the better choice. A framework introduces extra files, conventions, and styles that may not be necessary for a simple project. However, for websites containing repeated components, responsive layouts, or multiple developers, Bootstrap becomes a much more valuable tool. Although the initial learning process was frustrating at first, the time I spent learning this framework helped me save time on other assignments during this course. I believe the best approach is to combine Bootstrap with custom CSS. Bootstrap can manage the grid, navigation bar, spacing, buttons, and responsive behavior. Custom CSS can then provide the colors, fonts, and other details that give the website its own identity and help you make it your own.

## Conclusion

My experience with Bootstrap 5 was both frustrating and valuable. At first, the class names and component structures felt like extra rules that made HTML more complicated. I often questioned if writing regular CSS would be faster. Even so, as I continued using Bootstrap, its organization and structure started to make more sense to me. Classes such as container, row, col, float-start, and justify-content-end allowed me to create layouts with less custom CSS while also making it easier for me to change. Building the browser-history columns and IslandSnow navigation bar showed me how the reusable components of Bootstrap can greatly speed up the work spent on my code. UI frameworks require me to put in some time, but they provide consistency, responsive design, reusable components, and less repeated code in return. Bootstrap doesn't just eliminate the need to learn and understand HTML and CSS, which is why I think I enjoyed it better. Understanding these coding languages makes Bootstrap easier to use and implement. I would not say that Bootstrap makes website development easy; instead, it makes web-development problems more manageable by giving developers reusable tools that can be applied across future projects. Although Bootstrap was difficult to understand at first, the effort I invested in understanding it will help me complete future assignments in this class and build my own functioning websites outside this class.

## Own Choice Assignment Submission

<img width="1200px" class="rounded float-start pe-4" src="../img/ownchoice-HookedUpHawaii.png">

## AI Use
I used Grammarly to review my spelling, formatting, grammar, and sentence structure to ensure that my essay was cohesive, organized, and easy to read. It also helped me identify spelling errors and improve the flow between my ideas while still having my own voice in my writing style.
