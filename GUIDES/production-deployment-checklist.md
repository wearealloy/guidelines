# Production Deployment Checklist

Here’s a comprehensive list of tasks that we carry out before launching a website to the client’s Production server:

### Launch Schedule

 1. Always ask for launch (**date** and **time)**  .
2. We don’t launch websites on Fridays.

### Hosting & Domain Info
 1. Who is the client’s current **hosting** provider?
	- **1 .**  GoDaddy.
	- **2 .**  Bluehost.
	- **3 .**  HostGator.
	- **4 .** Hostinger.
	- **5 .** IONOS.
	- **6 .** Network Solutions...
 2. Who is the client’s current **domain** provider?  
 3. For the new site, is the client moving to a new hosting or domain provider?  
 4. Gather the client’s hosting and domain credentials and save them in LastPass  .
 5. Access Credentials
 6. **Point Domain + DNS Propagation:**
      - **1 .** If Domain and Host Service are not in the same place: DNS Records (or admin account access to generate them). Point DNS to the new domain

### Environments
 
 1. **Black Magic Staging:** Black Magic always creates a staging environment where we will do the full development and testing of the website.
    - The URL to Black Magic’s staging website is usually [clientname.heyblackmagic.com](http://clientname.heyblackmagic.com/)  
2. **Client’s Staging:** The client’s staging environment will be used to test domain before release to production. 
3. **Client’s Production** The client's Production site.

### Security

 1. **SSL Certificate:** SSL is a type of certificate that helps to make websites more secure by ensuring that the contents of a packet of data don’t get read until it gets to its designated reader (the user) . Think of your website as your house and by installing alarms (or SSL), you’re adding an extra layer of security to protect from hackers. This is important for SEO. The more secure your website,  the higher it will rank on Google. So the more secure your house, the better.
 
 2.  **Sherlock Security:** Once the site is in production install Sherlock Security Plugin [Sherlock Security Plugin](about:blank).

### Backups

For projects with a previous live site, we require access to those files on the server to make a backup of that previous site.
[Craft CMS](https://craftcms.com/), [Wordpress](https://wordpress.com/), or any CMS inherited proyect. Complete site backup and latest updated database.

### SEO

 1. We normally use plugins from Craft CMS : 
     - **1 .** [SEOmatic Plugin](https://plugins.craftcms.com/seomatic?craft4).
	  -   **2 .** [SEO Plugin](http://craft3.lexington-market.test/admin/plugin-store/seo).
	  -   **3 .**   Install **SEO Plugin** and make the corresponding settings (Create an SEO field and in each section where it is necessary to place it in a tab that says SEO).
2. **Tags**.
3. **Schema**: Configure the schema file that the site will need, you can find documentation on [schema.org](https://schema.org/).
4. **Robots.txt:** In case the site is made in Craft CMS, when making the configuration in SEO plugin the robots will already be working.
5.  **OpenGraph Image:** This image is configured in the SEO plugin, entering the route:
`admin/seo/settings` in the field: ***Default Social Image***.
4. **Redirects:** Check the old hosted site if it exists, check what would be the corresponding page on the site that will be currently hosted.

### Client Final Content

1. **Favicon:** 
  - Add all optimized **.ico, .png** favicon assets in every recomended sizes for all browsers and devices. This assests can be provided by client, so we just need add files in proyect's directory ```/assets/favicon/```.
  - If required assets have not been provided, we can generate them with [favicomatic](https://favicomatic.com/) only with an image icon created by us.

2. **Typography:** 
  - Web Fonts Files
    - ```.woff .woff2 .ttf .eot``` for ```@font-face```.
  - Typekit 
    - Create Web Project in Adobe Fonts, activate OpenType Features checkbox and set ```font-display: swap```. Paste final ```<link rel="stylesheet"...``` code into ```<head>``` or paste kit.css url into ```<script src=" "...``` tag.

4. **Image Optimization:** 
  - Make sure that the images are properly optimized for the good performance of the site, that they contain descriptive alts for the user, that they are mostly in webp format, that their measurements are adequate as well as their weight.
  - **Some tools used in Black Magic for image optimization are:**
    -  **1.**  [Image Transform](https://craftcms.com/docs/3.x/image-transforms.html) Craft CMS Tool.
	- **2.** [Optimize Tool for images](https://www.optimizeimages.com/tool).
	-  **3.** **Lazy Loading:** [Example](https://afarkas.github.io/lazysizes/index.html) and [Documentation Repository](https://github.com/aFarkas/lazysizes).


5. **CMS + Plugins Licenses + 3rd Party Services Subscriptions/Licenses:**
  -  Client final licenses for paid plugins or services set with blackmagic test accounts or services in trial period.

### API Keys
	 
 1. **Contact Forms Submissions Testing** (SMTP Info: host, username, password, port, encryption method (tls/ssl)): Access client SMTP accounts for final form configuration.
 2. **Contact Form Captcha:** Generate the Captcha of the form.
 3. **Google Analytics Script (+ Reporting):** Make sure the site takes Google Analytics if required.

### Testing

 1. **Google Lighthouse Testing:** Lighthouse is an open-source, automated tool for improving the accessibility, performance, quality, and correctness of your web apps. 
When auditing a page, Lighthouse runs a barrage of tests against the page, and then generates a report on how well the page did. From here you can use the failing tests as indicators on what you can do to improve your app


      - **1.** [Quick-start guide on using Lighthouse](https://chrome.google.com/webstore/detail/lighthouse/blipmdconlkpinefehnmjammfjpmpbjk?hl=es).
     - **2.** View your reports online in [Lighthouse Report Viewer](https://googlechrome.github.io/lighthouse/viewer/) (Extension Tool) or in Developers Tools.
 2.   **Google PageSpeed:** Link to test performance with the google tool, [PageSpeed Insights](https://pagespeed.web.dev/).
 3. **Accessibility Testing:** Test more accurately the accessibility of the page with screen readers and making sure that everything focusable works with the keyboard and Screen Readers.
 4. **Browser Testing:** Making sure that the web page looks good is different types of browsers such as: Google Chrome, Safari, Firefox...
 5. Check for possible **CORS errors**.
 6. **Old Site Backups:** Make a backup of the old site in case there is one.
 7. **Utility Pages:**
	  - **1.** 404.
	 - **2.** Site Down.
	 - **3.** Coming Soon.	
	-  **3.** **Privacy Policy:** Pages that normally go, just make sure they are on the web page.
8.  **Credits:** "***Site By Black Magic***" Normally we put the credits in the frontend of the footer indicating who made the design and development of the web, when the client does not want it to be seen, we insert an ascci code script so that the credits can be seen in the console.
9.  **Cookies Banner:** Make sure that the website has a cookie banner.
10. **CMS Training:** It is the final stretch when the client is taught to use the CMS.
11. **Sign-off Document:** It is practically the contract that the client is made to sign.

### Deliver Info

      - 1. **Deliver Credentials**.

[Return](../README.md)