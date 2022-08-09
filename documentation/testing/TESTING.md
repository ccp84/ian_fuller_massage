# Testing Documentation for Ian Fuller Sports Massage

## User Stories and Features

| Visitors to the site should be able to: |      |
| ----------------------------------------| --- |
| Load it on a mobile, tablet or desktop  | Media queries allow the site to be viewed efficiently at different window widths ![Screenshot of mobile tablet and desktop views](mainpage.png)|
| Navigate between the pages easily       | A consistent menu allows site visitors to navigate between the pages ![Screenshot of the navigation menu](navigation.png)|
| Find the prices of each service         | The prices are clearly visible, including offers from the servies and prices page. ![Screenshot of the services and prices page](servicepage.png)|
| Contact Ian                             | Contact details are visible from the bottom of the main page![Screenshot of contact details box](contact_details.png) |

|Features of the site:                    |         |
| --------------------------------------- | --------|
| A consistent header and footer throughout the site, wether viewed on a mobile, tablet or desktop. | The header and footer, although having minor image file variations for best viewing on each type of device, have a consistent style and layout. ![Image of Desktop header](desktop_header.png) as you can see there is only limited variation from this to the mobile view ![Image of mobile header](mobile_header.png). ![Image of desktop footer](tablet_desktop_footer.png) again very little variation in the footer design ![Image of mobile footer](mobile_footer.png) |
| A welcome from Ian                       | This is included on the main landing page to introduce visitors to the site. ![Screenshot of welcome text from Ian](mainpage.png) |
| For mobile and tablet views, a collapsible menu to save on screen space | The hamburger menu was kept across all designs for site consistency and clean code design. ![Screenshot of navigation menu](navigation.png) |
| Consistent corporate theme               | Use of the main colours and logo tie the site nicely together maintaining a consistent feel throughout the site. ![Preview of all views of the site](preview.png) |
| Link to social media                     | A link to the facebook page is included in the footer ![Screenshot of footer](tablet_desktop_footer.png) |
| A gallery of recent events               | A gallery is included on the reviews page from Joust 24 hour race. ![Screenshot of the picture gallery](gallery.png) |
| A contact form                           | I have not implemented this feature due to the lack of either PHP or JavaScript functionality to make it work properly. As this site is to eventually be used commercially, it is a feature I will be working on following submission to complete the PHP functionality by reviewing learning from my previous degree course to get it working correctly for the customer. |
| Professional accreditations on display   | I have used the FHT logo in the footer of the page in accordance with the rules set out by their membership. This links to Ian's personal page within their site where clients can review his memership of the FHT and leave reviews directly on the site there. ![Screenshot of footer](mobile_footer.png) |

## Code Validation

### W3C Validator

Initially the Reviews page threw up a duplicate classes error from applying two previously created classes to the same `<div>`.
![Screenshot of W3C Validator](w3c_reviews_error.png)
```html
<div class="box2" class="div_pic">
```
```css
 /*Dark box*/
  .box2 {
    color: #24d9f1;
    background-color: #4d4c4f;
    border-style: solid;
    border-width: 1px;
    border-color: #24d9f1;
    margin: 5px;
    padding: 2px;
  }
  /*Use to center and constrain images inside the grid*/
  .div_pic {
    text-align: center;
  }
  ```
To rectify this, I created a new `box2_pic` class for use on the reviews page and applied this to the gallery. 

```css
 /*To box in gallery pictures*/
  .box2_pic {
    color: #24d9f1;
    background-color: #4d4c4f;
    border-style: solid;
    border-width: 1px;
    border-color: #24d9f1;
    margin: 5px;
    padding: 2px;
    text-align: center;
  }
  ```

  All 3 pages now pass through the W3C validator
  ![Screenshots of W3C validation passes](w3c_passed.png)


  ### Jigsaw Validator

  The W3C CSS Jigsaw validation was passed with no errors and just 3 warnings on the code copied for the hamburger menu. 
  ![Screenshot of Jigsaw validation](css_validation.png)

## Responsiveness

## Accessibility (Lighthouse Score)

## Browser Compatibility

[Return to README](../../README.md)