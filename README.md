# new-project
Study Abroad Website Only Forntend



/* --- Global Styles & Resets --- */
*,
*::before,
*::after {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

:root {
    /* Define primary colors */
    --primary-color: #007bff; /* A nice blue for primary actions */
    --secondary-color: #6c757d; /* A subtle grey for secondary actions */
    --tertiary-color: #28a745; /* A green for tertiary actions/highlights */
    --dark-bg: #1a1a1a;
    --light-text: #ffffff;
    --dark-text: #333333;
    --overlay-dark: rgba(0, 0, 0, 0.7);
    --overlay-light: rgba(255, 255, 255, 0.9);
    --border-radius: 8px;
    --transition-speed: 0.3s ease;
}

body {
    font-family: 'Manrope', sans-serif;
    background-color: var(--dark-bg);
    color: var(--light-text);
    line-height: 1.6;
    scroll-behavior: smooth; /* Smooth scrolling for anchor links */
}

/* --- Utility Classes --- */
.container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 20px;
}

/* --- Header & Hero Section --- */
.header-hero {
    height: 100vh;
    background-image: url("london.jpg"); /* Main hero background */
    background-size: cover;
    background-position: center center;
    background-attachment: fixed;
    display: flex;
    flex-direction: column; /* Stack logo/nav and hero text */
    justify-content: space-between; /* Push nav to top, hero text to middle */
    align-items: center;
    text-align: center;
    color: var(--light-text);
    position: relative; /* For overlay */
}

.header-hero::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background-color: var(--overlay-dark); /* Dark overlay for text readability */
    z-index: 1; /* Ensure overlay is behind content */
}

.header-content {
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center; /* Center content vertically */
    flex-grow: 1; /* Allows it to take available space */
    position: relative; /* Above overlay */
    z-index: 2;
}

.logo {
    font-size: 2.5em;
    font-weight: 800;
    margin-bottom: 20px;
    color: var(--light-text);
    text-shadow: 3px 3px 6px rgba(0, 0, 0, 0.8);
    position: absolute; /* Position logo independently */
    top: 20px;
    left: 50%;
    transform: translateX(-50%);
    width: 100%;
    max-width: fit-content;
}

.main-nav {
    position: absolute; /* Position navigation independently */
    top: 20px;
    right: 20px;
    z-index: 10;
}

.main-nav ul {
    list-style: none;
    display: flex;
    gap: 25px; /* Spacing between nav items */
}

.main-nav a {
    color: var(--light-text);
    text-decoration: none;
    font-weight: 600;
    font-size: 1.1em;
    padding: 5px 0;
    transition: color var(--transition-speed);
}

.main-nav a:hover,
.main-nav a:focus {
    color: var(--primary-color);
}

.hero-text {
    max-width: 800px;
    padding: 0 20px;
    margin-top: 100px; /* Space from logo/nav */
}

.hero-text h2 {
    font-size: 3.5em;
    margin-bottom: 20px;
    font-weight: 700;
    text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.7);
}

.hero-text p {
    font-size: 1.5em;
    margin-bottom: 40px;
    max-width: 600px; /* Limit paragraph width */
    margin-left: auto;
    margin-right: auto;
    background-color: transparent; /* No background for hero text p */
    padding: 0;
    line-height: 1.5;
}

/* --- General Section Styles --- */
.info-section {
    padding: 80px 20px;
    text-align: center;
    background-color: var(--dark-bg);
    color: var(--light-text);
}

.alternate-bg {
    background-color: #2c2c2c; /* Slightly lighter dark background */
}

.section-title {
    font-size: 2.8em;
    margin-bottom: 25px;
    font-weight: 700;
    color: var(--primary-color);
}

.section-description {
    font-size: 1.2em;
    max-width: 900px;
    margin: 0 auto 30px auto;
    line-height: 1.8;
}

/* --- Banner Sections (Full-width images) --- */
.main_container.study-abroad-section,
.main_container.country-focus-section,
.main_container.growth-section,
.main_container.dream-choice-section {
    height: 60vh; /* Shorter height for these internal banners */
    background-repeat: no-repeat;
    background-position: center center;
    background-attachment: fixed;
    background-size: cover; /* All banners cover */
    display: flex;
    justify-content: center;
    align-items: center;
    position: relative;
    padding: 20px;
    overflow: hidden; /* Prevent content overflow */
}

/* Overlay for banner sections */
.main_container.study-abroad-section::before,
.main_container.country-focus-section::before,
.main_container.growth-section::before,
.main_container.dream-choice-section::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background-color: var(--overlay-dark);
    z-index: 1;
}

.main_container .heading {
    position: relative;
    z-index: 2;
}

.main_container .heading h1 {
    font-size: 3.5em;
    color: var(--light-text);
    text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.7);
    padding: 0; /* Remove default h1 padding here */
}


/* Individual Banner Images */
.study-abroad-section {
    background-image: url("america.jpg"); /* Or a general study image */
}

.country-focus-section {
    background-image: url("newzeland.jpg");
}

.growth-section {
    background-image: url("canda.jpg");
}

.dream-choice-section {
    background-image: url("japan.jpg");
}

/* --- Country Details Section --- */
.country-details {
    padding: 60px 20px;
    border-bottom: 1px solid rgba(255, 255, 255, 0.1);
}

.country-details:last-of-type {
    border-bottom: none; /* No border for the last one */
}

.country-name {
    font-size: 2.2em;
    margin-bottom: 15px;
    color: var(--tertiary-color); /* Green for country names */
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 15px; /* Space between text and icon */
}

.country-name .fas, .country-name .fab {
    font-size: 0.9em; /* Adjust icon size relative to text */
    color: var(--primary-color);
}

.country-description {
    font-size: 1.1em;
    max-width: 800px;
    margin: 0 auto;
    background-color: transparent; /* No background for these paragraphs */
    padding: 0;
}

/* --- Call To Action Section --- */
.cta-section {
    background-color: var(--primary-color); /* Highlight CTA section */
    color: var(--light-text);
    padding: 80px 20px;
}

.cta-section .section-title {
    color: var(--light-text); /* Ensure title is white on blue background */
    margin-bottom: 20px;
}

/* --- Buttons --- */
.btn {
    display: inline-block;
    padding: 15px 30px;
    border-radius: var(--border-radius);
    text-decoration: none;
    font-weight: 600;
    transition: background-color var(--transition-speed), transform var(--transition-speed);
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
    margin-top: 20px; /* Space below descriptions */
}

.btn-primary {
    background-color: var(--primary-color);
    color: var(--light-text);
    border: 2px solid var(--primary-color);
}

.btn-primary:hover {
    background-color: darken(var(--primary-color), 10%); /* Requires Sass/Less, use a specific hex for plain CSS */
    background-color: #0056b3; /* A darker blue */
    transform: translateY(-3px);
}

.btn-secondary {
    background-color: transparent;
    color: var(--primary-color);
    border: 2px solid var(--primary-color);
}

.btn-secondary:hover {
    background-color: var(--primary-color);
    color: var(--light-text);
    transform: translateY(-3px);
}

.btn-tertiary {
    background-color: var(--tertiary-color);
    color: var(--light-text);
    border: 2px solid var(--tertiary-color);
    padding: 10px 25px; /* Slightly smaller for country links */
    font-size: 0.9em;
}

.btn-tertiary:hover {
    background-color: darken(var(--tertiary-color), 10%); /* Use #218838 */
    background-color: #218838;
    transform: translateY(-2px);
}

.btn-large {
    padding: 20px 40px;
    font-size: 1.3em;
}

/* --- Footer --- */
.footer-section {
    background-color: #0a0a0a; /* Very dark background for footer */
    padding: 60px 20px 30px;
    color: #cccccc;
    text-align: center;
}

.footer-content {
    display: flex;
    flex-wrap: wrap; /* Allow columns to wrap on smaller screens */
    justify-content: space-around;
    gap: 30px;
    margin-bottom: 40px;
}

.footer-col {
    flex: 1; /* Allow columns to grow */
    min-width: 250px; /* Minimum width before wrapping */
    max-width: 300px;
    text-align: left;
}

.footer-col h3 {
    color: var(--primary-color);
    font-size: 1.6em;
    margin-bottom: 20px;
    font-weight: 600;
}

.footer-col p, .footer-col ul li {
    font-size: 0.95em;
    margin-bottom: 10px;
}

.footer-col ul {
    list-style: none;
}

.footer-col ul li a {
    color: #cccccc;
    text-decoration: none;
    transition: color var(--transition-speed);
}

.footer-col ul li a:hover {
    color: var(--primary-color);
}

.footer-col p .fas {
    margin-right: 10px;
    color: var(--tertiary-color);
}

.social-links {
    margin-top: 20px;
}

.social-links a {
    display: inline-block;
    width: 40px;
    height: 40px;
    line-height: 40px;
    background-color: #333;
    color: var(--light-text);
    margin: 0 10px;
    border-radius: 50%;
    text-align: center;
    font-size: 1.2em;
    transition: background-color var(--transition-speed);
}

.social-links a:hover {
    background-color: var(--primary-color);
}

.footer-bottom {
    border-top: 1px solid rgba(255, 255, 255, 0.1);
    padding-top: 20px;
    margin-top: 20px;
    font-size: 0.9em;
    color: #aaaaaa;
}

/* --- Responsive Design (Basic) --- */
@media (max-width: 992px) {
    .hero-text h2 {
        font-size: 2.8em;
    }

    .section-title {
        font-size: 2.2em;
    }

    .main_container .heading h1 {
        font-size: 2.8em;
    }

    .country-name {
        font-size: 1.8em;
    }

    .footer-content {
        flex-direction: column;
        align-items: center;
    }

    .footer-col {
        text-align: center;
        max-width: none;
        width: 100%;
    }
}

@media (max-width: 768px) {
    .main-nav {
        top: 80px; /* Move nav below logo */
        right: 0;
        left: 0;
        text-align: center;
    }

    .main-nav ul {
        justify-content: center;
        gap: 15px;
    }

    .hero-text h2 {
        font-size: 2.2em;
    }

    .hero-text p {
        font-size: 1.2em;
    }

    .section-title {
        font-size: 1.8em;
    }

    .section-description {
        font-size: 1em;
    }

    .main_container .heading h1 {
        font-size: 2.2em;
    }

    .country-name {
        font-size: 1.5em;
    }

    .btn {
        padding: 12px 25px;
        font-size: 0.95em;
    }

    .btn-large {
        padding: 15px 30px;
        font-size: 1.1em;
    }
}

@media (max-width: 480px) {
    .logo {
        font-size: 2em;
        top: 15px;
    }

    .main-nav {
        top: 60px; /* Adjust nav position for smaller screens */
    }

    .main-nav ul {
        flex-direction: column;
        gap: 10px;
    }

    .hero-text h2 {
        font-size: 1.8em;
    }

    .hero-text p {
        font-size: 1em;
    }

    .section-title {
        font-size: 1.5em;
    }

    .main_container .heading h1 {
        font-size: 1.8em;
    }

    .country-name {
        font-size: 1.3em;
        flex-direction: column; /* Stack icon and text */
        gap: 5px;
    }

    .country-name .fas, .country-name .fab {
        font-size: 1em;
    }

    .footer-col {
        min-width: unset;
        width: 100%;
    }
}
