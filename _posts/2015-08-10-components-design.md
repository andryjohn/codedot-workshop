---
layout: post
title: "🇫🇷Build<strong> your UI Librarie
</strong>"
subtitle: "Components are great for better designs"
section: css
---
<style>.embed-container { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; } .embed-container iframe, .embed-container object, .embed-container embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }</style><div class='embed-container'><iframe src='https://www.youtube.com/embed/ewxMpl09OwE' frameborder='0' allowfullscreen></iframe></div>

# Web Components

Now that you know the basics of HTML & CSS, let’s go a bit deeper into web design and CSS techniques.

* Get used to thinking in terms of web components; UI elements you can combine to build your web pages.

* Learn how to code your own CSS library of them! Having a cool library of components is the most powerful secret of frontend developers.


# Main takeaways

# What’s a component?

A component is a standard UI element that has a precise purpose:

* An **avatar** is generally used for a profile picture

* A **dropdown** list enables to hide/show a secondary navigation

* **Tabs** are here to split the page content into different clickable sections

* A **form** is here to capture user inputs

* A **card** displays each result in a nice way within a collection *(collection of Airbnb apartments, eBay items, etc…)*

![component](/images/components.png)

##Common web components


Combine components to build pages
Once you know all the common web components, building a web page becomes just like playing Lego. All you have to do is combine the right components. Here is an example:


Combining web components

Organize your CSS with component files
From this point, you will start organizing your CSS code with one CSS file for each component. Buttons are standard components, and so are avatars, cards, lists, navbar, tabs, forms, etc.. All these guys deserve their own separate CSS file. It means your project architecture will look like:

{% highlight quote %}

.
├── css
│   ├── components
│   │   ├── avatar.css
│   │   ├── banner.css
│   │   └── button.css
│   └── style.css
└── index.html
{% endhighlight quote %}

Then in style.css:

{% highlight css %}

/* Importing all components file */
@import url("components/avatar.css");
@import url("components/banner.css");
@import url("components/button.css");

{% endhighlight css %}


Then you just need one unique link to style.css in your HTML file:

{% highlight html %}

<head>
  <link rel="stylesheet" href="css/style.css">
</head>
{% endhighlight html %}

## Useful CSS techniques for building components

**Gradient filter**

When you have a card (or a banner) with a background image and some text content, it can be hard to read the text on top of the pictures. To remedy this, you need to add a dark, semi-transparent filter to make the content more readable.

For example, consider this dark filter:

{% highlight html %}

.banner {
  background-image: linear-gradient(rgba(0,0,0,0.8) 0%, rgba(0,0,0,0.2) 50%),
  url('/path/to/background.jpg');

  background-size: cover;
  color: white;
}
{% endhighlight html %}

Applying this gradient makes the header and tagline or Le Wagon so much more readable:


 Banner with a dark filter

![component](/images/gradient-example.png)

## Relative / Absolute

The **relative/absolute** CSS pattern is important when you need to position stuff in a specific place inside a component (e.g. a card).

* Putting the card as `position: relative` is a way to pin it and be able to position the things inside it precisely.

* Then you can make the inner elements `position: absolute` and place them wherever you want in the card thanks to the `top/bottom/left/right` properties.


![component](/images/relative-absolute.png)

<footer>The relative/absolute CSS pattern</footer>

## Flexbox

Flexboxes are awesome. It’s a layout mode intended to accommodate different screen sizes and different display devices. To turn a div into a flexbox is super easy: just add display: flex on your div. Then:

* That div is the flexbox

* All of its children elements are called flex items and can be distributed vertically and horizontally within the flexbox.


![component](/images/vocabulary.png)


## Main flexbox properties

Here are the important CSS properties **on the flexbox** (not on the item):

* `justify-content` distributes flex items horizontally (either with space-around the items or space-between the items).
* `align-items: center` allows use to vertically align the items (very useful).
You can also make a flex item grow and take all available space:

* `flex-grow: 1` will make a flex item grow and push its neighbours on the left and on the right 💪💪💪.

# Exercises

* Build [your own library](https://codedot.tk/UIkit)

* Design the Facebook Like button

*  Build an [Epicurious’ card](https://www.epicurious.com/search/chocolate%20cake)

* Use flexboxes to design your own breaking news feed

# Resources

* Bootstrap web components

* UX components on codepen.io

*  Flexbox guide

* Flexbox Froggy game


Happy Designing 🎨 🎨 🎨
