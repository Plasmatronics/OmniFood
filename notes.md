## 7 steps to a great website

# 1).Define
WHO IS THIS FOR? you, a client, your freelancing business, somebody else?
What is the website for? 
    define business and user goals of your web project
    business goal ex: selling premium dog food
    user goal ex: finding high-quality dog food for a good price
Define a very specific target audience.
    ex: Women 20-40, in Euorpe, earning 100k a year, with a passion for dogs
# 2).Plan
Plan and gather website content: copy(text), images, videos, etc.
Content is usually provided bt the client, but you also can help
them produce and find some content
    if they want content charge them extra

For Bigger sites, plan out the sitemap: what pages the site needs, and how
they are related to one another (content hierarchy)

Based on the content, plan what sections each page needs in order to convey the content's message, and in which order

Content GUIDES DESIGN!

Define the website personality
# 3).Sketch
Think about what components you need, and how you can use them in layout patterns
Get ideas out of your head!--> sketch or with some design software like FIgma.

Just keep experimenting until you arrive at a first good solution

You dont need to sketch everything AND DONT MAKE IT PERFECT... at some point you are ready to jump into HTML and CSS


# 4).Design and Build
Use decisions, content, and sketches from steps 1, 2 and 4 to design and build the website w HTML and CSS (Design in the browser)
You already have the layout and components that you selected in the previous step...now you need to design the actual visual styles
Create the design based on selected website personality, and perhaps the design guidelines jonas showed you, and even a lot of external inspiration

# 5).Test and Optimize
Make sure website works well in all MAJOR BROWSERS
Test the website on actual mobile devices, not just in Devtools
optimize all images, in terms of dimensions and file size
fix accessibility problems(like color contrast)
Run the lighthouse performance test and try to fix reported issues
Think about SEO.

# 6).Launch
Upload your website to a hosting platform... we will use a free one called Netlify
Chose and buy a great domain name... one that represents the brand well, is memorable, and is easy to write

# 7).Maintain and Update
Keep the content updated over time. If you are working with a client you can create a monthly maintenance contract (recurring revenue)
Instally analystics software(p much everybody uses google analytics... but there are privacy ones like Fathom)..this may inform future changes in site structure and content

A blog that is updated regularly is a good way to keep users coming back and is also good for SEO.

<!-- LETS IMPLEMENT -->
# Step 1: Define
## Who is it for?
For a Client

## What is it for?
Business Goal: Selling monthly food subscription
user goal: Eating well effortlessly, without spending a lot of time and money

## Target Audience
Busy people who like technology, are interested in a healthy diet, and have a well-paying job

# Step 2: Plan
## we are building a one-page marketing website (landing page)
## "tech company first, but with a major focus on consumer well-being"
 ### So we will go with a startup/upbeat personality with some elements of calm/peaceful

## SECTIONS
-Navigation+logo
-Hero
-Featured in Section
-How it Works
-Meals (and List of Diets)
-Testimonials + gallery
-Features+pricing
-Call to Action(CTA)
-Footer (contact info)

<!-- RESPONSIVE WEB DESIGN PRINCIPLES -->
# High Level Overview
We must implement these principles from the very beginning of a project
Responsive Design technique allows for a webpage to be adjustable to any possible screen size(window or viewport), while maintaining its layout and visual style.

In practice this makes the website consumable on all window sizes and devices

Its a set of best practices...all just CSS

# Responsive Design Ingredients

## 1). Fluid Layouts
To allow webpage to adapt to the current viewport width (or even height)
Use %(or vh/vw) units instead of px for elements that should adapt to viewport (usually layout)
use max-width instead of width

## 2). Responsive Units
use rem units instead of px for most lengths
To make it easy to scale the entire layout down or up automatically
helpful trick: setting 1 rem to 10px for easy calculations

## 3). Flexible Images
By default images dont scale automatically as we change the viewport
Always use % dimensions for images, together with the max-width property

## 4). Media Queries
Without media queries, responsive design wouldnt work at all, so in this way they bring responsive sites to life.
To change CSS Styles on certain viewport widths (called breakpoints)
THis allows us to create different versions of the app for different dimensions

Without the other steps, media queries are useless... we need the others to make media queries useful

## DESKTOP VS MOBILE FIRST DEVELOPMENT
We either start with desktop or mobile development, then media query to shrink/grow to the bigger/smaller screen.
Desktop first is more common, but mobile is becoming more and more modern
mobile first also forces us to really strip our website down to its bare essentials.

<!-- REM AND MAX-WIDTH -->

# More on Rem and Max-Width Properties
## Rem

## Max-Width
when we want the behavior of when theres no more additional space to fix the pixels, the element should simply have the width of the parent container
**if the view is smaller than the "max-width" property in px, then it will become the width of the parent container**

THIS IS DIFFERENT FROM A % width... a % width is contantly a % of the parent
What we want here is different... we want the width to be 1000px until the viewport is too small THEN we want the width to be the parent's width

## rem(root element font size)
the root of the document is the html element
if we dont define any font size on this element, then 1rem is equal to the default browser font-size....16px
so by default 1 rem is 16px... font-size:3 rem is (16*3)px and so on and so forth

The strength of the rem sizing property is its basd on font-size...
if we want to change the basis for rem--> change the font-size on the root element.
     the power of this is we can scale many things by changing the rem scaling via font-size on the html element
Now we can specify font-size, padding, margin ,etc. all in rem.
in dev tools, rem will be converted to px.

The issue: now huge accesibility problems exist for users who need to increase or decrease font size(bc right now the user cannot themselves change it)... so to fix this we change the font-size value on the html element to be a %... if we want the font-size to be 10px, well make it 62.5%

10px/16px=62.5%(percentage of users browsers font size setting)
in other words 62.5% of the default 16 is 10.
Doing this will now respect the user's desired font-size.

