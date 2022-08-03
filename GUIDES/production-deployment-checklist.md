## Production Deployment Checklist
In Black Magic we are guided by a list of tasks that we carry out before launching a site to the final server

 - ***Launch Schedule (Date + Time):*** Date the project will launch.
 - ***Hosting + Domain Info:***  Information that will be the domain of the client with the accesses to be able to host the site in that domain.
 - ***Create Staging & Production Environments:*** Staging will be the test domain before release to production.
 - ***Redirects:*** Check old hosted site if it exists, check what would be the corresponding page on the site that will be currently hosted.
 - ***Meta Data:*** 
 - ***SSL Certificate:*** 
 - ***SEO Plugin + Tags:*** In the case of craft, install the [SEO](https://plugins.craftcms.com/seo) plugin and make the corresponding settings (Create an SEO field and in each section where it is necessary to place it in a tab that says SEO).
 -  ***Schema:*** Configure the schema file that the site will need, you can find documentation on [shema.org](https://schema.org/docs/about.html).
 - ***Robots.txt:*** In case the site is made in Craft CMS, when making the configuration in SEO plugin the robots will already be working.
 - ***OpenGraph Image:*** This image is configured in the SEO plugin, entering the route: `admin/seo/settings` in the field: *Default Social Image*.
 - ***Favicon:*** Add the assets related to the favicon and the configuration so that it can be seen in the frontend.
 - ***Typography Licensing:*** The license of the fonts in case it is necessary.
 - ***CMS + Plugins Licenses + 3rd Party Services Subscriptions/Licenses:***  The licenses of the plugins in the case of being plugins pags.
 - ***Sherlock Security:*** Una vez el sitio esté en production instalar  [Sherlock](https://plugins.craftcms.com/sherlock?craft4) Security Plugin.
 - ***API Keys:***
 - ***Image Optimization:*** Make sure that the images are properly optimized for the good performance of the site, that they contain descriptive alts for the user, that they are mostly in webp format, that their measurements are adequate as well as their weight.
 - ***Contact Forms Submissions Testing (SMTP Info: host, username, password, port, encryption method (tls/ssl)):*** Access client SMTP accounts for final form configuration.
 - ***Contact Form Captcha:*** Generate the [Captcha](https://www.google.com/recaptcha/about/) of the form.

 - ***Google Analytics Script (+ Reporting):*** Make sure the site takes Google Analytics if required.
 - ***Google Lighthouse Testing:*** Testing for accessibility.
 - ***Google Pagespeed:*** Link to test performance with the google tool.
 - ***Google Lighthouse Performance Testing*** Testing for performance.
 - ***Accessibility Testing:*** Test more accurately the accessibility of the page with screen readers and making sure that everything focusable works with the keyboard.
 - ***Browser Testing:*** Making sure that the web page looks good is different types of browsers such as: Google Chrome, Safari, Firefox...
 - ***Check for possible CORS errors:***
 - ***Old Site Backups:*** Make a backup of the old site in case there is one.
 - ***Utility Pages: 404, Site Down, Coming Soon, Privacy:*** Pages that normally go, just make sure they are on the web page.
 - ***Credits: "Site By Black Magic":*** Normally we put the credits in the frontend of the footer indicating who made the design and development of the web, when the client does not want it to be seen, we insert an ascci code script so that the credits can be seen in the console.
 - ***Cookies Banner:*** Make sure that the website has a cookie banner.
 - ***CMS Training:*** It is the final stretch when the client is taught to use the CMS.
 - ***Deliver Credentials:*** ???
 - ***Sign-off Document:*** It is practically the contract that the client is made to sign.

[Return](../README.md)