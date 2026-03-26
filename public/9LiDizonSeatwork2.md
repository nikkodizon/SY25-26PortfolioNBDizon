# Seatwork #2 - Getting to know CSS Position and z-index.
### This seatwork will ask you to implement the different CSS position on a given code.
### short link to this .md file is: https://bit.ly/4c61P9K
#### Resources (also found in Khub week 5)
- [4 Minute Youtube Video on CSS Position](https://www.youtube.com/watch?v=YEmdHbQBCSQ)
- [CSS Position Tutorial](https://roycan.github.io/CssPositioningZIndexLab/)

### Instructions: 
1. This is individual submission in khub, but you can work with a partner.  When you submit in khub please place both your names in the submission bin.
2. Guided Activity (30 minutes), please follow what is being required.  

    - Make a copy of this .md file to your Q4 repository and name it as **SectionLNseatwork2.md** example **9LiCruzSeatwork2.md**. Place it in your q4 repository vscode local computer. Committing frequently to your Github repository.  
    - Copy the code below and paste it inside a new file (name it as SectionLNseatwork2.html). Place this file in the same location where the .md file is saved. 
    - Change the content values of the meta tags to your names for author/s and the date today for revised.
    - Please do the following tasks that will ask you to reposition HTML elements then answer the guided question for each task on the .md file. Commit changes to the .md file and to the .html file as well.
    **- This seatwork is worth 20pts and should be submitted by the end of the period** The link to [KHub submission bin](https://khub.mc.pshs.edu.ph/mod/assign/view.php?id=15481).
      - Submit the links to your .md file and .html file.

```html
<!DOCTYPE html>
<html>
<head>
  <meta name="author" content="DIZONVIBAL" />
  <meta name="revised" content="March26-2026" />
  <style>
    body { font-family: Arial, sans-serif; }
    .header, .footer {
      background: lightblue;
      padding: 10px;
    }
    .footer {
       opacity: 0.5;
    }
    .sidebar {
      background: lightgreen;
      width: 150px;
      height: 200px;
    }
    .content {
      background: lightyellow;
      width: 300px;
      height: 200px;
    }    
  </style>
</head>
<body>
  <div class="header">Header</div>
  <div class="sidebar">Sidebar</div>
  <div class="content">Main Content</div>
  <div class="footer">Footer</div>
</body>
</html>
```
### Step 1 (Static vs Relative):

- Add in css ```position: relative; top: 20px; left: 20px;``` to .sidebar.

- Guided Question: What changed compared to the default static positioning? Try to give different values to top and left or you can change it to bottom, right.

- ANSWER: When I added position: relative with top and left values, the sidebar moved from its original position, but it still occupied its original space in the layout and did not affect other elements

### Step 2 (Fixed):

- Add in css ```position: fixed; bottom: 0; width: 100%;``` to .footer.

- Guided Question: What happens when you scroll the page? Why does the footer behave differently from position relative?
- ANSWER: When I scroll the page, the footer stays at the bottom of the screen because position: fixed attaches it to the viewport instead of the normal document flow, unlike relative positioning which moves based on its original position

### Step 3 (Absolute):

- Add in css ```position: absolute; top: 66px; left: 200px;``` to .content.

- Guided Question: What is the effect of position: absolute on an element? How is it different from fixed?
- ANSWER: Using position: absolute moves the content to a specific location based on its nearest positioned parent, and it is removed from the normal flow, unlike fixed which stays relative to the screen

### Step 4 : (Absolute)

- Add in html ```<div class="notice">Notice!</div>``` and include the css below:

```css
.notice {
    position: absolute;
    top: 60px;
    left: 400px;
    background: orange;
    padding: 10px;
    z-index: 2;
}
```

- Give .content a z-index: 1.

- Guided Question: Why does the notice appear on top of the content? What happens if you swap the z‑index values?
- ANSWER: The notice appears on top of the content because it has a higher z-index, and if the values are swapped, the content will appear on top instead

- Challenge: 
    * What changes that you have to do on the code that will position .notice box on the top right corner of the .content box? Please write the code on paper as well (both html and css on the part of .notice and .content).
    * Try to change the position of .content to relative then to fixed. What do you observed each time?
    * What do you observe on about the effect of z-index on .notice and .content boxes?

- To position the notice at the top-right corner of the content, I need to set the content to position: relative and the notice to position: absolute with top: 0 and right: 0
- When I change the content to relative, the notice stays inside it, but when I change it to fixed, both elements stay in place on the screen while scrolling
- I observed that z-index controls which element appears on top, with higher values appearing in front

3. Please answer the following reflection questions (15 minutes)

    a. Could you summarize the differences between the CSS position values (static, relative, absolute, fixed)? 

    b. How does absolute positioning depend on its parent element?

    c. How do you differentiate sticky from fixed (you can research on sticky)?

    d. If you were designing a webpage for a school event, how might you use positioning to highlight important information? Please give concrete examples.

    
REFLECTION
a. The different CSS position values are static, which follows normal flow, relative, which moves based on its original position, absolute, which is positioned based on its parent, and fixed, which stays in place on the screen.

b. Absolute positioning depends on its parent because it uses the nearest positioned ancestor as its reference point.

c. Sticky positioning behaves like relative at first but becomes fixed when it reaches a certain scroll position, while fixed always stays in place.

d. In designing a school event webpage, I can use fixed for navigation bars, absolute for placing buttons or highlights on banners, relative for small adjustments, and sticky for announcements that should remain visible while scrolling.
