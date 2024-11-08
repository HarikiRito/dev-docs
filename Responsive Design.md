# Responsive Design

## 1. Introduction

Responsive design is a technique that allows us to create websites that are accessible and usable on different devices and screen sizes. 
Usually when making a website from the design, the designer will create a design for desktop, mobile, and tablet. The elements will be different for each device, but usually it not changes much, just the layout will be different.

## 2. How to make a website responsive
I will only focus on how to make a website responsive as a frontend developer. This technique also applies to mobile app development, but I will not cover it in this article since the concept is the same, just the technology is different.

To create a responsive website, we will use CSS media queries. Media queries are a powerful feature of CSS that allows us to apply different styles to a website based on the device's screen size. Read more [here](https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries/Using_media_queries).

For the layout, most of the time we will use the CSS Flexbox and Grid. Flexbox is a powerful layout model that allows us to create flexible and responsive layouts. Grid is a powerful layout model that allows us to create two-dimensional layouts. Read more about [Flexbox](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Basic_Concepts_of_Flexbox) and [Grid](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_grid_layout/Basic_concepts_of_grid_layout).

As of right now, there are many web frameworks that support responsive design out of the box, such as Material UI, Tailwind CSS, etc. These frameworks have their own set of tools and best practices that you can use to create a responsive website.


## 3. What tool do I use?

For me, I prefer to use Tailwind CSS because it has a lot of useful classes that I can use to create a responsive website. You might wonder why I don't use Bootstrap or other frameworks. The reason is that I want to have full control over the website, and I don't want to be limited by the framework.

For me, the atomic design that Tailwind CSS uses is awesome. Since I working intensively with web frameworks such as React, Vue, etc, splitting the UI into small and reusable components is a must. Tailwind CSS's atomic design is a good fit for that.

Other people don't like the Tailwind way because it could pollute the HTML with a lot of classes. I get that, but I don't think it's a big deal. Since I split the UI into small components, I can easily control the styles that applied to the component by just changing the class name. 

It also reduces the CSS bundle size by a lot since only the used classes will be included in the final CSS bundle, and they can be reused in different components.

## 4. Advice for beginners

If you are a beginner, start fresh with the traditional way of writing CSS for the layout. Once you get the hang of it, you can start to use Tailwind CSS or other frameworks to speed up the process.

Also, choosing one screen layout is a good way to start. For example, start with the desktop layout, then create the mobile layout, and then the tablet layout. This way, you can focus on one screen size at a time, and you don't need to worry about creating the layout for all screen sizes at once.
