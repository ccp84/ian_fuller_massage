# Portfolio Project 1 - Cheryl Phillips - "Ian Fuller Sports Massage"

![Preview of homepage](documentation/testing/preview.png)

## Concept

Ian Fuller Sports Massage is a new business startup providing sports massage therapy services. This website aims to promote Ian Fuller Sports Massage to new clients, as well as inform existing clients of offers and provide a means of contact for booking appointments.

### User Stories

Visitors to the site should be able to:
* Load it on a mobile, tablet or desktop
* Navigate between the pages easily
* Find out about the services offered by Ian
* Find the prices of each service
* Contact Ian

### Features of the site

* A consistent header and footer throughout the site, wether viewed on a mobile, tablet or desktop. 
* A welcome from Ian.
* For mobile and tablet views, a collapsible menu to save on screen space.
* Consistent corporate theme - colours used for Ians logo and facebook page are : `#24d9f1` and `#4d4c4f`
* Link to social media. 
* A gallery of recent events.
* A contact form.
* Professional accreditations on display. 

### Wireframes

[Link to Balsamiq files](documentation/wireframes/ian_fuller_massage.bmpr)

#### Mobile View
Designed with a collapsible menu for space saving on small screens. Header and footer will be consistent throughout all pages to maintain a uniform corporate image. Colours blue, grey and white match Ian's logo, printed media, and social media pages. 

![Image of mobile wireframe](documentation/wireframes/mobile.png)

#### Tablet View
Designed with a collapsible menu for space saving still although a larger screen than mobile, space is still at a premium users may be browsing portrait rather than landscape. Header and footer design will follow the same theme as mobile but will utilise the extra space to display the business name in the header. Colours will be consistent with corporate image. 

![Image of tablet wireframe](documentation/wireframes/tablet.png)

#### Desktop View
This design features a full header with a nav bar and main title image on the page. The nav bar will be sticky and follow the user down the page. The footer will remain the same design as the mobile and tablet layout. Colours will be consistent with corportage image. 

![Image of desktop wireframe](documentation/wireframes/desktop.png)

---

## Project Development

### Header Design

I started the project by developing the header as this will be mainly consistent across all pages. This has evolved slightly from the initial concept wireframe as visually the large block of blue at the top of the page as well as a banner image was redundant space on the site and didnt feel balanced. 

The final header design agreed on with the customer has a smaller top bar with the logo overlaying the banner image. 

**Mobile Header**

![Image of mobile header](documentation/testing/mobile_header.png)

The mobile version of the site header and nav bar is viewed on devices 600px or less. This used the ``mobile hide`` class in the stylesheet so that the ``<h1>`` title is not displayed on the small screen width. It displays a different image file for the main banner picture which is thinner to occupy less space on the screen and a smaller sized logo. The hamburger menu is used to ensure navigation does not occupy valuable screen space and detract from the site content. 

**Tablet Header**

![Image of tablet header](documentation/testing/tablet_header.png)

The tablet version of the site header and nav bar is viewed on devices between 600px and 992px. This reverts to standard display of the ``<h1>`` element and uses a larger banner image to take advantage of a bigger screen size. The logo displayed increases in size to take advantage of the screen size increase. Hamburger nav menu is maintained for consistency and clean design. 

**Desktop Header**

![Image of desktop header](documentation/testing/desktop_header.png)
The desktop version of the site header is viewed on any screen wider than 992px. This takes advantage of the banner image in full and the original sized logo image. I have maintained the hamburger nav menu for consistency across the site and after viewing a range of websites with them in use on their desktop version it provides an uncluttered viewing area for the site content. 

### Footer Design
Footer Design was completed next as it is consistent across all pages. This enabled me to clone the index page when creating further pages minimising repetitive work and ensuring consistency. It's main feature is to finish off the overall containment of the main content, and has links to social media and professional memberships related to the business. These links open in a new browser window. 

The footer sticks to the bottom of the viewing screen for asthetics, courtesy of code from Clever Sticky Footer - see credits.

**Mobile Footer**

![Image of mobile footer](documentation/testing/mobile_footer.png)

The mobile footer features a trimmed down version of the facebook image link for space saving. This is achieved using the ``<picture>`` tag with a media query nested inside the html.

**Tablet and Desktop Footer**

![Image of tablet/desktop footer](documentation/testing/tablet_desktop_footer.png)

Both the tablet and desktop views feature a larger "Find us on Facebook" image link to take advantage of the larger viewing area. 

### Landing Page

![Image of all 3 main page views](documentation/testing/mainpage.png)

All 3 views of the main page work from the same main CSS grid layout. 

**Responsive Features**
* The image associated with the 'Welcome' section disappears for mobile users to maximise screen space. 
* The main offer located in the center of the landing page is sized to 100% of the screen for mobile users, this has a ``max width`` however for larger screen sizes so as not to distort the image file, and be too out of proportion with the rest of the content. 
* CSS Flexbox is used in the last grid box on the page. This enables the contact details and opening times to stack on top of each other for mobile users, but spread out for a more balanced view for larger screen sizes. 

### Services and Pricing Page

![Image of all 3 services and pricing page views](documentation/testing/servicepage.png)

The Services and Pricing page is built from the same main CSS grid layout of the homepage for a mobile first approach of stacked boxes for content layout. 

**Responsive Features**
* CSS Flexbox is used to maintain a stacked layout for mobile viewing, and then allow the full width of larger screens to be used for tablet and desktop. 
* To allow for the headings to alternate sides inside the Flexbox layout, reverse display is used for alternate boxes so that the mobile content is still in the correct sequence. 

### Reviews and Gallery Page

![Image of all 3 reviews and gallery page views](documentation/testing/reviewpage.png)

The Reviews and Gallery page is built from the same mobile first CSS grid as the rest of the main site for a clean stacked layout. 

**Responsive Features**
* A secondary grid runs in the background on this page to format the boxes containing client reviews and gallery pictures into a 3 column format for tablet views or 4 columns for desktop. 
* Gallery images take up 100% of the viewing window on mobiles but are constrained to a ``max width`` in order to avoid horizontal scrolling in the secondary grid layouts. 

### Technologies Used
* HTML - Main language used for site functionality.
* CSS - Main language used for site style.
* CSS Grid and CSS Flexbox - Functionality used to enable responsive layout changes for different screenwidth breakpoints. 
* [GitHub](https://github.com/) - Used for version control during project development and cloud hosting of project code.
* [Canva](www.canva.com) - Logo design and image manipulation.
* Paint.net - Used for image manipulation and resizing.
* [Google Fonts](https://fonts.google.com/specimen/Quicksand) - Quicksand font used.
* [GitHub Projects](https://github.com/ccp84/ian_fuller_massage/projects/1) - used to track completion of project components.
![Screenshot of completed project board](/documentation/testing/project_board.png)

---

## Testing
[Link to testing carried out](TESTING.md)

---

## Deployment

The site was deployed to GitHub pages. The steps to deploy are as follows: 
  - In the [GitHub repository](https://github.com/ccp84/ian_fuller_massage), navigate to the Settings tab 
  - From the source section drop-down menu, select the **Main** Branch, then click "Save".
  - The page will be automatically refreshed with a detailed ribbon display to indicate the successful deployment.

The live link can be found [here](https://ccp84.github.io/ian_fuller_massage)

### Local Deployment

In order to make a local copy of this project, you can clone it. In your IDE Terminal, type the following command to clone my repository:

- `git clone https://github.com/ccp84/ian_fuller_massage.git`

Alternatively, if using Gitpod, you can click below to create your own workspace using this repository.

[![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io/#https://github.com/ccp84/ian_fuller_massage)

---

## Credits

**Code**

* [Device breakpoint media queries used from recommendation on W3Schools](https://www.w3schools.com/css/css_rwd_mediaqueries.asp)

``` css
/* Extra small devices (phones, 600px and down) */
@media only screen and (max-width: 600px) {...}

/* Small devices (portrait tablets and large phones, 600px and up) */
@media only screen and (min-width: 600px) {...}

/* Medium devices (landscape tablets, 768px and up) */
@media only screen and (min-width: 768px) {...}

/* Large devices (laptops/desktops, 992px and up) */
@media only screen and (min-width: 992px) {...}

/* Extra large devices (large laptops and desktops, 1200px and up) */
@media only screen and (min-width: 1200px) {...}
```

* [Hamburger menu code from Erik Terwan](https://codepen.io/erikterwan/pen/EVzeRP)
HTML and CSS code used with CSS modifications made to fit site style and theme 

* ['Sticky' footer code from Clever Sticky Footer!](https://css-tricks.com/a-clever-sticky-footer-technique/)

```css
html, body { height: 100%;}

body > footer {
  position: sticky;
  top: 100vh;
}
```

* CSS Flexbox tutorial followed on [W3 Schools](https://www.w3schools.com/css/css3_flexbox.asp)

* CSS Grid tutorial followed on [W3 Schools](https://www.w3schools.com/css/css_grid.asp)

**Images**

* All corporate images copyright of Ian Fuller Sports Massage designed by Cheryl Phillips and Gemma Linsley
* Facebook logo from [Freeiconspng.com](https://www.freeiconspng.com/img/46272)
* FHT logo used under the terms set out in Ian's membership of the [Federation of Holistic Therapists](https://www.fht.org.uk)
* CosmicDinosaur image designed by Chloe Linsley-Thomas 

**Other**

* [Reference used for correct accessibility labelling when hyperlinking an image file](https://usability.yale.edu/web-accessibility/articles/links)