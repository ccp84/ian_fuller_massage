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

**Full Screen**

Fullscreen views and links all tested as working for any size over 992px wide

![Screenshot of full screen view](fullscreen_chrome.png)

**Tablet View**

Tablet view tested as working for any sizes between 600px and 992px wide

![Screenshot of tablet view](tablet_firefox.png)

**Mobile View**

Mobile view tested for any width smaller than 600px wide tested both in a small browser window and on an iphone. 

![Screenshot of mobile view in small browser window](mobile_edge.png)
![Screenshot of mobile view on iphone](mobile_safari.png)

## Accessibility (Lighthouse Score)

### Home Page

**Initial audit points :**
* Image elements do not have explicit `width` and `height`

For the *Current Offer* image, this is handled by the css class applied to make it responsive:
```css
.grid_pic {
    width: 100%;
    max-width: 600px;
  }
```
For the 3 footer images however I have fixed these with a `height` of 50px again in the css as the footer height does not change across the 3 views.

```css
.foot_pic {
  height: 50px;
}
```
* Form elements do not have associated labels

This is referring to the checkbox used in the external code for the hamburger menu. 
```html
<input type="checkbox" />
```
To resolve this I have labelled this checkbox up as acting as a navigation menu 
```html
<input id="navi" type="checkbox" />
<label for="navi">This checkbox is acting as a navigation menu</label>
```
 
 * Document does not have a meta description 

 I have now added this to the `<head>` of the page

**Final Lighthouse scores after bug fixes:**

![Screenshot of lighthouse scores for homepage](home_lighthouse.png)

### Services and Pricing Page

**Initial Audit Points**

* Image elements do not have explicit ``width`` and ``height``

As for the index page, I have applied a `height` of 50px by using the ``foot_pic`` class as the height of the footer element does not change. 

```css
.foot_pic {
  height: 50px;
}
```

* Form elements do not have associated labels

To resolve this I have used the same fix as for the home page with labelling of the checkbox in the navigation menu code. 
```html
<input id="navi" type="checkbox" />
<label for="navi">This checkbox is acting as a navigation menu</label>
```
* Document does not have a meta description

Meta description added to the `<head>` element of the page

**Final Lighthouse scores after bug fixes for services page**

![Screenshot of lighthouse scores for services page](service_lighthouse.png)

### Reviews and Gallery Page

**Initial Audit Points**

* Image elements do not have explicit `width` and `height` 

Gallery images are handeled by the `grid_pic` class to make the responsive when wrapped in the `box2_pic` class:

```css
.grid_pic {
    width: 100%;
    max-width: 600px;
  }
```

The 3 footer images are again maintained at `50px` by the `foot_pic` class:

```css
.foot_pic {
  height: 50px;
}
```

* Form elements do not have associated labels

I have used the same `<label>` fix as on the other 2 pages to resolve this issue.

* Document does not have a meta description

I have added this to the `<head>` element of the document

**Final Lighthouse scores after bug fixes for reviews page**

![Screenshot of Lighthouse score for reviews page](review_lighthouse.png)

## Browser Compatibility

To test cross platform compatibility as far as possible, the site has been tested as working in the following browsers:

* Google Chrome

![Screenshot from Google Chrome](fullscreen_chrome.png)

* Firefox (Developer)

![Screenshot from Firefox blue edition](tablet_firefox.png)

* Microsoft Edge

![Screenshot from Edge](mobile_edge.png)

* Safari

![Screenshot from Safari](mobile_safari.png)

[Return to README](../../README.md)