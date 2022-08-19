## Production Deployment Checklist

In Black magic we are guided by a list of tasks that we carry out before launching a site to the final server

**Schedule Date | Time**

 - Set and Test Environments
   
 - Backups Content

 - Launch Production

  

**Client Hosting | Domain Info**

 - Client Domain Provider
 
 - Access Credentials

- If Domain and Host Service are not in the same place:

- DNS Records (or admin account access to generate them)

  

**Environments**

- Create Staging & Production Environments: Client Staging will be the test domain before release to production.

- Redirects: Check the old hosted site if it exists, check what would be the corresponding page on the site that will be currently hosted.

- SSL Certificate: SSL is a type of certificate that helps to make websites more secure by ensuring that the contents of a packet of data don’t get read until it gets to its designated reader (the user).

- Think of your website as your house and by installing alarms (or SSL), you’re adding an extra layer of security to protect from hackers. This is important for SEO. The more secure your website, the higher it will rank on Google. So the more secure your house, the better.

  
**Backups**

- Craft CMS complete project backup and updated database

- backupOnUpdate config file

**SEO**

- Craft CMS: SEO Plugin + Tags

- Install SEO plugin and make the corresponding settings (Create an SEO field and in each section where it is necessary to place it in a tab that says SEO).

- Schema: Configure the schema file that the site will need, you can find documentation on schema.org.

- Robots.txt: In case the site is made in Craft CMS, when making the configuration in SEO plugin the robots will already be working.

- OpenGraph Image: This image is configured in the SEO plugin, entering the route: admin/seo/settings in the field: Default Social Image.

  
  
**Client Final Content**

- Favicon: Add the assets related to the favicon and the configuration so that it can be seen in the frontend.

- Typography Licensing: The license of the fonts in case it is necessary.

- CMS + Plugins Licenses + 3rd Party Services Subscriptions/Licenses: The licenses of the plugins in the case of being plugins pags.

- Sherlock Security: Una vez el sitio esté en producción instalar Sherlock Security Plugin.

  

**API Keys:**

- Image Optimization: Make sure that the images are properly optimized for the good performance of the site, that they contain descriptive alts for the user, that they are mostly in webp format, that their measurements are adequate as well as their weight.

- Contact Forms Submissions Testing (SMTP Info: host, username, password, port, encryption method (tls/ssl)): Access client SMTP accounts for final form configuration.

- Contact Form Captcha: Generate the Captcha of the form.

- Google Analytics Script (+ Reporting): Make sure the site takes Google Analytics if required.

  

**Testing**

  
 - Google Lighthouse Testing: Testing for accessibility.

- Google Pagespeed: Link to test performance with the google tool.

- Google Lighthouse Performance Testing Testing for performance.

- Accessibility Testing: Test more accurately the accessibility of the page with screen readers and making sure that everything focusable works with the keyboard.

- Browser Testing: Making sure that the web page looks good is different types of browsers such as: Google Chrome, Safari, Firefox...

- Check for possible CORS errors:

- Old Site Backups: Make a backup of the old site in case there is one.

- Utility Pages: 404, Site Down, Coming Soon, Privacy: Pages that normally go, just make sure they are on the web page.

- Credits: "Site By Black Magic": Normally we put the credits in the frontend of the footer indicating who made the design and development of the web, when the client does not want it to be seen, we insert an ascci code script so that the credits can be seen in the console.

- Cookies Banner: Make sure that the website has a cookie banner.

- CMS Training: It is the final stretch when the client is taught to use the CMS.

- Sign-off Document: It is practically the contract that the client is made to sign.

[Return](../README.md)