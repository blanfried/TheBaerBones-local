# Your Website - Processed & Ready for Netlify

Congratulations! Your website has been processed and is ready for a professional deployment on Netlify. This document contains critical information about the features that have been enabled.

---

## File Structure & Clean URLs (netlify.toml)

To provide a professional user experience, your site has been configured to use "clean URLs" (e.g., `yoursite.com/about` instead of `yoursite.com/pages/about.html`).

This is handled by a special Netlify configuration file named `netlify.toml` that has been automatically added to the root of your project.

**This file is the modern replacement for `.htaccess` on the Netlify platform.** It tells Netlify's servers how to rewrite URLs correctly. Since it's included in this ZIP, you don't need to do anything extra when deploying. Your clean URLs will work automatically.

---

## IMPORTANT: Image Naming Best Practices

This script works by copying **all** images from your Webflow project's `images` folder into a single `assets/images` directory. For this process to be successful, it is crucial to follow good naming conventions within your Webflow project.

*   **Use Unique & Descriptive Names:** Avoid generic names like `image1.jpg` or `icon.svg`. A name like `about-page-hero-background.jpg` is much better. If you use the same filename for two different images in your Webflow project, one may be overwritten, causing an image to go missing on your live site.
*   **Use Web-Safe Characters:** Stick to letters, numbers, hyphens (`-`), and underscores (`_`). **Avoid spaces, special characters (`&`, `?`, `%`, etc.), and uppercase letters**, as they can cause unexpected issues with URL paths and file matching.

Following these practices in Webflow will prevent broken images and ensure your site is processed correctly every time.

---

## CRITICAL: How to Activate Netlify Forms

After you deploy your site to Netlify, you must activate form detection for your new forms to work.

1.  Go to your site's dashboard on Netlify.
2.  Navigate to **Site configuration > Forms**.
3.  Under **Form detection**, ensure it is enabled.

Any form submissions will now appear in your Netlify dashboard's "Forms" section.

---

## Spam Filtering & reCAPTCHA

Netlify provides automatic, powerful spam filtering out of the box. Because of this, any reCAPTCHA elements provided by Webflow have been **completely removed** from your site's code. This provides a cleaner user experience and relies on Netlify's superior server-side filtering.

A "honeypot" field (invisible to users) has also been added to each form as an additional layer of spam protection.

---

## Technical Enhancements

*   **Anti-Interference Script:** A small script has been injected to ensure Webflow's native form JavaScript does not interfere with Netlify's form submission process.
*   **Asset Bundling:** All CSS, JavaScript, and image assets have been organized into a clean `assets/` directory structure for easier management.
