![Pranjal Final Project Look](https://github.com/user-attachments/assets/b4f668f5-2824-4f19-b4fa-580e9dd5583e)
# Pranjal Khandelwal - Personal Portfolio Website
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Last Commit](https://img.shields.io/github/last-commit/golu19102003/Pranjal-Portfolio.svg)](https://github.com/golu19102003/Pranjal-Portfolio/commits/main)
[![Open Issues](https://img.shields.io/github/issues/golu19102003/Pranjal-Portfolio.svg)](https://github.com/golu19102003/Pranjal-Portfolio/issues)

## Overview

This repository contains the source code for my personal portfolio website, designed to showcase my skills, projects, professional experiences, and contact information. The website features a clean, modern, and responsive design with engaging animations and interactive elements to provide visitors with a comprehensive understanding of my capabilities and background.

The project is built using a combination of fundamental web technologies:

* **HTML:** Provides the semantic structure and organization of the website's content. It acts as the skeleton upon which the visual presentation and interactive behaviors are built.
* **CSS:** (Cascading Style Sheets) is used to style the website, controlling its layout, colors, typography, responsiveness across different devices, and visual effects like animations and transitions. The styles are primarily defined in the separate `stylesheet.css` file.
* **JavaScript:** Adds dynamic behavior and interactivity to the website. This includes the animated typing effect on the homepage (powered by the Typed.js library) and potentially other custom scripts for form handling, dynamic content updates, and UI enhancements (likely located in `main.js`).

The website aims to provide a seamless and engaging user experience, allowing visitors to easily navigate through different aspects of my professional profile.

## Technologies Used
A detailed breakdown of the technologies integrated into this portfolio website:

* **Core Web Technologies:**
    * **HTML (`index.html`):** The foundational markup language that structures all the content of the website, divided into logical sections like header, home, about, skills, portfolio, experience, and contact.
    * **CSS (`stylesheet.css`):** An external stylesheet responsible for the entire visual presentation of the website. This includes layout management (using techniques like Flexbox and Grid), color schemes, typography, handling responsiveness for various screen sizes (although explicit media queries need to be reviewed in `stylesheet.css`), and implementing animations.
    * **JavaScript (`main.js` - optional):** An external JavaScript file that likely contains custom scripts to add interactive features beyond basic HTML and CSS. This could include form submission handling, dynamic manipulation of the DOM, or custom UI behaviors.

* **External Libraries and Frameworks:**
    * **Font Awesome (via CDN):** A comprehensive icon library used to embed scalable vector icons throughout the website, enhancing visual communication (e.g., social media icons in the home and contact sections).
    * **Boxicons (via CDN):** Another open-source icon set utilized for various UI elements, such as the icons in the "Services" section and potentially others.
    * **Typed.js (via CDN):** A JavaScript library specifically used to create the animated typing effect in the "Home" section, where the profession is dynamically displayed.

## File Structure

The repository is organized with the following structure to maintain clarity and manageability:

portfolio/
├── index.html          # The main HTML file containing the website structure.
├── stylesheet.css      # The CSS file responsible for styling the website.
├── main.js             # (Optional) JavaScript file for custom interactive scripts.
└── assets/             # (Optional) Directory to store images, fonts, or other static assets.
└── ...


## Detailed Explanation of the Code
### 1. `index.html` (HTML Structure)
The `index.html` file provides the structural framework of the portfolio website. It is organized into distinct sections using semantic HTML5 tags:

* **`<head>` Section:**
    * `<meta charset="UTF-8">`: Specifies the character encoding for proper display of various characters.
    * `<meta http-equiv="X-UA-Comapatible" content="IE=edge">`: Ensures compatibility with the latest rendering engine in Internet Explorer.
    * `<meta name="viewport" content="width=device-width, initial-scale=1.0">`: Configures the viewport for responsive design, ensuring the website scales correctly on different devices.
    * `<title>portfolio</title>`: Sets the title that appears in the browser tab or window title bar.
    * `<link rel="stylesheet" href="stylesheet.css">`: Links the external CSS file (`stylesheet.css`) to style the HTML elements.
    * `<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" integrity="..." crossorigin="anonymous" referrerpolicy="no-referrer" />`: Includes the Font Awesome library from a CDN for using various icons. The `integrity` and `crossorigin` attributes enhance security.
    * `<link href='https://unpkg.com/boxicons@2.1.4/css/boxicons.min.css' rel='stylesheet'>`: Links the Boxicons library from a CDN, providing another set of icons.
    * `<script src="https://unpkg.com/typed.js@2.0.15/dist/typed.umd.js"></script>`: Includes the Typed.js library from a CDN, necessary for the animated typing effect.
    * `<script src="https://cdn.jsdelivr.net/npm/typed.js@2.0.11"></script>`: **Note:** This line includes Typed.js again, potentially a duplicate or an older version. It's advisable to use a single, consistent version.

* **`<header class="header">`:** The top section of the website containing the navigation.
    * `<a href="#" class="logo">Portfolio.</a>`: The website's logo, acting as a link back to the homepage. The `#` indicates it currently links to the top of the same page.
    * `<nav class="navbar">`: The navigation menu.
        * `<a href="#home" style="--i:1" class="active">Home</a>`: Link to the "Home" section. The `style="--i:1"` likely applies a CSS variable for animation staggering. The `active` class indicates the current or default active page.
        * `<a href="#about" style="--i:2">About</a>`: Link to the "About" section.
        * `<a href="#skills" style="--i:3">Skills</a>`: Link to the "Skills" section.
        * `<a href="#project" style="--i:4">Portfolio</a>`: Link to the "Portfolio/Project" section.
        * `<a href="#experiences" style="--i:5">Experience</a>`: Link to the "Experience" section.
        * `<a href="#contact" style="--i:6">Contact</a>`: Link to the "Contact" section.

* **`<section class="home" id="home">`:** The main introductory section.
    * `<div class="home-content">`: Contains the textual content.
        * `<h3>Hello, It's Me</h3>`
        * `<h1>Pranjal Khandelwal</h1>`
        * `<h3>And I'm a <span class="text"></span></h3>`: The `<span>` with the class `text` is the target for the Typed.js animation, displaying the different roles.
        * `<p>`: A brief description of my professional interests and skills.
        * `<div class="home-sci">`: Container for social media icons.
            * `<a href="..." style="--i:8"><i class="fab fa-linkedin"></i></a>`: LinkedIn profile link using a Font Awesome icon. The `style="--i:8"` likely contributes to animation staggering. Similar links exist for GitHub, Twitter, Facebook, and Instagram.
        * `<a href="#" class="btn-box"> More About Me</a>`: A button to navigate to the "About" section.

    * `<span class="home-imgHover"></span>`: An empty `<span>` likely used for a visual hover effect on the home section background, styled in `stylesheet.css`.

* **`<section class="about" id="about">`:** The section providing information about me.
    * `<div class="about-img">`: Contains the profile picture.
        * `<img src="...">`: The source URL of the profile image.
    * `<div class="about-text">`: Contains the descriptive text.
        * `<h2>About<span>Me</span></h2>`
        * `<h4>Software Developer</h4>`: My primary role/title.
        * `<p>`: A more detailed paragraph about my background, education, and professional philosophy.
        * `<a href="#" class="btn-box">More About Me</a>`: Another button, potentially leading to more detailed information or further down the section.

* **`<section>` (containing `<div class="services" id="services">`)`:** This section highlights my key service areas.
    * `<div class="container">`: Likely used for layout and responsiveness.
    * `<h1 class="sub-title">My<span>Services</span></h1>`
    * `<div class="services-list">`: Contains individual service blocks. Each block includes:
        * An icon (`<i class='bx bx-chart' style='color:#00eeff'></i>`, `<i class='bx bx-code-alt' style='color:#00eeff'></i>'`, `<i class='bx bx-crop' style='color:#00eeff'></i>'`) using Boxicons with inline styling for color.
        * `<h2>`: The title of the service (e.g., "Data Science Enthusiast").
        * `<p>`: A brief description of the service offered.
        * `<a href="#" class="read">Learn More</a>`: A link to get more details about the service.

* **`<h1 class="sub-title">My<span>Skills</span></h1>`**
* **`<Section>` (containing `<div class="container1" id="skills">`)`:** This section showcases my technical and professional skills.
    * **Technical Skills:**
        * `<h1 class="heading1">Technical Skills</h1>`
        * `<div class="Technical-bars">`: Contains individual technical skill bars. Each skill `div` includes:
            * An icon (`<i style="..." class='bx bxl-html5'></i>'`, `<i style="..." class='fab fa-node-js'></i>'`, etc.) with inline color styling.
            * `<div class="info"><span>Skill Name</span></div>`: Displays the name of the technical skill.
            * `<div class="progress-line skill-name"><span></span></div>`: The `<span>` inside this `div` is likely styled using CSS (based on the class name like `html`, `css`, `javascript`) to visually represent the proficiency level.

    * **Professional Skills:**
        * `<h1 class="heading1">Professional Skills</h1>`
        * `<div class="radial-bars">`: Contains circular progress indicators for professional skills. Each skill `div` includes:
            * `<svg x="0px" y="0px" viewBox="0 0 200 200">`: An SVG element to draw the circular progress bar.
                * `<circle class="progress-line" cx="100" cy="100" r="80"></circle>`: The static background circle.
                * `<circle class="path path-n" cx="100" cy="100" r="80"></circle>`: The dynamic circle that represents the skill level. The `path-n` class (e.g., `path-1`, `path-2`) is likely used with CSS and potentially JavaScript to control the fill.
            * `<div class="percentage">XX%</div>`: Displays the percentage value of the skill.
            * `<div class="text">Skill Name</div>`: The name of the professional skill.

* **`<section>` (containing `<div id="portfolio" id="project">`)`:** This section displays my projects.
    * `<div class="main-text" id="project">`: Contains the section title.
        * `<h2>Latest<span>Projects</span></h2>`
    * `<div class="portfolio-content">`: Contains individual project listings. Each project `div` (with class `row`) includes:
        * `<img src="...">`: The image representing the project.
        * `<div class="layer">`: An overlay that appears on hover, providing project details.
            * `<h5>Project Title</h5>`
            * `<p>Project Description...</p>`
            * `<a href="#"><i class='bx bx-link-external' style="color: aliceblue"></i></a>`: A link icon (currently linking to `#`).

* **`<section>` (containing `<div class="services" id="experiences">`)`:** This section details my professional experiences.
    * `<div class="container">`
    * `<h1 class="sub-title">My<span>Experiences</span></h1>`
    * `<div class="services-list">`: Contains individual experience blocks. Each block includes:
        * `<img src="..." alt="Company Logo" style="width:50px; height:50px;color:#0ef">`: The logo of the company/organization.
        * `<h2>Role @ Company/Organization</h2>`
        * `<p>Location: ..., Duration: ..., Description: ...</p>`: Details about the role, duration, and responsibilities.
        * `<a href="#" class="read">Learn More</a>`: A link for more information (currently linking to `#`).

* **`<section class="contact" id="contact">`:** The contact information section.
    * `<div class="contact-text">`: Contains contact details and a call to action.
        * `<h1>Contact<span>Me</span></h1>`
        * `<h4>Let's Work Together</h4>`
        * `<p>`: A brief encouraging message for potential collaborators.
        * `<div class="contact-list">`: Contains contact information.
            * `<li><i class='bx bxs-send'></i>email@example.com</li>`
            * `<li><i class="bx bxs-phone"></i>phone number</li>`
        * `<div class="contact-icons">`: Social media links (same as in the "Home" section).
    * `<div class="contact-form">`: The contact form.
        * `<form action="">`: The form element. The empty `action` attribute means it will submit to the same page. **Note:** A server-side script or a form submission service would be needed to process the submitted data.
        * `<input type="" placeholder="..." required>`: Input fields for name, email, and subject, with the `required` attribute.
        * `<textarea name="" id="" cols="40" rows="10" placeholder="..." required></textarea>`: A text area for the message.
        * `<input type="submit" value="submit" class="send">`: The submit button.

* **`<div class="last-text">`:** The footer section.
    * `<p>Developed with love by Pranjal Khandelwal @2025</p>`: Copyright information.

* **`<a href="#" class="top"><i class='bx bx-up-arrow-alt'></i></a>`:** A back-to-top button using a Boxicons icon.

* **`<script src="main.js"></script>`:** Links the external JavaScript file (`main.js`) at the end of the `<body>`, ensuring the HTML content is loaded before the script executes.








### 2. `stylesheet.css` (CSS Styling)
The `stylesheet.css` file contains all the styles that define the visual appearance of the website. Key aspects include:
* **Basic Reset:** Sets default margins, paddings, and `box-sizing` for all elements to ensure consistent styling across browsers.
* **Body Styling:** Defines the overall background color and text color of the website.
* **Header Styling:** Styles the fixed navigation header, including the logo, navigation links, and their hover effects. It likely uses CSS for layout (e.g., Flexbox) and includes animations for the header elements.
* **Home Section Styling:** Styles the main landing section with background images, text positioning, social media icons, and the "More About Me" button. It also includes styles for the hover effect on the background.
* **About Section Styling:** Defines the layout for the image and text content in the "About" section, potentially using CSS Grid or Flexbox.
* **Services Section Styling:** Styles the container for the service listings and the individual service blocks, including icons, text, and the "Learn More" links.
* **Skills Section Styling:**
    * Styles the headings for technical and professional skills.
    * **Technical Skills:** Styles the individual skill bars, including the background, the progress indicator (likely using CSS `width` property based on the class names), and the text labels.
    * **Professional Skills:** Styles the container for the radial bars and the SVG elements. It likely uses CSS to style the static circle (`progress-line`) and the dynamic path (`path-n`). **Note:** The actual animation of the radial bars to represent the percentages likely involves JavaScript manipulating the `stroke-dasharray` and `stroke-dashoffset` properties of the SVG circles.
* **Portfolio/Project Section Styling:** Styles the grid layout for the project thumbnails and the overlay that appears on hover with project details.
* **Experiences Section Styling:** Similar to the "Services" section, it styles the layout for the experience listings, including company logos, roles, descriptions, and "Learn More" links.

The `stylesheet.css` file defines the visual styling of the portfolio website. Here's a detailed breakdown of the styles applied to different elements:
### A. Global Reset and Body Styles
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'poppins', sans-serif;
}

body {
    color: #ededed; /* Light gray text color */
    background: #081b29; /* Dark blue background color */
}
* **(Universal Selector):** Resets the default margin, padding, and sets the box-sizing to border-box for all elements, ensuring consistent box model behavior. It also sets the default font-family to 'poppins' with a sans-serif fallback.
body: Sets the default text color to a light gray (#ededed) and the background color to a dark blue (#081b29) for the entire webpage.

### B. Header Styles
.header {
    position: fixed; /* Fixed positioning at the top of the viewport */
    top: 0;
    left: 0;
    width: 100%;
    padding: 20px 10%; /* Top/bottom padding of 20px, left/right of 10% */
    background: transparent; /* Transparent background */
    display: flex; /* Enables Flexbox layout */
    justify-content: space-between; /* Spaces out logo and navigation */
    align-items: center; /* Vertically aligns logo and navigation */
    z-index: 100; /* Ensures the header stays on top of other elements */
}
.logo {
    position: relative;
    font-size: 25px;
    color: #fff; /* White logo text */
    text-decoration: none;
    font-weight: 600;
    cursor: default;
    opacity: 0; /* Initially hidden */
    animation: slideRight 1s ease forwards; /* Slide-in animation from the left */
}
.navbar a {
    display: inline-block; /* Allows setting width/height and inline flow */
    font-size: 25px;
    color: #fff; /* White navigation link text */
    text-decoration: none;
    font-weight: 500;
    margin-left: 35px; /* Spacing between navigation links */
    transition: .3s; /* Smooth transition for hover effects */
    animation: slideTop .5s ease forwards; /* Slide-in animation from the bottom */
    animation-delay: calc(.2s * var(--i)); /* Staggered animation delay using CSS variable */
}
.navbar a:hover {
    color: #0ef; /* Cyan color on hover */
}
* **.header:** Styles the fixed header at the top. It uses Flexbox to arrange the logo and navigation links with space in between and vertically centered. The z-index ensures it remains visible while scrolling.
* **.logo:** Styles the website logo. It's initially hidden (opacity: 0) and animated to slide in from the left using the slideRight animation.
* **.navbar a:** Styles the individual navigation links. They are displayed as inline-block elements, have white text, and are animated to slide in from the top with a staggered delay based on a CSS variable (--i) likely set in the HTML. A smooth transition is applied for hover effects.
* **.navbar a:hover:** Changes the color of the navigation links to cyan (#0ef) on hover.

### C. Home Section Styles
.home {
    position: relative;
    width: 100%;
    justify-content: space-between;
    height: 100vh; /* Full viewport height */
    background: url("[https://ik.imagekit.io/o8qjepjebt/Untitled%20design.png?updatedAt=1748330997199](https://ik.imagekit.io/o8qjepjebt/Untitled%20design.png?updatedAt=1748330997199)") no-repeat; /* Background image */
    background-size: cover; /* Scales the background image to cover the entire element */
    background-position: center; /* Centers the background image */
    display: flex; /* Enables Flexbox layout */
    align-items: center; /* Vertically aligns content */
    padding: 70px 10% 0; /* Top padding, left/right padding, no bottom padding */
}
.home-content {
    max-width: 600px; /* Limits the maximum width of the content */
}
.home-content h3 {
    font-size: 32px;
    font-weight: 700;
    opacity: 0; /* Initially hidden */
    animation: slideBottom 1s ease forwards; /* Slide-in animation from the top */
    animation-delay: .7s;
}
.home-content h3:nth-of-type(2) {
    margin-bottom: 30px;
    animation: slideTop 1s ease forwards; /* Slide-in animation from the bottom */
    animation-delay: .7s;
}
.home-content h3 span {
    color: #0ef; /* Cyan color for the span within the h3 */
}
.home-content h1 {
    font-size: 56px;
    font-weight: 700;
    margin: -3px 0;
    opacity: 0; /* Initially hidden */
    animation: slideRight 1s ease forwards; /* Slide-in animation from the left */
    animation-delay: 1s;
}
.home-content p {
    font-size: 20px;
    opacity: 0; /* Initially hidden */
    animation: slideLeft 1s ease forwards; /* Slide-in animation from the right */
}
.home-sci a {
    display: inline-flex; /* Inline Flexbox for icon alignment */
    justify-content: center;
    align-items: center;
    width: 40px;
    height: 40px;
    background: transparent;
    border: 2px solid #0ef; /* Cyan border */
    border-radius: 50%; /* Circular shape */
    font-size: 20px;
    color: #0ef; /* Cyan icon color */
    text-decoration: none;
    transition: .5s ease; /* Smooth transition for hover effects */
    opacity: 0; /* Initially hidden */
    animation: slideLeft 1s ease forwards; /* Slide-in animation from the right */
    animation-delay: calc(.2s * var(--i)); /* Staggered animation delay */
    margin: 30px 15px 30px 0; /* Spacing around social icons */
}
.home-sci a:hover {
    background: cyan;
    color: #081b29; /* Dark blue icon color on hover */
    box-shadow: 0 0 20px cyan; /* Cyan box shadow on hover */
}
.btn-box {
    display: inline-block;
    padding-top: 15px;
    padding-left: 32px;
    background: #0ef; /* Cyan background */
    border-radius: 40px;
    width: 200px;
    height: 50px;
    font-size: 16px;
    color: #081b29; /* Dark blue text color */
    letter-spacing: 1px;
    text-decoration: none;
    font-weight: 600;
    opacity: 0; /* Initially hidden */
    animation: slideTop 1s ease forwards; /* Slide-in animation from the bottom */
    animation-delay: 2s;
    box-shadow: 0 0 5px #0ef,
                0 0 25px #0ef; /* Cyan box shadow */
}
.btn-box:hover {
    box-shadow: 0 0 5px cyan,
                0 0 25px cyan, 0 0 50px cyan,
                0 0 100px cyan, 0 0 200px cyan; /* More intense cyan box shadow on hover */
}
* **.home:** Styles the main home section, setting its height to the full viewport, applying a background image, using Flexbox for layout, and adding padding.
* **.home-content:** Limits the width of the text content within the home section.
* **.home-content h3, .home-content h3:nth-of-type(2), .home-content h1, .home-content p:** Style the headings and paragraph text within the home section. They are initially hidden and animated to slide in from different directions with varying delays.
* **.home-content h3 span:** Styles the <span> element within the h3 to have a cyan color, likely used for highlighting.
* **.home-sci a:** Styles the social media icons as circular elements with a cyan border and text. They are animated to slide in from the left with a staggered delay.
* **.home-sci a:hover:** Changes the background to cyan, text to dark blue, and adds a cyan box shadow on hover.
* **.btn-box:** Styles the "More About Me" button with a cyan background, rounded corners, dark blue text, and a subtle cyan box shadow. It's animated to slide in from the top.
* **.btn-box:hover:** Applies a more pronounced and layered cyan box shadow on button hover.
  
### D. About Section Styles
.about{
    display: grid; /* Enables Grid layout */
    grid-template-columns: repeat(2,1fr); /* Creates two equal-width columns */
    align-items: center; /* Vertically aligns items in the grid */
    gap: 1.5rem; /* Spacing between grid items */
}
.about-img img{
    padding-bottom: 20%;
    max-width: 630px;
    height: auto;
    width: 100%;
    border-radius: 8px;
}
.about-text h2{
    font-size: 60px;
}
.about-text h2 span{
    color: #0ef; /* Cyan color for the span within the h2 */
}
.about-text h4{
    font-size: 29px;
    font-weight: 600;
    color: #fff; /* White text color */
    line-height: 1.7;
    margin: 15px 0 30px; /* Top/bottom margin */
}
.about-text p{
    color:aliceblue; /* Light blue text color */
    font-size: 20px;
    line-height: 1.4;
    margin-bottom: 4rem;
}
* **.about:** Uses CSS Grid to create a two-column layout for the image and text in the "About" section, with vertical alignment and a gap between the columns.
* **.about-img img:** Styles the image within the "About" section, setting a maximum width, making it responsive, and adding a slight bottom padding and rounded corners.
* **.about-text h2:** Styles the main heading of the "About" section.
* **.about-text h2 span:** Styles the <span> within the heading to be cyan.
* **.about-text h4:** Styles the subheading with a white color and specific font size, weight, and line height.
* **.about-text p:** Styles the paragraph text with a light blue color, font size, and line height, adding a bottom margin.

### E. Services Section Styles
#services{
    color: aliceblue; /* Light blue text color */
    font-size:  20px;
    line-height: 1.4;
    margin-bottom: 4rem;
}
.sub-title{
    text-align: center;
    font-size: 60px;
    padding-bottom: 70px;

}
.sub-title span{
   color: #0ef; /* Cyan color for the span within the subheading */
}
.container{
    padding: 90px;
}
.services-list{
    display: grid; /* Enables Grid layout */
    grid-template-columns: repeat(auto-fit,minmax(259px,1fr)); /* Creates responsive columns */
    grid-gap: 40px; /* Spacing between service items */
    margin-top: 20px;
}
.services-list div{
    background-color: transparent;
    padding: 40px;
    font-size: 13px;
    font-weight: 13px;
    border-right: 10px; /* Note: This might not be intended for a solid border */
    border-radius: 20px;
    transition: background 0.5s, transform 0.5s; /* Smooth transitions for hover */
    box-shadow: 1px 1px 20px #012290f7,
                1px 1px 40px #0053b8f7; /* Blue box shadows */
}
.services-list div i {
    font-size: 50px;
    margin-bottom: 30px;
}
.services-list div h2{
    font-size: 30px;
    font-weight: 500;
    margin-bottom: 15px;
}
.services-list div a {
    display: inline-block;
    justify-content: center;
    text-align: center;
    width: 200px;
    height: 50px;
    background-color: #0ef; /* Cyan background */
    border: 2px solid #0ef; /* Cyan border */
    margin-top: 20px;
    padding-top: 13px;
    border-radius: 25px;
    font-size: 16px;
    color: #081b29; /* Dark blue text */
    text-decoration: none;
    transition: .5s ease;
    opacity: 0; /* Initially hidden */
    animation: slideLeft 1s ease forwards; /* Slide-in animation */
    animation-delay: calc(.2s * var(--i)); /* Staggered animation */
    margin: 30px 15px 30px 0;
}
.services-list a:hover {
    background: cyan;
    color: #081b29;
    box-shadow: 0 0 20px cyan,
                0 0 25px cyan, 0 0 50px cyan,
                0 0 100px cyan, 0 0 200px cyan; /* More intense cyan box shadow on hover */
}
}

### F. Services Section Styles (Continued)
.read {
    display: inline-block;
    padding: 12px 28px;
    background: #0ef; /* Cyan background */
    border-radius: 40px;
    font-size: 16px;
    color: #081b29; /* Dark blue text */
    letter-spacing: 1px;
    text-decoration: none;
    font-weight: 600;
    opacity: 0; /* Initially hidden */
    animation: slideTop 1s ease forwards; /* Slide-in animation */
    animation-delay: 2s;
    box-shadow: 0 0 5px #0ef,
                0 0 25px #0ef; /* Cyan box shadow */
    border: 2px solid #0ef; /* Cyan border */
    transition: background-color 0.3s ease, color 0.3s ease; /* Smooth transition for hover */
}
.read:hover {
    box-shadow: 0 0 5px cyan,
                0 0 25px cyan, 0 0 50px cyan,
                0 0 100px cyan, 0 0 200px cyan; /* More intense cyan box shadow on hover */
}
.services-list div:hover{
    transform: translateY(-10px); /* Slight upward movement on hover */
}
* **.sub-title:** Styles the main subheading for the "Services" section. It centers the text, sets a large font size of 60px, and adds a substantial bottom padding of 70px to create visual separation.
* **.sub-title span:** Specifically styles the <span> element within the .sub-title, setting its color to cyan (#0ef) for emphasis.
* **.container:** This class likely acts as a container for the "Services" section content, adding a consistent padding of 90px on all sides to control spacing around the content.
* **.services-list:** This is the container for the individual service blocks. It utilizes CSS Grid to create a responsive layout (repeat(auto-fit,minmax(259px,1fr))). This means it will create as many columns as can fit within the container, with each column having a minimum width of 259px and sharing equal available space. A grid-gap of 40px adds spacing between the service items. A margin-top of 20px provides some space below the subheading.
* **.services-list div:** Styles each individual service block.
* **background-color: transparent;:** Makes the default background transparent.
* **padding: 40px;:** Adds padding inside each service block.
* **font-size: 13px; font-weight: 13px;:** Sets a small font size and weight for the text within the block. Note: The font-weight: 13px seems unusual as font weights are typically multiples of 100. This might be a typo and intended to be a standard weight like 300 or 400.
* **border-right: 10px;:** Adds a 10px right border. Note: This might not be the intended visual effect as no border-style or border-color is specified, so it might appear as a default solid black border unless overridden elsewhere.
* **border-radius: 20px;:** Rounds the corners of the service block.
* **transition: background 0.5s, transform 0.5s;:** Applies smooth transitions for changes in background and transform properties (used for the hover effect).
* **box-shadow: 1px 1px 20px #012290f7, 1px 1px 40px #0053b8f7;:** Adds two layers of blue box shadows to create a subtle depth effect.
* **.services-list div i:** Styles the icons within each service block, setting a large font-size of 50px and adding a margin-bottom of 30px for spacing below the icon.
* **.services-list div h2:** Styles the service titles, setting a font-size of 30px, a font-weight of 500, and a margin-bottom of 15px.
* **.services-list div a:** Styles the "Learn More" links within each service block.
* **display: inline-block; justify-content: center; text-align: center;:** Makes it a block-level element that can be sized and centers its content.
* **width: 200px; height: 50px;:** Sets a fixed width and height for the button.
* **background-color: #0ef; border: 2px solid #0ef;:** Gives it a cyan background and border.
* **margin-top: 20px; padding-top: 13px;:** Adds top margin and padding to position the text within the button.
* **border-radius: 25px;:** Rounds the corners of the button.
* **font-size: 16px; color: #081b29; text-decoration: none;:** Sets the text style.
* **transition: .5s ease; opacity: 0; animation: slideLeft 1s ease forwards; animation-delay: calc(.2s * var(--i)); margin: 30px 15px 30px 0;:** Applies a smooth transition, initially hides the button (opacity: 0), animates it to slide in from the left with a staggered delay, and adds margins.
* **.services-list a:hover:** Styles the "Learn More" link on hover, changing the background to cyan, the color to #081b29 (dark blue), and applying a more intense cyan box shadow.
* **.read:** This class seems to be a duplicate style for the "Learn More" links, potentially applied directly in the HTML as well. It has similar styling to .services-list div a but with a different animation (slideTop). It also includes a border and a transition for the background-color and color.
* **.read:hover:** Similar hover effect to .services-list a:hover with an intense cyan box shadow.
* **.services-list div:hover:** Applies a transform: translateY(-10px); on hover, causing the entire service block to move slightly upwards, providing a visual interaction cue.

### G. Skills Section Styles
section{
    display: flex; /* Enables Flexbox layout for sections */
    flex-wrap: wrap; /* Allows items to wrap to the next line on overflow */
}
.container1{
    width: 600px; /* Fixed width for the skills container */
    height: 500px; /* Fixed height for the skills container */
    padding: 75px 90px; /* Padding inside the container */
    margin-left: 120px; /* Left margin to position the container */
}
.heading1{
    text-align: center; /* Centers the heading text */
    text-decoration: underline; /* Adds an underline */
    text-underline-offset: 10px; /* Space between text and underline */
    text-decoration-thickness: 5px; /* Thickness of the underline */
    margin-bottom: 90px; /* Bottom margin for spacing */
}
.bar{
    font-size: 23px;
    position: relative;
    align-items: center;
    margin-bottom: 25px;
}
.Technical-bars .bar{
    margin-top: 40px 0; /* Top and bottom margin for technical skill bars */
}
.Technical-bars .bar:first-child{
    margin-top: 0; /* No top margin for the first technical skill bar */
}
.Technical-bars .bar:last-child{
    margin-bottom: 0; /* No bottom margin for the last technical skill bar */
}
.Technical-bars .bar .info{
    margin-bottom: 5px; /* Bottom margin for skill info */
}
.Technical-bars .bar .info span{
    font-size: 17px;
    font-weight: 500;
    animation: showtext 0.5s ease forwards; /* Fade-in animation */
    opacity: 0; /* Initially hidden */
}
.Technical-bars .bar .progress-line{
    position: relative;
    border-radius: 10px;
    width: 100%;
    height: 5px;
    background-color: #000000; /* Black background for the progress bar track */
    animation: animate 1s cubic-bezier(1,0,0.5,1) forwards; /* Animation to expand the progress bar */
    transform: scaleX(0); /* Initially scaled to 0 width */
    transform-origin: left; /* Animation starts from the left */
}
.Technical-bars .bar .progress-line span{
    height: 100%;
    background-color: #0ef; /* Cyan color for the progress bar fill */
    position: absolute;
    border-radius: 10px;
    animation: animate 1s 1s cubic-bezier(1,0,0.5,1) forwards; /* Delayed animation for the fill */
    transform: scaleX(0); /* Initially scaled to 0 width */
    transform-origin: left; /* Animation starts from the left */
}
.progress-line.html span{
    width: 95%; /* Sets the fill width for HTML skill */
}
.progress-line.css span{
    width: 80%; /* Sets the fill width for CSS skill */
}
.progress-line.javascript span{
    width: 75%; /* Sets the fill width for JavaScript skill */
}
.progress-line.react span{
    width: 80%; /* Sets the fill width for React skill */
}
.progress-line.node span{
    width: 70%; /* Sets the fill width for Node.js skill */
}
.progress-line.express span{
    width: 75%; /* Sets the fill width for Express.js skill */
}
.progress-line.mongodb span{
    width: 80%; /* Sets the fill width for MongoDB skill */
}
.progress-line.mysql span{
    width: 80%; /* Sets the fill width for MySQL skill */
}
.progress-line.c-basics span{
    width: 95%; /* Sets the fill width for C Basics skill */
}
.progress-line.java span{
    width: 85%; /* Sets the fill width for Java skill */
}
.progress-line.dsa span{
    width: 60%; /* Sets the fill width for DSA skill */
}
.progress-line.ai-ml-concepts span{
    width: 75%; /* Sets the fill width for AI/ML Concepts skill */
}
.progress-line.software-development span{
    width: 90%; /* Sets the fill width for Software Development skill */
}
.progress-line.salesforce span{
    width: 80%; /* Sets the fill width for Salesforce skill */
}
.progress-line span::after{
    position: absolute;
    padding: 1px 8px;
    background-color: #000; /* Black background for the percentage label */
    color: #fff; /* White color for the percentage text */
    font-size: 12px;
    border-radius: 3px;
    top: -28px;
    right: -20px;
    animation: showtext 0.5s 1.5s linear forwards; /* Delayed fade-in for the label */
    opacity: 0; /* Initially hidden */
}
.progress-line.html span::after{
    content: "95%"; /* Sets the content for HTML percentage */
}
.progress-line.css span::after{
    content: "80%"; /* Sets the content for CSS percentage */
}
.progress-line.javascript span::after{
    content: "75%"; /* Sets the content for JavaScript percentage */
}
.progress-line.react span::after{
    content: "80%"; /* Sets the content for React percentage */
}
.progress-line.node span::after{
    content: "70%"; /* Sets the content for Node.js percentage */
}
.progress-line.express span::after{
    content: "75%"; /* Sets the content for Express.js percentage */
}
.progress-line.mongodb span::after{
    content: "80%"; /* Sets the content for MongoDB percentage */
}
.progress-line.mysql span::after{
    content: "80%"; /* Sets the content for MySQL percentage */
}
.progress-line.c-basics span::after{
    content: "95%"; /* Sets the content for C Basics percentage */
}
.progress-line.java span::after{
    content: "85%"; /* Sets the content for Java percentage */
}
.progress-line.dsa span::after{
    content: "60%"; /* Sets the content for DSA percentage */
}
.progress-line.ai-ml-concepts span::after{
    content: "75%"; /* Sets the content for AI/ML Concepts percentage */
}
.progress-line.software-development span::after{
    content: "90%"; /* Sets the content for Software Development percentage */
}
.progress-line.salesforce span::after{
    content: "80%"; /* Sets the content for Salesforce percentage */
}
.progress-line span::before{
    content: "";
    position: absolute;
    width: 0;
    height: 0;
    border: 7px solid transparent;
    border-bottom-width: 0px;
    border-right-width: 0px;
    border-top-color: #000; /* Black color for the tooltip arrow */
    top: -10px;
    right: 0;
    animation: showtext 0.5s 1.5s linear forwards; /* Delayed fade-in for the arrow */
    opacity: 0; /* Initially hidden */
}
@keyframes animate{
    100%{
        transform: scaleX(1); /* Animates the width to 100% */
    }
}
@keyframes showtext{
    100%{
        opacity: 1; /* Fades in the text/arrow */
    }
}
* **section:** Sets the display to flex and flex-wrap: wrap. This is a general style for sections, likely used to arrange content within them. flex-wrap: wrap ensures that if the content exceeds the container width, it will wrap to the next line.
* **.container1:** This class specifically styles the container for the "Technical Skills" section. It has a fixed width and height, adds padding around the content, and sets a margin-left to position it on the page.
* **.heading1:** Styles the main heading within the "Skills" section (likely "Technical Skills"). It centers the text, adds an underline with a specific offset and thickness, and provides margin-bottom for spacing.
* **.bar:** This class likely represents a single skill bar. It sets a font-size, uses position: relative to allow absolute positioning of child elements, aligns items vertically using align-items: center (though in this context, it might not have a direct effect on inline elements), and adds margin-bottom for spacing between skill bars.
* **.Technical-bars .bar:** Applies specific top and bottom margins to the skill bars within the .Technical-bars container.
* **.Technical-bars .bar:first-child and .Technical-bars .bar:last-child:** Remove the top margin from the first skill bar and the bottom margin from the last skill bar to avoid extra spacing at the beginning and end of the list.
* **.Technical-bars .bar .info:** Adds margin-bottom to the container holding the skill name.
* **.Technical-bars .bar .info span:** Styles the skill name text. It sets the font-size and font-weight, applies a fade-in animation (showtext), and is initially hidden (opacity: 0).
* **.Technical-bars .bar .progress-line:** Styles the background track of the progress bar. It's relatively positioned, has rounded corners, a width of 100%, a fixed height, a black background-color, an animation (animate) to expand from left to right, and is initially scaled to 0 width from the left.
* **.Technical-bars .bar .progress-line span:** Styles the colored fill of the progress bar. It has 100% height, a cyan background-color, is absolutely positioned within the track, has rounded corners, a delayed animation (animate), and is also initially scaled to 0 width from the left.
* **.progress-line.html span to .progress-line.salesforce span:** These rules set the specific width of the cyan fill for each technical skill (HTML, CSS, JavaScript, etc.), representing the proficiency level.
* **.progress-line span::after:** Creates a pseudo-element to display the percentage value next to the progress bar. It's absolutely positioned, has padding, a black background, white text, a small font-size, rounded corners, is positioned above and to the right of the progress bar, and has a delayed fade-in animation.
* **.progress-line.html span::after to .progress-line.salesforce span::after:** These rules set the specific content (the percentage value) for each skill's percentage label.
* **.progress-line span::before:** Creates a pseudo-element to act as a small black arrow pointing down from the percentage label. It uses borders to create the triangle shape, is absolutely positioned above the progress bar, and also has a delayed fade-in animation.
* **@keyframes animate:** Defines the animation that expands the width of the progress bar fill from 0 to 100%.
* **@keyframes showtext:** Defines a simple fade-in animation by changing the opacity from 0 to 1.

### H. Portfolio Section Styles
.main-text{
    padding-top: 130px;
    margin-top: 980px; /* Large top margin, likely to position it below other sections */
}
.main-text h2{
    font-size: 60px;
    line-height: 1;
    text-align: center;
}
.main-text h2 span{
    color: #0ef; /* Cyan color for the span within the heading */
}
.portfolio-content{
    display: grid; /* Enables Grid layout */
    grid-template-columns: repeat(auto-fit, minmax(350px, auto)); /* Creates responsive columns with a minimum width of 350px */
}
.row{
    position: relative; /* Allows absolute positioning of the layer */
    overflow: hidden; /* Hides the layer when it extends beyond the row */
    border-radius: 8px;
    cursor: pointer; /* Changes cursor to indicate interactivity */
}
.row img{
    width: 90%;
    height: 60%;
    background: transform 0.5s; /* Note: 'background' property doesn't handle transitions directly, should be 'transition' */
    margin-top: 150px;
    margin-left: 25px;
    align-items: center; /* Might not have a direct effect on block-level images */
}
.layer{
    width: 100%;
    height: 0; /* Initially hidden */
    background: linear-gradient(rgba(16, 215, 254, 0.1),#0ef); /* Gradient background */
    border-radius: 8px;
    left:0;
    bottom: 0;
    overflow: hidden;
    display: flex; /* Enables Flexbox layout for content within the layer */
    flex-direction: column; /* Arranges items vertically */
    align-items: center; /* Centers items horizontally */
    justify-content:center; /* Centers items vertically */
    text-align: center;
    padding: 0 40px;
    transition: height 0.5s; /* Smooth transition for height changes on hover */
}
.layer h5{
    color: #000; /* Black color for the project title */
    font-size: 20px;
    font-weight: 600;
    margin-top: 100px; /* Pushes the title down when the layer appears */
}
.layer p{
    color: #000; /* Black color for the project description */
    font-size: 1rem;
    line-height: 1.8;
    margin-bottom: 30px;
}
.layer i {
    color: #ff004f; /* Pink/red color for the link icon */
    margin-top: 20px;
    font-size: 20px;
    background: #fff; /* White background for the icon */
    width: 60px;
    height: 60px;
    display: flex; /* Centers the icon */
    align-items: center;
    justify-content: center;
    border-radius: 50%; /* Circular shape for the icon background */
}
.row:hover img{
    transform: scale(1.1); /* Slightly zooms in the image on hover */
    height: 25%; /* Reduces the image height on hover, making space for the layer */
}
.row:hover .layer{
    height: 40%; /* Reveals the layer on hover */
}
* **.main-text:** Styles the main heading area for the "Portfolio" section. It adds a significant padding-top and margin-top, likely to position the heading below the preceding sections.
* **.main-text h2:** Styles the main title of the "Portfolio" section, setting a large font-size, a tight line-height, and centering the text.
* **.main-text h2 span:** Styles the <span> element within the title, setting its color to cyan (#0ef) for emphasis.
* **.portfolio-content:** This class uses CSS Grid to create a responsive layout for the portfolio project items. repeat(auto-fit, minmax(350px, auto)) ensures that there will be as many columns as can fit with a minimum width of 350px, and the columns will expand to fill the available space.
* **.row:** Represents a single portfolio project item.
* **position: relative;:** Sets the positioning context for the .layer element, allowing it to be absolutely positioned within the .row.
* **overflow: hidden;:** Ensures that when the .layer appears (by increasing its height), it doesn't cause scrollbars or overflow the .row boundaries.
* **border-radius: 8px;:** Rounds the corners of the project item.
* **cursor: pointer;:** Changes the mouse cursor to a pointer on hover, indicating that the element is interactive.
* **.row img:** Styles the image associated with each portfolio project.
* **width: 90%; height: 60%;:** Sets the initial width and height of the image within its container.
* **background: transform 0.5s;:** Note: This line is likely incorrect. The background property doesn't handle transitions. It should probably be transition: transform 0.5s; to create a smooth transition when the image is scaled on hover.
* **margin-top: 150px; margin-left: 25px;:** Adds top and left margins to position the image within the .row.
* **align-items: center;:** This property is typically used in Flexbox or Grid layouts to align items along the cross axis. It might not have a direct visual effect on a block-level <img> element in this context.
* **.layer:** This element acts as an overlay that appears on hover to provide more information about the project.
* **width: 100%; height: 0;:** Sets the initial width to full and the height to 0, making it initially hidden.
* **background: linear-gradient(rgba(16, 215, 254, 0.1),#0ef);:** Applies a linear gradient as the background, starting with a very transparent cyan and transitioning to a solid cyan.
* **border-radius: 8px;:** Rounds the corners to match the .row.
* **left: 0; bottom: 0;:** Positions the layer at the bottom-left of its .row container (due to position: absolute in .layer and position: relative in .row).
* **overflow: hidden;:** Ensures that any content within the layer that exceeds its bounds is hidden.
* **display: flex; flex-direction: column; align-items: center; justify-content: center; text-align: center;:** Uses Flexbox to arrange the content within the layer vertically and centers it both horizontally and vertically. The text is also centered.
* **padding: 0 40px;:** Adds left and right padding to the content within the layer.
* **transition: height 0.5s;:** Creates a smooth transition for the height property when it changes (on hover).
* **.layer h5:** Styles the project title within the .layer, setting the text color to black, a specific font size and weight, and adding a margin-top to push it down when the layer becomes visible.
* **.layer p:** Styles the project description within the .layer, setting the text color to black, a font size of 1rem, and a line-height for readability, along with a bottom margin.
* **.layer i:** Styles the icon (likely a link icon) within the .layer. It sets a pink/red color, a font size, a white background, fixed width and height to create a circular shape (due to border-radius: 50%), and uses Flexbox to center the icon within its circular background.
* **.row:hover img:** Styles the image within the .row on hover. It scales the image up slightly (transform: scale(1.1)) and reduces its height to 25%, making space for the .layer to become more visible.
* **.row:hover .layer:** Styles the .layer on hover of the .row, increasing its height to 40%, thus revealing the project information.

### I. Contact Section Styles (`.contact`, `.contact-text h1`, `.contact-text h1 span`, `.contact-text h4`, `.contact-text p`, `.contact-list`, `.contact-list li`, `.contact-list i`, `.contact-list li a:hover`, `.contact-icons i`, `.contact-icons i:hover`, `.contact-form form`, `.contact-form form input`, `.contact-form form textarea`, `.contact-form form .send`, `.contact-form form .send:hover`)
This CSS styles the "Contact" section of the portfolio, providing a layout for contact information and a form for direct communication.

* **`.contact`**: Sets up a two-column grid layout (`display: grid; grid-template-columns: repeat(2,1fr)`) for the contact information and the contact form. It vertically aligns the items in the grid (`align-items: center`), adds a `gap` between the columns, and includes `padding-left` and `margin-top` for spacing.
* **`.contact-text h1`**: Styles the main heading of the contact information area, setting a large `font-size`, a tight `line-height`, and a small `margin-left`.
* **`.contact-text h1 span`**: Styles the `<span>` element within the contact heading, setting its `color` to cyan (`#0ef`) for emphasis.
* **`.contact-text h4`**: Styles a subheading within the contact information, setting `margin`, a light gray `color`, a `font-size`, and `font-weight`, along with a `margin-left`.
* **`.contact-text p`**: Styles the paragraph text in the contact information, setting a grayish `color`, `font-size`, `line-height`, `margin-bottom`, and `margin-left` for readability and spacing.
* **`.contact-list`**: Styles an unordered list (`<ul>` or `<ol>`) containing contact details, adding `margin-bottom` for spacing.
* **`.contact-list li`**: Styles each list item, adding `margin-bottom` for vertical spacing and setting `display: block`.
* **`.contact-list i`**: Styles the icons within the contact list items, setting an inline-block display, cyan `color`, `font-size`, `font-weight`, applying a smooth transition (`transition: all .40s ease`), and adding a `margin-left`.
* **`.contact-list li a:hover`**: Styles the hover effect for links within the contact list items, applying a series of cyan box shadows to create a glowing effect.
* **`.contact-icons i`**: Styles the social media icons. They are displayed as inline-flex containers to center their content, have fixed `width` and `height` for a circular shape (due to `border-radius: 50%`), a transparent `background`, a cyan `border`, a `font-size`, cyan `color`, no text decoration, `margin-left` and `margin-bottom` for spacing, a smooth transition, and are initially hidden (`opacity: 0`) with a slide-in animation from the left (`@keyframes slideLeft` with a staggered delay).
* **`.contact-icons i:hover`**: Styles the hover effect for the social media icons, changing the `background` to cyan, the `color` to black, and adding a cyan box shadow.
* **`.contact-form form`**: Sets the positioning context to `relative` for the form.
* **`.contact-form form input, form textarea`**: Styles the input fields and the textarea within the contact form. They have no border or outline.

### J. Footer and Back-to-Top Styles (`.last-text p`, `.top`, `.top i`)
These styles define the appearance of the footer text and the "back to top" button.
* **`.last-text p`**: Styles the paragraph element that likely contains the copyright or other footer text. It sets the `width` to 100% to span the container, centers the text (`text-align: center`), adds `padding` at the top and bottom, sets the `background-color` to a light cyan (`rgb(0, 213, 255)`), applies a light `font-weight`, and adds `margin-top` for spacing from the preceding content.
* **`.top`**: Styles the container for the "back to top" button. It uses `position: fixed` to keep it in a consistent location on the screen even when scrolling, positions it `2.1rem` from the bottom and right edges of the viewport.
* **`.top i`**: Styles the icon (likely an arrow) within the "back to top" button. It sets the `color` to black, the `background-color` to cyan (`#0ef`), a `font-size` of `20px`, adds `padding` around the icon, and applies a `border-radius` for slightly rounded corners.

### K. Keyframe Animations (`@keyframes slideRight`, `@keyframes slideLeft`, `@keyframes slideTop`, `@keyframes slideBottom`)
These CSS `@keyframes` rules define animations used throughout the portfolio for various elements, creating entrance or movement effects.
* **`@keyframes slideRight`**: Animates an element to slide in from the left. At `0%` of the animation, the element is translated `100px` to the left and is fully transparent (`opacity: 0`). At `100%`, it's translated to its original horizontal position (`0px`) and becomes fully visible (`opacity: 1`).
* **`@keyframes slideLeft`**: Animates an element to slide in from the right. At `0%`, it's translated `100px` to the right and is transparent. At `100%`, it's at its original horizontal position and fully visible.
* **`@keyframes slideTop`**: Animates an element to slide in from the bottom. At `0%`, it's translated `100px` downwards and is transparent. At `100%`, it's at its original vertical position and fully visible.
* **`@keyframes slideBottom`**: Animates an element to slide in from the top. At `0%`, it's translated `100px` upwards and is transparent. At `100%`, it's at its original vertical position and fully visible.
These animations are used to add subtle and engaging visual effects as different parts of the portfolio load or become interactive.






### 3. JavaScript (`main.js` and Inline `<script>` Tags)
The JavaScript code adds dynamic behavior and interactivity to the website. The provided code snippet in the prompt directly demonstrates the use of the Typed.js library:
var typed = new Typed(".text", {
  strings: ["Data Science Enthusiast", "Salesforce Administrator","Software Developer", "Full Stack Web Developer","Salesforce Architect" ],
  typeSpeed: 100,
  backSpeed: 100,
  backDelay: 1000,
  loop: true
});
* **var typed = new Typed(".text", { ... });:** This line initializes the Typed object, which is the core of the Typed.js library. It targets the HTML element with the class name .text. In the index.html file, this class is applied to a <span> element within the "Home" section:
<h3>And I'm a <span class="text"></span></h3>
This <span> is where the animated text will be displayed.
  
* **strings:** ["Data Science Enthusiast", "Salesforce Administrator","Software Developer", "Full Stack Web Developer","Salesforce Architect" ]: This array defines the sequence of strings that will be typed and backspaced in the animation. The library will cycle through these roles.

* **typeSpeed: 100:** This property sets the speed at which characters are typed, measured in milliseconds per character. A value of 100 means each character will appear after a 100-millisecond delay.

* **backSpeed: 100:** This property sets the speed at which characters are backspaced (deleted), also in milliseconds per character. A value of 100 means each character will be deleted after a 100-millisecond delay.

* **backDelay: 1000:** This property specifies the delay in milliseconds before the backspacing begins after a string has been fully typed. A value of 1000 means there will be a 1-second pause before the text starts to be deleted.

* **loop: true:** This boolean property determines whether the animation should loop continuously. Setting it to true will make the typing and backspacing sequence repeat indefinitely.
This JavaScript code, likely placed within a <script> tag in the index.html file (either inline or within the linked main.js), is responsible for the dynamic and engaging introduction on the homepage, effectively highlighting my diverse skill set and areas of expertise.
The main.js file might contain additional JavaScript code to handle other interactive elements on the website, such as form submissions, dynamic updates to the skills section (especially the radial progress bars), or the functionality of the back-to-top button.

* **Potential Improvements and Considerations**
Responsiveness: Ensure the stylesheet.css includes comprehensive media queries to provide an optimal viewing experience across various screen sizes (desktops, tablets, and mobile devices).
Accessibility: Implement ARIA attributes and follow accessibility best practices to make the website usable for individuals with disabilities.
Image Optimization: Optimize all images in the assets/ directory (if present) to reduce file sizes and improve page loading times.
Code Organization: For larger projects, consider further modularizing CSS and JavaScript for better maintainability.
Form Handling: Implement a server-side script or integrate a form submission service to process the data submitted through the contact form.
JavaScript for Radial Bars: The dynamic filling of the professional skills radial bars likely requires JavaScript to manipulate the SVG elements based on the percentage values. This logic would typically reside in main.js.
Navigation Active State: While the initial "Home" link has the active class, JavaScript could be used to dynamically update this class as the user scrolls to different sections of the page, providing better visual feedback.
Contributing
If you have any suggestions or find issues with the website, feel free to open an issue or submit a pull request.

License
This project is licensed under the MIT License - see the LICENSE file for details.

Author
Pranjal Khandelwal
LinkedIn:  https://www.linkedin.com/in/pranjal-khandelwal-1a46682a4/
GitHub:  https://github.com/golu19102003
Twitter:  https://x.com/Pranjal76009498
Facebook:  https://www.facebook.com/profile.php?id=100095370905135
Instagram:  https://www.instagram.com/pranjal19102003_2.0/
