# Free Static WordPress Sites

> Learn how to build and host unlimited free static WordPress sites on Vercel, Netflify or DigitalOcean

## Quick Overview

This approach transforms your WordPress site into a collection of static HTML files, served directly to visitors.

Let's break down how this all works:

**1. Traditional WordPress:**

- Relies on PHP, a server-side language, to generate web pages dynamically upon each user request.
- Content is stored in a database, and PHP fetches it when needed.

**2. Static WordPress:**

- Uses a free plugin (Simply Static) to "capture" your WordPress site's content and media, generating static HTML, CSS, and JavaScript files.
- These files are then deployed to a free web server, eliminating the need for PHP or a database.

**Pros:**

- Blazing Fast Speed: Static files are incredibly lightweight and served quickly, resulting in significantly faster loading times. This improves user experience and SEO.
- Enhanced Security: With no database or PHP execution, the attack surface is drastically reduced, making your site less vulnerable to common WordPress security threats.
- Simplified Hosting: Static sites can be hosted on free hosting platforms, and you won't need managed WordPress hosting.

**Cons:**

- Limited Dynamic Functionality: Features requiring real-time data updates, like contact forms, user logins, or e-commerce, become more complex to implement.
- Content Updates Require Re-Generation: Every time you update your site's content, you need to re-generate the static files and re-deploy them.

Static WordPress is ideal for:

- Blogs
- Portfolios
- Business websites with mostly static content

It's less suitable for:

- Membership sites
- Online stores
- Sites requiring frequent content updates or dynamic features

For more detailed information, you can check out this [blog post](https://www.websiterating.com/blog/wordpress/how-to-host-a-static-wordpress-site-for-free/)

Now, let's dive into a step-by-step guide on how to set all of this up and get your unlimited free static WordPress sites up and running!

## LocalWP

**1. Install LocalWP on your local machine**

First, [download LocalWP for free](https://localwp.com/). Choose the version that matches your operating system (Windows, macOS, or Linux). Once downloaded, run the installer and follow the on-screen instructions. LocalWP makes it super easy to set up a local development environment.

When using LocalWP on a Windows machine you should choose Apache as the web server ([see](https://docs.simplystatic.com/article/56-how-to-fix-problems-with-your-local-development-tool))

**2. Download and use this Blueprint**

LocalWP Blueprints are pre-configured WordPress environments that save you time. You can import a Blueprint to quickly set up a site with specific settings. For this tutorial, we'll use a Blueprint designed for static WordPress sites. You can download it here: 

[Blueprint Link].

To import the Blueprint, open LocalWP and click on the 'Blueprints' tab. Then, click 'Import' and select the Blueprint file you downloaded.

**3. Create your WordPress site**

Now, let's create your WordPress site.

![image](https://github.com/user-attachments/assets/f8800814-0746-4294-a625-b7b2f66fe532)

- Launch LocalWP and start a new site. Click the '+' button in LocalWP to begin the process of creating a new site. You'll be guided through a few simple steps.

- Name your site and configure the environment. Give your site a descriptive name, like "My Static Site" or something related to its content. LocalWP will let you customize the local domain name (e.g., mystaticsite.local) – you can usually stick with the defaults.  

- Choose your preferred PHP version and database type (again, defaults are generally fine). Access your WordPress dashboard. Once LocalWP finishes setting up your site, you'll be able to access the WordPress dashboard directly. This is where the magic happens!

![image](https://github.com/user-attachments/assets/db521b5d-5bb6-40c7-854a-220ab55f704d)

- Install your theme. Head over to the 'Appearance' -> 'Themes' section of your WordPress dashboard. Here, you can browse and install themes to control the look and feel of your site. Choose a theme that aligns with your vision and install it.

- Add essential plugins.  Plugins extend the functionality of your WordPress site. Navigate to 'Plugins' -> 'Add New' in your dashboard. Search for and install plugins that are essential for your site's purpose. For example, if you're building a blog, you might want plugins for SEO, contact forms, or social media sharing.

Now you have a fully functional WordPress site running locally.  Take some time to customize your theme, configure your plugins, and start creating content!

## Static WordPress

**1. Install the SimplyStatic free plugin**

Log in to your WordPress site's dashboard (using the local URL provided by LocalWP). In the left-hand menu, go to 'Plugins' > 'Add New'. Search for 'Simply Static' and click 'Install Now'. Once installed, click 'Activate'.

**2. Export static build to a local directory**

![image](https://github.com/user-attachments/assets/44339a21-a734-4291-8471-bba8b7420484)

After activating SimplyStatic, go to 'Settings' > 'Simply Static'. Here, you can customize the export process. For now, keep the default settings.

![image](https://github.com/user-attachments/assets/99b33521-a24d-4896-a73f-db5abf0a2454)

Choose a directory on your computer where you want to save the static files (e.g., 'C:\Users\Local Sites\my-static-site\export'). Click 'Generate Static Files' to start the export.

## GitHub (Desktop)

1. Git commit the local directory

[Download GitHub Desktop](https://desktop.github.com/download/) and sign up for a free account.

Open GitHub Desktop and click 'Create a New Repository'.

![image](https://github.com/user-attachments/assets/44d23d87-546d-40fb-8aa0-8583789a95d5)

Choose the directory where you exported your static site files ('C:\Users\Local Sites\my-static-site\export' in our example).

Give your repository a name (e.g., 'my-static-site') and click 'Create Repository'.

GitHub Desktop will detect the files in the directory. Add a commit message like 'Initial static site build' and click 'Commit to main'.

2. Publish to GitHub

In GitHub Desktop, you'll see an option to 'Publish repository'. Click it.

Verify the repository name and choose whether you want it to be public or private.

Click 'Publish repository'. This will push your local files to a new repository on GitHub.com.

Sign in to GitHub.com, go to the repositiory and check that the static files of your WordPress site are there.

## Deploy to Vercel, Netlify, or DigitalOcean

1. Sign up for Vercel, Netlify, or DigitalOcean

You have several great options for hosting your static site for free:

Vercel: [Vercel signup link] - Known for its simplicity and speed, and generous free plan.
Netlify: [Netlify signup link] - Another popular choice with a generous free tier.
DigitalOcean: [DigitalOcean signup link] - Offers more control and flexibility, but might be a bit more technical.

Choose the platform that best suits your needs and create a free account.

2. Import the GitHub repository

Once you've signed up and logged in to your chosen platform, look for an option to 'Import Project' or 'New Site from Git'. Connect your GitHub account and select the repository you created ('my-static-site').

These platforms are designed for easy static site deployment. They'll auto-detect your site's build settings and deploy it automatically. You'll get a live URL where you can access your site!

3. Deploy

Deploy your site. This might involve clicking a 'Deploy' button or following a simple wizard.

4. Connect Your Custom Domain

Once deployed, each platform provides a default domain name (e.g., your-site-name.vercel.app, your-site-name.netlify.app).

To use a custom domain (e.g., www.yourdomain.com), you'll need to follow the platform-specific instructions for adding and verifying your domain. This usually involves updating DNS records with your domain registrar (like GoDaddy, Namecheap, etc.).

## Automating Deployments with GitHub Actions

Here's how you can set up a system that (semi) automatically detects changes in your local directory and pushes them to GitHub.

1. GitHub Desktop

GitHub Desktop is a user-friendly application that can simplify this process significantly. Here's how you can use it:

GitHub Desktop will automatically track changes in this folder.

Whenever you make changes:

- Open GitHub Desktop
- You'll see the changes listed
- Add a summary (commit message)
- Click "Commit to main"
- Click "Push origin"
