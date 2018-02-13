### Week 1 CSSTTR

This week we got started with CSSTTR. We are expected to build a keyboard-accessible website, made for Marijn as the user of this site. Marijn is a great programmer and loves beautiful design. He also has some physical constraints. The given components have to be styled accordingly, using only CSS. 

###### Step 1: 
##### The Concept

My first step was thinking up a concept that would fit all components inside. This isn’t a requirement and could even take up more time than it should, but by doing this I can stay within a specific purpose for my website. The semantic markup and guidelines for the user experience are explicit. This benefits my design and styling. The concept I came up with was a platform for sharing, sorting and connecting music. Songs and playlists are presented and the user can rate the labels given to music they have already listened to. This way, all songs are getting appropriate labels by their listeners. By rating labels on songs, users earn points they can use to “purchase” playlists, so they can contribute. This way, only users who actively rate labels for songs can contribute to playlists. All components are given a purpose in this design. This concept will take up some more time than just putting the components on one page without any meaning or purpose, but will help me empathize with the user and benefit the design. 

###### Step 2: 
##### Research

Before getting started, I wanted to know more about CSS grid. I had to refresh my memory and learn about responsive designs using CSS grid. I watched [this YouTube video](https://youtu.be/7kVeCqQCxlk?t=18m1s). The usage of CSS grid as opposed to FlexBox and the benefits in responsive design are really well explained. It’s shown how to give grid areas (cells) a name and then use that name for the element assigned to those cells. By doing this, only the template rows and columns have to be redefined when the screen width changes. 

A second thing I had to look up, were the best practices for keyboard accessibility. Things like "skip to main"- and "back to top" buttons and styling the :focus and :active elements are examples of practices I'd like to add to my pages. 

###### Step 3: 
##### Actually start writing something

The first thing I did was starting my page with the "navigation.html" component. Before this navigation, a skip to main has to be available. 
```html
<a href="#main">Skip to main content</a>
```
This line is the first one in the body. This skips the <nav> and jumps right to this line:
```html
<main id="main" tabindex="-1">
```
The href in the first line is linked to this ID. The [tabindex](https://developer.mozilla.org/nl/docs/Web/HTML/Global_attributes/tabindex) "indicates if its element can be focused, and if/where it participates in sequential keyboard navigation". I used value "1" because it means the element should be focusable in sequential keyboard navigation, with its order defined by the value of the number.

I did the same with a back to top button, an "a" element at the bottom of main that directs back to body. This way, the tabbing doesn't have lead to changing the URL and getting stuck there. Stay tabbing, and you will get back to the first "skip"-button and get back to the main content. 

###### Step 4:
##### Styling something

I want the "skip"-button to not be visible, unless the user is using their keyboard for navigation. The :focus and :active attributes are perfect for this practice. 
```CSS
a[href="#main"] {
    position: absolute;
    top: auto;
    width: 1px;
    height: 1px;
    overflow: hidden;
    z-index: -10;
}
a[href="#main"]:focus,
a[href="#main"]:active {
    color: #fff;
    background-color: #000;
    top: auto;
    width: 30%;
    height: auto;
    overflow: auto;
    z-index: 10;
}
```
This makes sure the link element is hidden at first and doesn't influence the rest of the elements by using position:absolute. To support the tabbing even more, I used :focus-within on the article elements, so it's clear at all times what item is focussed.

I also added some @media (min-width)'s to later use for the CSS grid. The first CSS I've written is mobile first, so the expansion of the design comes later. 

###### Step 5
##### The assigned additions

The fancy ampersand is the first thing I added from the book. The method of putting a span around the ampersand and working the CSS on that class works, but is messy. We have to style only one character, so the font stacks are used. It will only be used for that one character, and all others will get the second, third, etc. font from our font stack.




### Week 2 CSSTTR

This week, it's a lot more clear as what to do for the final assignment. Sadly, I now know I have to do a lot to hand in everything I wanted to make. Best thing to do now is make a planning and strictly stick to it.

#### Weekly planning

##### 13/02
- [ ] __Complete the HTML as it should be.__
    - [ ] Check if all the right elements are there (like the "lang" attribute). 
    - [ ] Watch the semantic markup, a couple of articles should be in a section.
    - [ ] Add all the pages I want to make and write some content so the components make sense. 
- [ ] __Style everything I have now (on the main page).__
    - [ ] Make sure the nav as it is in components is accessable through tabs in a dropdown.
    - [ ] Make the remaining assignments from last week from the CSS book. 
    - [ ] Add the grid in the media queries.
    - [ ] Figure out how to make a carousel that is accessable through tabs. (tabindex)
- [ ] __This weeks assignments (at least read them all).__
    - [ ] Loading spinner — 8.43
    - [ ] Transitions op :hovers en :focus—8.42
    - [ ] Cursor—6.29
    - [ ] Extending the clickable area—6.30
    - [ ] Custom checkboxes—6.31
    - [ ] (Pseudo)random background—2.7
    - [ ] [Validatie van het formulier](https://codepen.io/joostf/pen/VKyPxk)

##### 13 or 14 or 15 / 02
- [ ] __Read the articles for CSSTTR and make sketchnotes.__
    - [ ] [CSS inheritance](https://www.smashingmagazine.com/2016/11/css-inheritance-cascade-global-scope-new-old-worst-best-friends/)
    - [ ] [Semantic CSS and selectors](https://www.smashingmagazine.com/2013/08/semantic-css-with-intelligent-selectors/)
    - [ ] [Semantic CSS and the framework](https://www.ebayinc.com/stories/blogs/tech/how-our-css-framework-helps-enforce-accessibility/)

##### 15/02
- [ ] __Finish the log-in field.__
    - [ ] Fancy transitions and :focus
    - [ ] Clear transitions that actually help the user
- [ ] __Work out the detail-page.__
    - [ ] Accessable through tabs
    - [ ] Make sure all the HTML is correct
    - [ ] Style it
    - [ ] Add the rating component and style it.
- [ ] __Make the chatbox-component.__
    - [ ] Style it 
    - [ ] Make accessable

- [ ] __Make sure everything from 13/02 is finished, repeat this planning if not.__

##### 16/02 
- [ ] __Push everything on a new branch before 09:37!!!__

