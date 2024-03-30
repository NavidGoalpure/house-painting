# Versatile Landing, Blog & Docs Template for a Simplified Web Presence

![ScrewFast](https://github.com/mearashadowfax/ScrewFast/assets/125820963/cdf299bd-414a-4a2d-baf0-d188bb4709c7)

ScrewFast is an open-source template designed for quick and efficient web project setup, blending minimalism with functionality. Whether you're showcasing a portfolio, launching a company landing page, or running a blog, ScrewFast provides everything you need. By combining the power of the [Astro](https://astro.build/), [Tailwind CSS](https://tailwindcss.com/), and [Preline UI](https://preline.co/), this template offers a functional and aesthetically pleasing solution for your web presence.

**[View Live Demo](https://screwfast.uk)**

## Table of Contents

- [Why Choose ScrewFast?](#why-choose-screwfast)
- [Features](#features)
- [What's New](#whats-new)
- [Getting Started](#getting-started)
  - [Installation](#installation)
  - [Development Commands](#development-commands)
- [Deployment](#deployment)
  - [Building Your Site](#building-your-site)
  - [Deploying to Vercel](#deploying-to-vercel)
- [Project Structure](#project-structure)
- [Static Assets and Public Resources](#static-assets-and-public-resources)
- [Customization](#customization)
  - [Editing Component Variables](#editing-component-variables)
  - [Props in Component Instances](#props-in-component-instances)
  - [Customizing Navigation and Footer Links](#customizing-navigation-and-footer-links)
    - [Navigation Bar Links](#navigation-bar-links)
    - [Footer Links](#footer-links)
    - [Social Media Links](#social-media-links)
- [Integrations and Enhancements](#integrations-and-enhancements)
  - [Lenis for Smooth Scrolling](#lenis-for-smooth-scrolling)
  - [GSAP Integration](#gsap-integration)
  - [Hiding Scrollbar](#hiding-scrollbar)
  - [SEO Configuration](#seo-configuration)
    - [Customizing Metadata with Meta.astro](#customizing-metadata-with-metaastro)
    - [Applying Metadata in Layouts](#applying-metadata-in-layouts)
    - [Customizing Metadata on Individual Pages](#customizing-metadata-on-individual-pages)
    - [Extending Metadata for SEO](#extending-metadata-for-seo)
    - [Structured Data and Rich Snippets](#structured-data-and-rich-snippets)
    - [Using Astro SEO Integrations](#using-astro-seo-integrations)
  - [Robots.txt](#robotstxt)
  - [Astro Integrations](#astro-integrations)
  - [Flexibility with Integrations](#flexibility-with-integrations)
- [Tools and Technologies](#tools-and-technologies)
  - [Preline UI](#preline-ui)
  - [Tailwind CSS](#tailwind-css)
  - [Deployment and Security](#deployment-and-security)
  - [HTML Minification](#html-minification)
- [Contributing](#contributing)
- [License](#license)

## Why Choose ScrewFast?

- **Efficient Architecture:** Deploy faster with a template that's simple to set up and navigate.
- **Optimized for Small Projects:** Perfect for crisp, professional web personas without excess complexity.
- **Highly Customizable:** Flexibly adapt and style your site using Astro and Tailwind CSS.

## Features

- **Astro-Powered:** Utilize a modern static-site generation framework.
- **Tailwind CSS:** Enjoy rapid UI development with a utility-first CSS framework.
- **Preline UI:** Implement prebuilt UI components for added elegance.
- **GSAP Integration:** Impress with professional and polished animations.
- **Markdown Content Collections:** Organize and manage your content seamlessly.
- **SEO and Responsiveness:** Ensure your site is discoverable and accessible on any device.

## What's New

### Added Features

- [x] **Social Share Component**:

  - Enables users to share blog posts on social media platforms.
  - Provides easy sharing of a blog post's title and URL.
  - Integrates Clipboard.js for link URL copy functionality.

- [x] **Bookmark Button Component**:

  - Allows users to bookmark blog posts for later reference.
  - Provides a visual indication of whether a post is bookmarked.
  - Utilizes `localStorage` to store bookmarks locally in the browser.
  - For SSR, replace `localStorage` with cookies to persist bookmarked posts.
    - This setup opens up the possibility for the server to dynamically render content based on user-specific bookmarks, should you choose to implement this feature.

- [x] **Post Feedback Component**:
  - Collects user feedback at the end of each blog post.
  - Serves as a UI demonstration with no live back-end integration.

### Planned Improvements

- [ ] Implement a table of contents (ToC) sidebar for blog articles.

### Bug Fixes

- Currently, there are no known bugs. If you encounter any issues, please report them on our [issues page](https://github.com/mearashadowfax/ScrewFast/issues).

## Getting Started

This guide will provide you with the necessary steps to set up and familiarize yourself with the Astro project on your local development machine.

### Installation

Start by installing the project dependencies. Open your terminal, navigate to the project's root directory, and execute:

```bash
npm install
```

This command will install all the necessary dependencies defined in the `package.json` file.

### Development Commands

With dependencies installed, you can utilize the following npm scripts to manage your project's development lifecycle:

- `npm run dev`: Starts a local development server with hot reloading enabled.
- `npm run preview`: Serves your build output locally for preview before deployment.
- `npm run build`: Bundles your site into static files for production.

For detailed help with Astro CLI commands, visit [Astro's documentation](https://docs.astro.build/en/reference/cli-reference/).

## Deployment

### Building Your Site

Before deployment, you need to create a production build:

```bash
npm run build
```

This creates a `dist/` directory with your built site (configurable via [outDir in Astro](https://docs.astro.build/en/reference/configuration-reference/#outdir)).

### Deploying to Vercel

Click the button below to start deploying your project on Vercel:

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2Fmearashadowfax%2FScrewFast)

## Project Structure

ScrewFast organizes modular components, content, and layouts to streamline development and content management. Expand for a detailed overview of the directory structure:

```md
src/
├── components/ # Reusable components
│ ├── Meta.astro # Meta component for SEO
│ ├── sections/ # Components for various sections of the website
│ ├── ThemeIcon.astro # Component for toggling light/dark themes
│ └── ui/ # UI components categorized by functionality
├── content/ # Markdown files for blog posts, insights, products, and site configuration
│ ├── blog/  
│ ├── insights/  
│ ├── products/  
│ └── config.ts # Contains site-wide configuration options
├── images/ # Static image assets for use across the website
├── layouts/ # Components defining layout templates
│ └── MainLayout.astro # The main wrapping layout for all pages
├── pages/ # Astro files representing individual pages and website sections
│ ├── 404.astro # Custom 404 page
│ ├── blog/  
│ ├── contact.astro  
│ ├── index.astro # The landing/home page
│ ├── insights/  
│ ├── products/  
│ ├── robots.txt.ts # Dynamically generates robots.txt
│ └── services.astro  
└── utils/ # Shared utility functions and helpers
```

## Static Assets and Public Resources

Static files served directly to the browser are within the `public` directory at the root of the project. Expand for the layout:

```md
public/
├── apple-touch-icon.png
├── favicon.ico
├── icon-192.png
├── icon-512.png
├── icon.svg
├── manifest.webmanifest
├── maskable_icon.png
├── maskable_icon_x512.png
├── scripts/
│ └── vendor/
│ ├── gsap/ # Animations powered by GSAP (GreenSock Animation Platform)
│ │ └── gsap.min.js
│ ├── lenis/ # Lenis script for smooth scrolling effects
│ │ └── lenis.js
│ └── preline/ # Preline UI plugins
│ ├── accordion/
│ ├── collapse/
│ ├── overlay/
│ └── tabs/
└── social.png # Image used for social media sharing previews
```

The scripts in the `public/scripts/vendor` directory are essential for the interactivity and aesthetic features of the website. Do not remove these unless you plan to replace their functionality.

## Customization

ScrewFast allows for easy customization to suit your specific needs. Here are a couple of ways you can configure components and content:

### Editing Component Variables

Some components have properties defined as TypeScript variables within the component file. Here's an example of customizing the `FeaturesGeneral` component:

```typescript
// Define the string variables title and subTitle for the main heading and sub-heading text.
const title: string = "Meeting Industry Demands";
const subTitle: string =
  "At ScrewFast, we tackle the unique challenges encountered in the hardware and construction sectors.";
```

For collections of content like testimonials or statistics, edit the corresponding array of objects:

```typescript
// An array of testimonials
const testimonials: Testimonial[] = [...];

// An array of statistics
const statistics: StatProps[] = [...];
```

Modify the content within these arrays to reflect your data.

### Props in Component Instances

You can pass values to props directly in the page files for components used across pages. Here's an example of a `HeroSection` and `ClientsSection` component with inline props:

```html
<HeroSection
  subTitle="Top-quality hardware tools and expert construction services for every project need."
  primaryBtn="Start Exploring"
  primaryBtnURL="/explore"
/>

<ClientsSection
  title="Trusted by Industry Leaders"
  subTitle="Experience the reliability chosen by industry leaders."
/>
```

Edit the props such as `title`, `subTitle`, `primaryBtn`, etc., to personalize these sections. Ensure that you maintain the structure and data types of the props.

### Customizing Navigation and Footer Links

Edit the `navigation.ts` file within the `utils` directory to manage navigation bar and footer links:

#### Navigation Bar Links

Edit the `navBarLinks` array to adjust navigation bar links:

```typescript
// An array of links for the navigation bar
export const navBarLinks: NavLink[] = [
  { name: "Home", url: "/" },
  { name: "Products", url: "/products" },
  { name: "Services", url: "/services" },
  { name: "Blog", url: "/blog" },
  { name: "Contact", url: "/contact" },
];
```

Replace `name` with the display text and `url` with the appropriate path to pages on your site.

#### Footer Links

Similarly, adjust the links displayed in the footer by editing the `footerLinks` array:

```typescript
// An array of links for the footer
export const footerLinks: FooterLinkSection[] = [
  {
    section: "Product",
    links: [
      { name: "Tools & Equipment", url: "/tools-equipment" },
      { name: "Construction Services", url: "/construction-services" },
      { name: "Pricing", url: "/pricing" },
    ],
  },
  {
    section: "Company",
    links: [
      { name: "About us", url: "/about" },
      { name: "Blog", url: "/blog" },
      { name: "Careers", url: "/careers" },
      { name: "Customers", url: "/customers" },
    ],
  },
];
```

Each section within the `footerLinks` array represents a group of links. Update the `section` value for the group heading and modify each link's `name` and `url` as needed.

#### Social Media Links

Replace the placeholder URLs in the `socialLinks` object with your social media profiles:

```typescript
// An object of links for social icons
export const socialLinks: SocialLinks = {
  facebook: "#",
  twitter: "#",
  github: "#",
  linkedin: "#",
  instagram: "#",
};
```

> [!NOTE]
> Remember to add complete and valid URLs for the navigation to function properly. These customizations will reflect throughout your Astro site, promoting consistency across all pages.

</details>

## Integrations and Enhancements

ScrewFast leverages the power of Astro — a modern, cutting-edge site building framework — and integrates it seamlessly with the utility-first CSS framework TailwindCSS, to deliver exceptional site performance and a seamless user experience. Here are some notable integrations and enhancements included in the project:

ScrewFast is now equipped with the Starlight, which is designed to elevate the user's experience with documentation. This modern and elegant theme comes with a suite of features to make the content more accessible and pleasant to navigate.

Key Features:

- **Site Navigation and Search**: Navigate through the documentation with ease using intuitive sidebar and built-in search functionality.
- **Internationalization**: Cater to a global audience with the ability to switch languages, making documentation accessible to everyone, everywhere.
- **SEO Friendly**: Optimized for search engines to help users quickly find the information they need.
- **Code Highlighting and Dark Mode**: Enhances code readability with syntax highlighting, and offers a dark mode to reduce eye strain for users.
- **Mobile Responsive Design**: Whether you're on a phone, tablet, or desktop, the documentation adapts to your screen size for optimal readability.

With Starlight, you gain access to a wealth of powerful features and integrations, along with extensive customization options to fit your needs.

> [!NOTE]
> Dive into the Starlight's comprehensive feature list and learn how it can streamline your development process by visiting the theme's [documentation site](https://starlight.astro.build/).

### Lenis for Smooth Scrolling

Experience buttery smooth scrolling with [Lenis](https://lenis.studiofreight.com/). We've integrated Lenis to provide an enhanced scrolling experience that's both fluid and responsive.

Here's how we set up Lenis in `src/layouts/MainLayout.astro`:

```astro
<script is:inline src="/scripts/vendor/lenis/lenis.js"></script>
<script is:inline>
  // Script to handle Lenis library settings for smooth scrolling
  const lenis = new Lenis({
    smooth: true,
    smoothTouch: false
  });

  function raf(time) {
    lenis.raf(time); // Update Lenis on each animation frame
    requestAnimationFrame(raf); // Continuously invoke the raf function at refresh rate
  }
  requestAnimationFrame(raf); // Start the loop
</script>
<style>
html.lenis {
  height: auto;
}
.lenis.lenis-smooth {
  scroll-behavior: auto !important;
}
.lenis.lenis-smooth [data-lenis-prevent] {
  overscroll-behavior: contain;
}
.lenis.lenis-stopped {
  overflow: hidden;
}
.lenis.lenis-scrolling iframe {
  pointer-events: none;
}
</style>
```

Please note that smooth scrolling can affect accessibility and performance on some devices, so be sure to test it comprehensively across different environments.

> [!NOTE]
> If you would like to remove Lenis and return to the browser's default scrolling behavior, simply comment out or delete these lines from the `MainLayout.astro` file.

### GSAP Integration

For individual product pages, [GSAP](https://gsap.com/) has been integrated to add engaging animations that execute as soon as the product page loads. You can find and modify the GSAP configuration in the script sections of the product page file located at `src/pages/products/[...slug].astro`:

```astro
<script is:inline src="/scripts/vendor/gsap/gsap.min.js"></script>
<script>
  window.addEventListener("load", (event) => {
    if (window.gsap) {
      const gsap = window.gsap;
      // Initialize GSAP animations...
    }
  });
</script>
```

**Customizing Animations:**

Please tailor the GSAP animations within this script to fit your project's look and feel. The provided example is a starting point, representing how to leverage GSAP for immediate visual impact as a product page loads.

**Modifying or Removing Animations:**

- To modify an animation, update the properties and parameters within the `gsap.from()` method, or add new GSAP animation calls as required.
- Should GSAP not be needed, or if you prefer a different animation method, simply remove the aforementioned script segment.

> [!NOTE]
> We've chosen to keep the integration lean and focused, but GSAP's comprehensive documentation can be referred to for more complex animations: [GSAP Documentation](https://gsap.com/docs/v3/).

### Hiding Scrollbar

To achieve a cleaner and more spacious design, the default scrollbar has been visually removed. While this choice fits the aesthetic goals of the project, it's important to consider that hiding scrollbars can sometimes affect accessibility and user experience. We recommend evaluating this design decision within the context of your user base and their needs.

For those who prefer custom-styled scrollbars, we suggest using the [tailwind-scrollbar](https://adoxography.github.io/tailwind-scrollbar/) plugin, which adds Tailwind CSS utilities for scrollbar styles, allowing for more controlled customization that can also meet accessibility standards.

> [!NOTE]
> If you wish to return the default scrollbar, you can comment out or remove the following CSS from `src/layouts/MainLayout.astro`:

```html
<style>
  .scrollbar-hide::-webkit-scrollbar {
    display: none;
  }
  .scrollbar-hide {
    -ms-overflow-style: none;
    scrollbar-width: none;
  }
</style>
```

Additionally, update the `<html>` tag to remove the `scrollbar-hide` class, resulting in:

```html
<html lang="en" class="scroll-pt-16"></html>
```

### SEO Configuration

The ScrewFast template incorporates a flexible SEO configuration that empowers you to effectively optimize each page for search engines as well as social media platforms. By utilizing the `Meta.astro` component, you can easily customize important metadata such as page titles, descriptions, author information, and social media images to improve your site's visibility and engagement.

#### Customizing Metadata with Meta.astro

The `Meta.astro` component is pre-configured with default metadata values that should be defined to align with your website's content, ensuring out-of-the-box SEO readiness. These defaults can be overridden on a per-page basis:

```astro
---
// In Meta.astro component
const defaultDescription = "ScrewFast offers top-tier hardware tools and expert construction services.";
const { meta = defaultDescription } = Astro.props;
---
```

By setting the `defaultDescription` to a value that accurately reflects the content of your website, you ensure that all pages will have a relevant default meta description unless otherwise specified.

#### Applying Metadata in Layouts

When applying metadata within your layouts, such as `MainLayout.astro`, you can pass the desired metadata values as props to the `Meta` component:

```astro
---
// In MainLayout.astro file
const { meta } = Astro.props;

interface Props {
  meta?: string;
}
---

<Meta meta={meta} />
```

#### Customizing Metadata on Individual Pages

Finally, custom metadata can be passed to your layout component within individual page files, allowing for page-specific overrides:

```astro
---
// In your individual page file
import MainLayout from '../layouts/MainLayout.astro';
---

<MainLayout meta="Find the perfect hardware tools with ScrewFast for all your construction needs.">
  <!-- Page content -->
</MainLayout>
```

With this setup, the Meta component receives the custom meta description and applies it to the page's metadata. If no custom value is passed, the default from `Meta.astro` will be used instead.

#### Extending Metadata for SEO

For a more robust SEO strategy, you can create additional properties in the `Meta.astro` component. For instance, you may want to include specific Open Graph tags for article publishing dates or tags for Twitter-specific metadata.

#### Structured Data and Rich Snippets

Structured data in JSON-LD format can be managed by the `Meta.astro` component, improving how search engines understand your page content and potentially enhancing search results with rich snippets. Modify the `structuredData` property with relevant [schema.org](https://schema.org) types and properties:

```astro
<MainLayout
  structuredData={{
    "@context": "https://schema.org",
    "@type": "WebSite",
    "name": "ScrewFast",
    "url": "https://screwfast.uk",
    "description": "Discover top-quality hardware tools and services"
  }}
>
```

#### Using Astro SEO Integrations

While the template provides a custom SEO solution, you may choose to utilize an Astro integration such as [Astro SEO](https://github.com/jonasmerlin/astro-seo#readme) for additional SEO features and optimizations. Integrating such a package might provide more automated metadata management and additional SEO-focused functionality.

### Robots.txt

`robots.txt` is dynamically generated using the code found in src/pages/robots.txt.ts. This configuration follows the example from the Astro Docs:

```ts
import type { APIRoute } from "astro";

const robotsTxt = `
User-agent: *
Allow: /

Sitemap: ${new URL("sitemap-index.xml", import.meta.env.SITE).href}
`.trim();

export const GET: APIRoute = () => {
  return new Response(robotsTxt, {
    headers: {
      "Content-Type": "text/plain; charset=utf-8",
    },
  });
};
```

### Astro Integrations

Maximize your website's efficiency with these built-in Astro integrations:

- [Astro Compressor](https://github.com/sondr3/astro-compressor#readme): Automatically compresses Astro-generated site using gzip or brotli, ensuring faster load times.
  Configure the compressor in `astro.config.mjs` file:

```mjs
   export default defineConfig({
     // ...other Astro configurations
    integrations: [...other Astro integrations, compressor({ gzip: false, brotli: true })],
   });
```

- [Astro Sitemap](https://docs.astro.build/en/guides/integrations-guide/sitemap/): Automatically generates a sitemap for a website, which is vital for SEO and helping search engine bots crawl pages effectively. To set up the Astro Sitemap, be sure to specify your site's base URL and any additional options in `astro.config.mjs` file:

```mjs
export default defineConfig({
  // ...
  site: "https://example.com",
  integrations: [sitemap()],
});
```

### Flexibility with Integrations

The great thing about Astro is its rich ecosystem of integrations, allowing you to tailor project functionalities to your exact needs. Feel free to explore [Astro integrations page](https://astro.build/integrations/) and add additional capabilities as you see fit.

</details>

## Tools and Technologies

This project is built using a variety of tools and technologies that enhance its performance, maintainability, and developer experience. Below is a list of the key tools and their roles in the project:

### Preline UI

Interactive components like navbars, modals, and accordions are built using [Preline UI](https://preline.co), a comprehensive open-source component library.

### Tailwind CSS

Styling across our project leverages the utility-first classes offered by [Tailwind CSS](https://tailwindcss.com). This methodology allows us to create custom layouts and components with speed and efficiency.

To ensure consistent code formatting, particularly for class sorting, we have integrated the `prettier-plugin-tailwindcss` [plugin](https://github.com/tailwindlabs/prettier-plugin-tailwindcss). The following configuration is set in the `.prettierrc` file at the root of the project:

```json
{
  "plugins": ["prettier-plugin-tailwindcss"]
}
```

### Deployment and Security

We deploy our project on [Vercel](https://vercel.com), capitalizing on their robust platform for seamless CI/CD workflows. Using `vercel.json`, we set stringent security headers and caching policies, ensuring adherence to security and performance best practices:

```json
{
  "headers": [
    {
      "source": "/(.*)",
      "headers": [
        {
          "key": "Content-Security-Policy",
          "value": "default-src 'self'; [other-directives]"
        },
        "Additional security headers..."
      ]
    }
  ]
}
```

### HTML Minification

For optimal site performance, we post-process our HTML files with `process-html.mjs`, a [custom script](https://straffesites.com/en/blog/optimize-astro-html-post-build) that minifies HTML after the build phase to reduce file size and improve load times.

Here is a snippet from our HTML minification script in `process-html.mjs`:

```mjs
/process-html.mjs
// Post-build HTML minification script snippet
// ...
await Promise.all(
  files.map(async (file) => {
    // File processing and minification logic
  })
);
```

We encourage you to refer to the detailed documentation for each tool to fully understand their capabilities and how they contribute to the project:

- [Preline UI Documentation](https://preline.co/docs)
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [Vercel Documentation](https://vercel.com/docs)
- [html-minifier Documentation](https://github.com/kangax/html-minifier)

## Contributing

If you're interested in helping, you can contribute in several ways:

1. Reporting Issues: Feel free to use the issue tracker to report bugs or request features.
2. Submitting Pull Requests: If you've fixed a bug or added a new feature, submit a pull request with a clear description of your changes.
3. Providing Feedback: Share your thoughts on the project's current features and suggest improvements.

## License

This project is released under the MIT License. Please read the [LICENSE](https://github.com/mearashadowfax/ScrewFast/blob/main/LICENSE) file for more details.
