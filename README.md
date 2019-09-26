# atomic-design

# 'src/components'

This folder will contain all components that would be used in our application.
Its majorly divided into 5 parts:-

- atoms (HTML elements)
- molecules (Group of HTML elements)
- organisms (Group of molecules and/or HTML elements)
- templates (Group of organisms and Molecules without any props or Data)
- pages (Templates with Data)

- Atoms are UI elements that can’t be broken down any further and serve as the elemental building blocks of an interface.
- Molecules are collections of atoms that form relatively simple UI components.
- Organisms are relatively complex components that form discrete sections of an interface.
- Templates place components within a layout and demonstrate the design’s underlying content structure.
- Pages apply real content to templates and articulate variations to demonstrate the final UI and test the resilience of the design system.

Read the full book [Atomic Design by Brad Frost](http://atomicdesign.bradfrost.com/).
Example of Atomic Design:- http://atomicdesign.bradfrost.com/images/content/instagram-atomic.png
[Click here](https://miro.medium.com/max/1331/0*BBNnpHeIAAfmVcX_.gif) to get a quick peek into Atomic Design.
Templates are page-level objects that place components into a layout and articulate the design’s underlying content structure.


# 'src/components/atoms'

> Should Ideally be an empty folder.

These atoms include [basic HTML elements](https://developer.mozilla.org/en-US/docs/Web/HTML/Element) like form labels, inputs, buttons, and others that can’t be broken down any further without ceasing to be functional.
Ideally this folder should contain nothing, as HTML elements are **the** unbreakable building blocks upon which all Higher order components are built upon.
In fact there is a [Periodic table mentioning basic HTML elements](http://atomicdesign.bradfrost.com/images/content/html-periodic-table.png).
For more details [Click here](http://atomicdesign.bradfrost.com/chapter-2/#atoms)


# 'src/components/molecules'

> Molecules are combination of atoms & molecules only.
> Molecules are simply combinations of basic HTML elements and other molecules.
> Try not to have stateful components as molecules, or limit it to <2 states.

The molecules are relatively simple groups of UI elements functioning together as a unit. For example, a form label, search input, and button can join together to create a [search form molecule](http://atomicdesign.bradfrost.com/images/content/molecule-search-form.png).

Creating molecules helps UI designers and developers to adhere to _Single responsibility Principle_.

**The result is a simple, portable, reusable component that can be dropped in anywhere**

For more details [Click here](http://atomicdesign.bradfrost.com/chapter-2/#molecules)

# 'src/components/organisms'

> Organisms are relatively complex UI components composed of groups of molecules and/or atoms and/or other organisms.
> **These organisms form distinct sections of an interface.**

For Example : The [header](http://atomicdesign.bradfrost.com/images/content/organism-header.png) forms a standalone section of an interface, even though it contains several smaller pieces of interface with their own unique properties and functionality.

An Organism can have same molecule repeated over and over again (Example)[http://atomicdesign.bradfrost.com/images/content/organisms-product-grid.png].

Difference between molecules and organisms:

- Molecules are relatively simple
  Organisms are complex.

- Molecules .
  Organism forms a standalone section of an interface.

- General rule of thumb is that if you break a component down and get

  - basic _tags_ (such as an image, heading, paragraph, button, etc), it’s a molecule.
  - smaller _components_ (social share lists, cards, media object, etc) it’s an organism.

- Molecules are more like _helpers_  
  Organisms are more like _standalone Components_

[**Standalone**](https://ugc-about.futurelearn.com/wp-content/uploads/04_small.jpg) - The “standalone” elements can “survive” on their own – they can be viewed as their own self-contained units of content and functionality. e.g- Jumbotron Container, Call to action Container, Header Section, Footer Section
[**helper**](https://ugc-about.futurelearn.com/wp-content/uploads/03_small.jpg) - Helpers don’t make sense on their own. e.g. - Card Description, Like and comments section, Share section.

To have a clearer picture on what the difference is [Click Here](https://about.futurelearn.com/blog/atomic-design-molecules-organisms)

For more details [Click here](http://atomicdesign.bradfrost.com/chapter-2/#organisms)


# 'src/components/templates'

> Templates don't have any Data
> Basically a Page skeleton

Templates are page-level objects that place components into a layout and articulate the design’s underlying content structure.
Template displays all the necessary page components functioning together, which provides context for these relatively abstract molecules and organisms.
Important characteristic of templates is that they focus on the page’s underlying content structure rather than the page’s final content

For more details [Click here](http://atomicdesign.bradfrost.com/chapter-2/#templates)


# 'src/components/pages'

> Similar to _Containers_ they hold the data and control the flow of the same.
> Pages can have only Templates.

Pages are the final representation
Pages are specific instances of templates that show what a UI looks like with real representative content in place.[Example](http://atomicdesign.bradfrost.com/images/content/page.png)

_Pages also provide a place to articulate variations in templates, which is crucial for establishing robust and reliant design systems._ Here are just a few examples of template variations:

- A user has one item in their shopping cart and another user has ten items in their cart.
- A web app’s dashboard typically shows recent activity, but that section is suppressed for first-time users.
- One article headline might be 40 characters long, while another article headline might be 340 characters long.
- Users with administrative privileges might see additional buttons and options on their dashboard compared to users who aren’t admins.
- In all of these examples, the underlying templates are the same, but the user interfaces change to reflect the dynamic nature of the content. These variations directly influence how the underlying molecules, organisms, and templates are constructed. Therefore, creating pages that account for these variations helps us create more resilient design systems.

For more details [Click here](http://atomicdesign.bradfrost.com/chapter-2/#pages)


