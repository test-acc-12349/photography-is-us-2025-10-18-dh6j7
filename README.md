# Photography Is Us Landing Page - Maintenance & Customization Guide

## Table of Contents
1. [Overview](#overview)
2. [Updating Text Content](#updating-text-content)
3. [Modifying Tailwind CSS Classes](#modifying-tailwind-css-classes)
4. [Fixing Broken Links](#fixing-broken-links)
5. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
6. [Troubleshooting](#troubleshooting)
7. [Best Practices](#best-practices)

---

## Overview

This landing page is built with **HTML**, **Tailwind CSS** (a utility-first CSS framework), and **Font Awesome** (for icons). Understanding the structure will help you maintain and customize it effectively.

### Key Components:
- **Announcement Bar**: Promotional message at the top
- **Header/Navigation**: Logo, menu links, and mobile hamburger menu
- **Hero Section**: Large banner with main headline
- **Features Section**: Three-column layout highlighting key products
- **Benefits Section**: Alternating text and image sections
- **Testimonials**: Customer reviews with ratings
- **FAQ Section**: Expandable accordion questions
- **Newsletter**: Email subscription form
- **Footer**: Links, contact info, and social media

---

## Updating Text Content

### 1. Announcement Bar
**Location**: Lines 103-107

This is the promotional message at the very top of the page.

**Current text:**
```html
<p class="text-sm md:text-base font-light tracking-wide">
    <i class="fas fa-shipping-fast mr-2"></i>Free Worldwide Shipping on Orders Over $50
</p>
```

**How to change it:**
1. Open `index.html` in your text editor
2. Find the text "Free Worldwide Shipping on Orders Over $50"
3. Replace it with your message, for example:
```html
<p class="text-sm md:text-base font-light tracking-wide">
    <i class="fas fa-shipping-fast mr-2"></i>Limited Time: 20% Off All LED Kits!
</p>
```

**💡 Pro Tip**: Keep announcements short and impactful. The `text-sm md:text-base` means it will be small on mobile and regular-sized on desktop.

---

### 2. Logo/Brand Name
**Location**: Lines 110-113

**Current text:**
```html
<div class="flex items-center space-x-2">
    <i class="fas fa-camera text-gray-900 text-2xl"></i>
    <span class="text-xl md:text-2xl font-bold text-gray-900 tracking-tight">Photography Is Us</span>
</div>
```

**How to change it:**
Simply replace "Photography Is Us" with your brand name:
```html
<span class="text-xl md:text-2xl font-bold text-gray-900 tracking-tight">Your Brand Name</span>
```

**To change the icon**, visit [Font Awesome Icons](https://fontawesome.com/icons) and find your preferred icon. Replace `fa-camera` with the new icon name. For example, to use a lightbulb:
```html
<i class="fas fa-lightbulb text-gray-900 text-2xl"></i>
```

---

### 3. Navigation Menu Items
**Location**: Lines 116-121

**Current text:**
```html
<a href="#features" class="text-gray-700 hover:text-gray-900 font-medium smooth-transition text-sm">Features</a>
<a href="#benefits" class="text-gray-700 hover:text-gray-900 font-medium smooth-transition text-sm">Benefits</a>
<a href="#faq" class="text-gray-700 hover:text-gray-900 font-medium smooth-transition text-sm">FAQ</a>
<a href="#contact" class="text-gray-700 hover:text-gray-900 font-medium smooth-transition text-sm">Contact</a>
```

**How to add a new menu item:**
1. Copy one of the existing `<a>` tags
2. Paste it next to the others
3. Change the text and href:

```html
<a href="#portfolio" class="text-gray-700 hover:text-gray-900 font-medium smooth-transition text-sm">Portfolio</a>
```

**Important**: The `href="#portfolio"` must match a section ID on your page (like `<section id="portfolio">`). If the section doesn't exist, the link won't work.

---

### 4. Hero Section Headline
**Location**: Lines 160-163

**Current text:**
```html
<h1 class="text-4xl md:text-6xl lg:text-7xl font-bold tracking-tight leading-tight mb-6 md:mb-8">
    Photography Is Us
</h1>
```

**How to change it:**
```html
<h1 class="text-4xl md:text-6xl lg:text-7xl font-bold tracking-tight leading-tight mb-6 md:mb-8">
    Your New Headline Here
</h1>
```

**Understanding the text sizes:**
- `text-4xl` = Extra large (mobile)
- `md:text-6xl` = Larger (tablets)
- `lg:text-7xl` = Largest (desktops)

This ensures the headline looks good on all screen sizes.

---

### 5. Hero Section Subtitle
**Location**: Lines 164-167

**Current text:**
```html
<p class="text-xl md:text-2xl lg:text-3xl font-light leading-relaxed mb-8 md:mb-12 text-gray-100">
    Best Photography Kit
</p>
```

**How to change it:**
```html
<p class="text-xl md:text-2xl lg:text-3xl font-light leading-relaxed mb-8 md:mb-12 text-gray-100">
    Your Subtitle Here
</p>
```

---

### 6. Hero Section Description
**Location**: Lines 168-172

**Current text:**
```html
<p class="text-base md:text-lg text-gray-200 mb-8 md:mb-12 max-w-2xl mx-auto leading-relaxed">
    Professional-grade LED lighting, premium tripods, and pro equipment to elevate your photography game
</p>
```

**How to change it:**
```html
<p class="text-base md:text-lg text-gray-200 mb-8 md:mb-12 max-w-2xl mx-auto leading-relaxed">
    Your description text here. Make it compelling and benefit-focused.
</p>
```

---

### 7. Feature Cards
**Location**: Lines 201-280

There are three feature cards. Here's how to update the first one:

**Current text:**
```html
<h3 class="text-xl md:text-lg lg:text-xl font-bold text-gray-900 mb-3">
    LED Lighting
</h3>
<p class="text-gray-600 leading-relaxed text-sm md:text-base">
    Professional-grade LED lighting systems with adjustable color temperature and brightness control...
</p>
```

**How to change it:**
```html
<h3 class="text-xl md:text-lg lg:text-xl font-bold text-gray-900 mb-3">
    Your Feature Title
</h3>
<p class="text-gray-600 leading-relaxed text-sm md:text-base">
    Your feature description here.
</p>
```

**To change the icon and color gradient:**
Find this section in each card:
```html
<div class="w-16 h-16 bg-gradient-to-br from-yellow-400 to-orange-500 rounded-full flex items-center justify-center mb-6">
    <i class="fas fa-lightbulb text-white text-2xl"></i>
</div>
```

- Change `fa-lightbulb` to your preferred icon
- Change `from-yellow-400 to-orange-500` to new colors:
  - `from-blue-400 to-blue-600`
  - `from-green-400 to-green-600`
  - `from-purple-400 to-purple-600`

**To update the bullet points:**
```html
<ul class="mt-4 space-y-2 text-sm text-gray-600">
    <li class="flex items-center">
        <i class="fas fa-check text-green-500 mr-3"></i>
        Your first benefit
    </li>
    <li class="flex items-center">
        <i class="fas fa-check text-green-500 mr-3"></i>
        Your second benefit
    </li>
</ul>
```

---

### 8. Benefits Section Titles and Content
**Location**: Lines 314-416

**Example - Free Delivery section:**
```html
<h3 class="text-3xl md:text-4xl font-bold text-gray-900 mb-4 tracking-tight">
    Free Delivery
</h3>
<p class="text-lg text-gray-600 leading-relaxed mb-6">
    We believe photography equipment should be accessible to everyone...
</p>
```

**How to change it:**
Simply replace the text between the opening and closing tags with your content.

---

### 9. Testimonials
**Location**: Lines 470-530

**Current structure:**
```html
<div class="testimonial-card bg-white rounded-2xl p-8 border border-gray-200 hover:border-gray-300">
    <div class="flex items-center mb-4">
        <div class="flex text-yellow-400">
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
        </div>
    </div>
    <p class="text-gray-600 leading-relaxed mb-6 text-base">
        "The quality of the equipment exceeded my expectations..."
    </p>
    <div class="flex items-center">
        <div class="w-12 h-12 bg-gradient-to-br from-blue-400 to-blue-600 rounded-full flex items-center justify-center text-white font-bold mr-4">
            SM
        </div>
        <div>
            <p class="font-semibold text-gray-900">Sarah Martinez</p>
            <p class="text-sm text-gray-600">Professional Photographer</p>
        </div>
    </div>
</div>
```

**How to update testimonials:**

1. **Change the quote:**
```html
<p class="text-gray-600 leading-relaxed mb-6 text-base">
    "Your new testimonial text here"
</p>
```

2. **Change the customer name:**
```html
<p class="font-semibold text-gray-900">New Customer Name</p>
```

3. **Change the job title:**
```html
<p class="text-sm text-gray-600">Their job title</p>
```

4. **Change the initials in the avatar:**
```html
<div class="w-12 h-12 bg-gradient-to-br from-blue-400 to-blue-600 rounded-full flex items-center justify-center text-white font-bold mr-4">
    NC
</div>
```

5. **Change the avatar color:**
Replace `from-blue-400 to-blue-600` with:
- `from-green-400 to-green-600`
- `from-purple-400 to-purple-600`
- `from-red-400 to-red-600`

---

### 10. FAQ Questions and Answers
**Location**: Lines 551-634

**Current structure:**
```html
<div class="accordion-item bg-white border border-gray-200 rounded-xl overflow-hidden hover:border-gray-300 smooth-transition">
    <button class="w-full px-6 md:px-8 py-5 md:py-6 flex items-center justify-between hover:bg-gray-50 smooth-transition text-left" onclick="toggleAccordion(this)">
        <span class="text-lg md:text-xl font-semibold text-gray-900 pr-4">
            What is included in the photography kit?
        </span>
        <i class="accordion-icon fas fa-chevron-down text-gray-600 flex-shrink-0 smooth-transition"></i>
    </button>
    <div class="accordion-content px-6 md:px-8 pb-5 md:pb-6 border-t border-gray-200">
        <p class="text-gray-600 leading-relaxed">
            Our complete photography kit includes professional LED lighting systems...
        </p>
    </div>
</div>
```

**How to update FAQ items:**

1. **Change the question:**
```html
<span class="text-lg md:text-xl font-semibold text-gray-900 pr-4">
    Your new question here?
</span>
```

2. **Change the answer:**
```html
<p class="text-gray-600 leading-relaxed">
    Your answer text here.
</p>
```

**To add a new FAQ item:**
Copy the entire `<div class="accordion-item">` block and paste it below the existing FAQs. Update the question and answer text.

---

### 11. Footer Links and Information
**Location**: Lines 710-790

**Company description:**
```html
<p class="text-gray-400 leading-relaxed mb-6">
    Professional photography equipment and lighting solutions for creators worldwide.
</p>
```

**How to change it:**
```html
<p class="text-gray-400 leading-relaxed mb-6">
    Your company description here.
</p>
```

**Quick Links section:**
```html
<li>
    <a href="#features" class="text-gray-400 hover:text-white smooth-transition">Features</a>
</li>
```

**Contact information:**
```html
<li class="flex items-start">
    <i class="fas fa-envelope text-gray-500 mr-3 mt-1 flex-shrink-0"></i>
    <a href="mailto:admin@led.com" class="text-gray-400 hover:text-white smooth-transition break-all">admin@led.com</a>
</li>
```

**How to update email:**
Replace `admin@led.com` with your email address:
```html
<a href="mailto:your-email@domain.com" class="text-gray-400 hover:text-white smooth-transition break-all">your-email@domain.com</a>
```

**How to update phone:**
Replace `+1-800-LED-PHOTO` with your phone number:
```html
<a href="tel:+1-800-YOUR-NUMBER" class="text-gray-400 hover:text-white smooth-transition">+1-800-YOUR-NUMBER</a>
```

---

## Modifying Tailwind CSS Classes

### Understanding Tailwind CSS Basics

Tailwind CSS uses utility classes that you combine to style elements. Instead of writing custom CSS, you add classes directly to HTML tags.

**Example:**
```html
<p class="text-lg text-gray-600 font-bold">This is styled text</p>
```

Breaking this down:
- `text-lg` = Large text size
- `text-gray-600` = Gray color
- `font-bold` = Bold font weight

### Common Tailwind Classes Used in This Page

#### Text Sizing
```
text-sm      = Small
text-base    = Regular (default)
text-lg      = Large
text-xl      = Extra large
text-2xl     = 2x large
text-3xl     = 3x large
text-4xl     = 4x large
```

**How to use it:**
```html
<!-- This text will be large on mobile, extra-large on tablets, and 2x large on desktops -->
<h2 class="text-2xl md:text-3xl lg:text-4xl">My Heading</h2>
```

#### Responsive Prefixes
These prefixes change styling at different screen sizes:
- `sm:` = Small screens (640px)
- `md:` = Medium screens (768px)
- `lg:` = Large screens (1024px)

**Example:**
```html
<p class="text-sm md:text-base lg:text-lg">
    This text is small on mobile, regular on tablets, large on desktops
</p>
```

#### Colors
Tailwind uses a color system with intensity levels (50-900):
```
bg-gray-50      = Very light gray background
bg-gray-100     = Light gray background
bg-gray-900     = Very dark gray background
text-white      = White text
text-gray-600   = Medium gray text
```

**How to change text color:**
```html
<!-- Change from gray to blue -->
<p class="text-blue-600">My text</p>
```

**How to change background color:**
```html
<!-- Change background from white to light gray -->
<div class="bg-gray-50">Content</div>
```

#### Spacing (Padding & Margin)
```
p-4      = Padding on all sides
px-4     = Padding left and right
py-4     = Padding top and bottom
m-4      = Margin on all sides
mx-auto  = Center horizontally
```

**Example:**
```html
<!-- Add padding and center content -->
<div class="px-6 py-8 mx-auto">Content</div>
```

#### Common Modifications in This Page

**1. Change Button Colors**

**Current button:**
```html
<a href="https://led.com" class="btn-primary inline-flex items-center px-6 py-2.5 bg-gray-900 text-white font-semibold rounded-full hover:bg-gray-800 smooth-transition">
    Shop Now
    <i class="fas fa-arrow-right ml-2"></i>
</a>
```

**To make it blue:**
```html
<a href="https://led.com" class="btn-primary inline-flex items-center px-6 py-2.5 bg-blue-600 text-white font-semibold rounded-full hover:bg-blue-700 smooth-transition">
    Shop Now
    <i class="fas fa-arrow-right ml-2"></i>
</a>
```

**Key changes:**
- `bg-gray-900` → `bg-blue-600` (button background)
- `hover:bg-gray-800` → `hover:bg-blue-700` (button on hover)

**2. Change Card Styling**

**Current feature card:**
```html
<div class="feature-card bg-white border border-gray-200 rounded-2xl p-8 md:p-6 lg:p-8 hover:border-gray-300">
```

**To add more shadow and change border:**
```html
<div class="feature-card bg-white border-2 border-blue-200 rounded-2xl p-8 md:p-6 lg:p-8 hover:border-blue-400 shadow-lg">
```

**Changes:**
- `border border-gray-200` → `border-2 border-blue-200` (thicker, blue border)
- `hover:border-gray-300` → `hover:border-blue-400` (blue on hover)
- Added `shadow-lg` (adds shadow effect)

**3. Change Section Background Colors**

**Current:**
```html
<section class="w-full py-16 md:py-24 px-4 sm:px-6 lg:px-8 bg-white">
```

**To make it light gray:**
```html
<section class="w-full py-16 md:py-24 px-4 sm:px-6 lg:px-8 bg-gray-50">
```

**4. Adjust Padding/Spacing**

**Current:**
```html
<div class="py-16 md:py-24 px-4">
```

**To add more spacing:**
```html
<div class="py-20 md:py-32 px-6">
```

**Changes:**
- `py-16` → `py-20` (more vertical padding on mobile)
- `md:py-24` → `md:py-32` (more vertical padding on tablets+)
- `px-4` → `px-6` (more horizontal padding)

**5. Change Gradient Colors**

**Current gradient:**
```html
<div class="w-16 h-16 bg-gradient-to-br from-yellow-400 to-orange-500 rounded-full">
```

**To change to blue gradient:**
```html
<div class="w-16 h-16 bg-gradient-to-br from-blue-400 to-blue-600 rounded-full">
```

**To change to green gradient:**
```html
<div class="w-16 h-16 bg-gradient-to-br from-green-400 to-green-600 rounded-full">
```

**Understanding gradients:**
- `bg-gradient-to-br` = Gradient direction (top-left to bottom-right)
- `from-yellow-400` = Starting color
- `to-orange-500` = Ending color

### Responsive Design Tips

**Always test on multiple screen sizes:**
1. Mobile (320px - 640px)
2. Tablet (641px - 1024px)
3. Desktop (1025px+)

**Mobile-first approach:**
Start with mobile classes, then add `md:` and `lg:` prefixes for larger screens.

**Example:**
```html
<!-- Good: Starts mobile, adds styles for larger screens -->
<h1 class="text-2xl md:text-3xl lg:text-4xl">Heading</h1>

<!-- Bad: Only works on large screens -->
<h1 class="lg:text-4xl">Heading</h1>
```

---

## Fixing Broken Links

### Step 1: Identify All Links in the Page

Links in this landing page are in three main areas:

1. **Navigation Menu** (Header)
2. **Call-to-Action (CTA) Buttons** (Throughout the page)
3. **Footer Links**

### Step 2: Understand Link Types

#### Internal Links (Within Your Site)
These use `#` to link to sections on the same page:
```html
<a href="#features">Features</a>
```

This links to:
```html
<section id="features">...</section>
```

#### External Links (Outside Your Site)
These use full URLs:
```html
<a href="https://led.com">Shop Now</a>
```

### Step 3: Find and Fix All Links

#### Navigation Menu Links

**Location**: Lines 116-121 (Desktop) and 140-144 (Mobile)

**Current links:**
```html
<a href="#features" class="text-gray-700 hover:text-gray-900 font-medium smooth-transition text-sm">Features</a>
<a href="#benefits" class="text-gray-700 hover:text-gray-900 font-medium smooth-transition text-sm">Benefits</a>
<a href="#faq" class="text-gray-700 hover:text-gray-900 font-medium smooth-transition text-sm">FAQ</a>
<a href="#contact" class="text-gray-700 hover:text-gray-900 font-medium smooth-transition text-sm">Contact</a>
```

**These links work if the corresponding sections exist on your page:**
- `#features` → `<section id="features">` (Line 189)
- `#benefits` → `<section id="benefits">` (Line 316)
- `#faq` → `<section id="faq">` (Line 549)
- `#contact` → `<footer id="contact">` (Line 707)

✅ **These are correct and don't need fixing.**

#### "Shop Now" Button Links

**Location**: Multiple locations (Lines 127, 145, 173, 341, 371, 402, 448)

**Current link:**
```html
<a href="https://led.com" class="btn-primary inline-flex items-center px-6 py-2.5 bg-gray-900 text-white font-semibold rounded-full hover:bg-gray-800 smooth-transition">
    Shop Now
    <i class="fas fa-arrow-right ml-2"></i>
</a>
```

**To fix this link:**
1. Replace `https://led.com` with your actual shop URL:

```html
<a href="https://your-shop-domain.com" class="btn-primary inline-flex items-center px-6 py-2.5 bg-gray-900 text-white font-semibold rounded-full hover:bg-gray-800 smooth-transition">
    Shop Now
    <i class="fas fa-arrow-right ml-2"></i>
</a>
```

**Example with Shopify:**
```html
<a href="https://myshop.myshopify.com" class="btn-primary...">
```

**Example with WooCommerce:**
```html
<a href="https://mywebsite.com/shop" class="btn-primary...">
```

**⚠️ Important**: There are **7 instances** of this link. You must update all of them:
- Line 127 (Header desktop)
- Line 145 (Header mobile)
- Line 173 (Hero section)
- Line 341 (Benefits - Free Delivery)
- Line 371 (Benefits - Fast Shipping)
- Line 402 (Benefits - High Quality)
- Line 448 (CTA Section)

**Quick way to find them all:**
1. Press `Ctrl+F` (or `Cmd+F` on Mac)
2. Search for `https://led.com`
3. Replace each instance with your shop URL

#### Footer Links

**Location**: Lines 740-765

**Quick Links section:**
```html
<li>
    <a href="#features" class="text-gray-400 hover:text-white smooth-transition">Features</a>
</li>
<li>
    <a href="#benefits" class="text-gray-400 hover:text-white smooth-transition">Benefits</a>
</li>
<li>
    <a href="#faq" class="text-gray-400 hover:text-white smooth-transition">FAQ</a>
</li>
<li>
    <a href="https://led.com" class="text-gray-400 hover:text-white smooth-transition">Shop</a>
</li>
<li>
    <a href="#" class="text-gray-400 hover:text-white smooth-transition">Blog</a>
</li>
```

**Issues to fix:**
1. The "Shop" link points to `https://led.com` (should be your shop URL)
2. The "Blog" link points to `#` (broken - needs a real link or page)

**How to fix:**

1. **Update Shop link:**
```html
<li>
    <a href="https://your-shop-domain.com" class="text-gray-400 hover:text-white smooth-transition">Shop</a>
</li>
```

2. **Fix Blog link** (Option A - if you have a blog):
```html
<li>
    <a href="https://your-domain.com/blog" class="text-gray-400 hover:text-white smooth-transition">Blog</a>
</li>
```

**Or Option B - if you don't have a blog yet:**
```html
<li>
    <a href="#" class="text-gray-400 hover:text-white smooth-transition cursor-not-allowed opacity-50">Blog</a>
</li>
```

**Support Links section:**
```html
<li>
    <a href="#" class="text-gray-400 hover:text-white smooth-transition">Contact Us</a>
</li>
<li>
    <a href="#" class="text-gray-400 hover:text-white smooth-transition">Shipping Info</a>
</li>
<li>
    <a href="#" class="text-gray-400 hover:text-white smooth-transition">Returns</a>
</li>
<li>
    <a href="#" class="text-gray-400 hover:text-white smooth-transition">Warranty</a>
</li>
<li>
    <a href="#" class="text-gray-400 hover:text-white smooth-transition">Track Order</a>
</li>
```

**How to fix these:**
Each `#` should point to a real page or section. Examples:

```html
<li>
    <a href="https://your-domain.com/contact" class="text-gray-400 hover:text-white smooth-transition">Contact Us</a>
</li>
<li>
    <a href="https://your-domain.com/shipping" class="text-gray-400 hover:text-white smooth-transition">Shipping Info</a>
</li>
<li>
    <a href="https://your-domain.com/returns" class="text-gray-400 hover:text-white smooth-transition">Returns</a>
</li>
<li>
    <a href="https://your-domain.com/warranty" class="text-gray-400 hover:text-white smooth-transition">Warranty</a>
</li>
<li>
    <a href="https://your-domain.com/track" class="text-gray-400 hover:text-white smooth-transition">Track Order</a>
</li>
```

#### Contact Information Links

**Location**: Lines 770-785

**Email link:**
```html
<li class="flex items-start">
    <i class="fas fa-envelope text-gray-500 mr-3 mt-1 flex-shrink-0"></i>
    <a href="mailto:admin@led.com" class="text-gray-400 hover:text-white smooth-transition break-all">admin@led.com</a>
</li>
```

**How to fix:**
Replace `admin@led.com` with your email:
```html
<a href="mailto:your-email@domain.com" class="text-gray-400 hover:text-white smooth-transition break-all">your-email@domain.com</a>
```

**Phone link:**
```html
<li class="flex items-start">
    <i class="fas fa-phone text-gray-500 mr-3 mt-1 flex-shrink-0"></i>
    <a href="tel:+1-800-LED-PHOTO" class="text-gray-400 hover:text-white smooth-transition">+1-800-LED-PHOTO</a>
</li>
```

**How to fix:**
Replace the phone number:
```html
<a href="tel:+1-800-YOUR-NUMBER" class="text-gray-400 hover:text-white smooth-transition">+1-800-YOUR-NUMBER</a>
```

#### Bottom Footer Links

**Location**: Lines 799-805

```html
<a href="#" class="text-gray-500 hover:text-gray-400 smooth-transition text-sm">Privacy Policy</a>
<a href="#" class="text-gray-500 hover:text-gray-400 smooth-transition text-sm">Terms of Service</a>
<a href="#" class="text-gray-500 hover:text-gray-400 smooth-transition text-sm">Cookie Settings</a>
```

**⚠️ These are broken and need fixing.** See the next section for detailed instructions.

---

## Linking Privacy and Terms Pages

### Step 1: Create the Policy Pages

First, you need to create the actual policy pages. Create two new HTML files in the same folder as your `index.html`:

#### Create `privacy.html`

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Privacy Policy - Photography Is Us">
    <title>Privacy Policy - Photography Is Us</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Sora:wght@300;400;500;600;700&display=swap');
        * {
            font-family: 'Sora', sans-serif;
        }
    </style>
</head>
<body class="bg-white text-gray-900">
    <!-- Header (Copy from index.html) -->
    <header class="sticky top-0 z-50 w-full bg-white border-b border-gray-200 shadow-sm">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex items-center justify-between">
            <div class="flex items-center space-x-2">
                <i class="fas fa-camera text-gray-900 text-2xl"></i>
                <span class="text-xl md:text-2xl font-bold text-gray-900 tracking-tight">Photography Is Us</span>
            </div>
            <div class="hidden md:flex items-center space-x-8">
                <a href="index.html#features" class="text-gray-700 hover:text-gray-900 font-medium text-sm">Features</a>
                <a href="index.html#benefits" class="text-gray-700 hover:text-gray-900 font-medium text-sm">Benefits</a>
                <a href="index.html#faq" class="text-gray-700 hover:text-gray-900 font-medium text-sm">FAQ</a>
                <a href="index.html#contact" class="text-gray-700 hover:text-gray-900 font-medium text-sm">Contact</a>
            </div>
            <div class="hidden md:block">
                <a href="https://your-shop-domain.com" class="inline-flex items-center px-6 py-2.5 bg-gray-900 text-white font-semibold rounded-full hover:bg-gray-800">
                    Shop Now
                    <i class="fas fa-arrow-right ml-2"></i>
                </a>
            </div>
        </nav>
    </header>

    <!-- Main Content -->
    <section class="w-full py-16 md:py-24 px-4 sm:px-6 lg:px-8 bg-white">
        <div class="max-w-4xl mx-auto">
            <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-8">Privacy Policy</h1>
            
            <div class="prose prose-lg text-gray-600 space-y-6">
                <h2 class="text-2xl font-bold text-gray-900 mt-8">Introduction</h2>
                <p>
                    Photography Is Us ("we," "us," "our," or "Company") is committed to protecting your privacy. This Privacy Policy explains how we collect, use, disclose, and safeguard your information when you visit our website.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">Information We Collect</h2>
                <p>
                    We may collect information about you in a variety of ways. The information we may collect on the site includes:
                </p>
                <ul class="list-disc pl-6 space-y-2">
                    <li>Personal Data: Personally identifiable information, such as your name, shipping address, email address, and telephone number, that you voluntarily give to us when you register with the site or when you choose to participate in various activities related to the site.</li>
                    <li>Financial Data: Financial information, such as data related to your payment method (e.g., valid credit card number, card brand, expiration date) that we may collect when you purchase, order, return, exchange, or request information about our services from the site.</li>
                    <li>Data From Social Networks: User information from social networks, including your name, your social network username, location, gender, birth date, email address, profile picture, and any other information you choose to make public.</li>
                </ul>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">Use of Your Information</h2>
                <p>
                    Having accurate information about you permits us to provide you with a smooth, efficient, and customized experience. Specifically, we may use information collected about you via the site to:
                </p>
                <ul class="list-disc pl-6 space-y-2">
                    <li>Generate a personal profile about you so that future visits to the site will be personalized as possible.</li>
                    <li>Increase the efficiency and operation of the site.</li>
                    <li>Monitor and analyze usage and trends to improve your experience with the site.</li>
                    <li>Notify you of updates to the site.</li>
                    <li>Perform other business activities as needed.</li>
                </ul>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">Disclosure of Your Information</h2>
                <p>
                    We may share information we have collected about you in certain situations:
                </p>
                <ul class="list-disc pl-6 space-y-2">
                    <li>By Law or to Protect Rights: If we believe the release of information is necessary to comply with the law.</li>
                    <li>Third-Party Service Providers: We may share your information with third parties that perform services for us or with us, including payment processors, data analysis providers, email delivery services, customer service, and marketing assistance.</li>
                </ul>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">Security of Your Information</h2>
                <p>
                    We use administrative, technical, and physical security measures to protect your personal information. However, perfect security does not exist on the Internet.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">Contact Us</h2>
                <p>
                    If you have questions or comments about this Privacy Policy, please contact us at:
                </p>
                <p>
                    Email: <a href="mailto:admin@led.com" class="text-blue-600 hover:text-blue-800">admin@led.com</a>
                </p>

                <p class="text-sm text-gray-500 mt-8">
                    Last Updated: January 2024
                </p>
            </div>
        </div>
    </section>

    <!-- Footer (Copy from index.html) -->
    <footer class="w-full bg-gray-900 text-gray-300 pt-16 md:pt-24 pb-8">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-4 gap-8 md:gap-12 mb-12">
                <div>
                    <div class="flex items-center space-x-2 mb-6">
                        <i class="fas fa-camera text-white text-2xl"></i>
                        <span class="text-xl font-bold text-white">Photography Is Us</span>
                    </div>
                </div>
                <div>
                    <h4 class="text-lg font-bold text-white mb-6">Quick Links</h4>
                    <ul class="space-y-3">
                        <li><a href="index.html#features" class="text-gray-400 hover:text-white">Features</a></li>
                        <li><a href="index.html#benefits" class="text-gray-400 hover:text-white">Benefits</a></li>
                        <li><a href="index.html#faq" class="text-gray-400 hover:text-white">FAQ</a></li>
                    </ul>
                </div>
                <div>
                    <h4 class="text-lg font-bold text-white mb-6">Support</h4>
                    <ul class="space-y-3">
                        <li><a href="privacy.html" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
                        <li><a href="terms.html" class="text-gray-400 hover:text-white">Terms of Service</a></li>
                    </ul>
                </div>
                <div>
                    <h4 class="text-lg font-bold text-white mb-6">Contact</h4>
                    <ul class="space-y-4">
                        <li class="flex items-start">
                            <i class="fas fa-envelope text-gray-500 mr-3 mt-1"></i>
                            <a href="mailto:admin@led.com" class="text-gray-400 hover:text-white">admin@led.com</a>
                        </li>
                    </ul>
                </div>
            </div>
            <div class="border-t border-gray-800 my-12"></div>
            <div class="flex flex-col md:flex-row items-center justify-between gap-6">
                <p class="text-gray-500 text-sm">
                    &copy; 2024 Photography Is Us. All rights reserved.
                </p>
                <div class="flex items-center space-x-6">
                    <a href="privacy.html" class="text-gray-500 hover:text-gray-400 text-sm">Privacy Policy</a>
                    <a href="terms.html" class="text-gray-500 hover:text-gray-400 text-sm">Terms of Service</a>
                </div>
            </div>
        </div>
    </footer>
</body>
</html>
```

#### Create `terms.html`

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Terms of Service - Photography Is Us">
    <title>Terms of Service - Photography Is Us</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Sora:wght@300;400;500;600;700&display=swap');
        * {
            font-family: 'Sora', sans-serif;
        }
    </style>
</head>
<body class="bg-white text-gray-900">
    <!-- Header (Copy from index.html) -->
    <header class="sticky top-0 z-50 w-full bg-white border-b border-gray-200 shadow-sm">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex items-center justify-between">
            <div class="flex items-center space-x-2">
                <i class="fas fa-camera text-gray-900 text-2xl"></i>
                <span class="text-xl md:text-2xl font-bold text-gray-900 tracking-tight">Photography Is Us</span>
            </div>
            <div class="hidden md:flex items-center space-x-8">
                <a href="index.html#features" class="text-gray-700 hover:text-gray-900 font-medium text-sm">Features</a>
                <a href="index.html#benefits" class="text-gray-700 hover:text-gray-900 font-medium text-sm">Benefits</a>
                <a href="index.html#faq" class="text-gray-700 hover:text-gray-900 font-medium text-sm">FAQ</a>
                <a href="index.html#contact" class="text-gray-700 hover:text-gray-900 font-medium text-sm">Contact</a>
            </div>
            <div class="hidden md:block">
                <a href="https://your-shop-domain.com" class="inline-flex items-center px-6 py-2.5 bg-gray-900 text-white font-semibold rounded-full hover:bg-gray-800">
                    Shop Now
                    <i class="fas fa-arrow-right ml-2"></i>
                </a>
            </div>
        </nav>
    </header>

    <!-- Main Content -->
    <section class="w-full py-16 md:py-24 px-4 sm:px-6 lg:px-8 bg-white">
        <div class="max-w-4xl mx-auto">
            <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-8">Terms of Service</h1>
            
            <div class="prose prose-lg text-gray-600 space-y-6">
                <h2 class="text-2xl font-bold text-gray-900 mt-8">Agreement to Terms</h2>
                <p>
                    These Website Standard Terms and Conditions (these "Terms" or these "Terms and Conditions") contained herein on this webpage, shall govern your use of this website, including all pages within this website (collectively referred to herein as the "Website"). These Terms and Conditions are in addition to any terms and conditions of sale which appear on this Website. If you disagree with any part of these terms and conditions, then you may not use this website.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">Use License</h2>
                <p>
                    Permission is granted to temporarily download one copy of the materials (information or software) on Photography Is Us's Website for personal, non-commercial transitory viewing only. This is the grant of a license, not a transfer of title, and under this license you may not:
                </p>
                <ul class="list-disc pl-6 space-y-2">
                    <li>Modifying or copying the materials</li>
                    <li>Using the materials for any commercial purpose or for any public display</li>
                    <li>Attempting to decompile or reverse engineer any software contained on the Website</li>
                    <li>Removing any copyright or other proprietary notations from the materials</li>
                    <li>Transferring the materials to another person or "mirroring" the materials on any other server</li>
                </ul>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">Disclaimer</h2>
                <p>
                    The materials on Photography Is Us's Website are provided on an 'as is' basis. Photography Is Us makes no warranties, expressed or implied, and hereby disclaims and negates all other warranties including, without limitation, implied warranties or conditions of merchantability, fitness for a particular purpose, or non-infringement of intellectual property or other violation of rights.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">Limitations</h2>
                <p>
                    In no event shall Photography Is Us or its suppliers be liable for any damages (including, without limitation, damages for loss of data or profit, or due to business interruption) arising out of the use or inability to use the materials on Photography Is Us's Website.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">Accuracy of Materials</h2>
                <p>
                    The materials appearing on Photography Is Us's Website could include technical, typographical, or photographic errors. Photography Is Us does not warrant that any of the materials on its Website are accurate, complete, or current. Photography Is Us may make changes to the materials contained on its Website at any time without notice.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">Links</h2>
                <p>
                    Photography Is Us has not reviewed all of the sites linked to its Website and is not responsible for the contents of any such linked site. The inclusion of any link does not imply endorsement by Photography Is Us of the site. Use of any such linked website is at the user's own risk.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">Modifications</h2>
                <p>
                    Photography Is Us may revise these Terms and Conditions for its Website at any time without notice. By using this Website, you are agreeing to be bound by the then current version of these Terms and Conditions.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">Governing Law</h2>
                <p>
                    These Terms and Conditions are governed by and construed in accordance with the laws of the jurisdiction where Photography Is Us is located, and you irrevocably submit to the exclusive jurisdiction of the courts in that location.
                </p>

                <p class="text-sm text-gray-500 mt-8">
                    Last Updated: January 2024
                </p>
            </div>
        </div>
    </section>

    <!-- Footer (Copy from index.html) -->
    <footer class="w-full bg-gray-900 text-gray-300 pt-16 md:pt-24 pb-8">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-4 gap-8 md:gap-12 mb-12">
                <div>
                    <div class="flex items-center space-x-2 mb-6">
                        <i class="fas fa-camera text-white text-2xl"></i>
                        <span class="text-xl font-bold text-white">Photography Is Us</span>
                    </div>
                </div>
                <div>
                    <h4 class="text-lg font-bold text-white mb-6">Quick Links</h4>
                    <ul class="space-y-3">
                        <li><a href="index.html#features" class="text-gray-400 hover:text-white">Features</a></li>
                        <li><a href="index.html#benefits" class="text-gray-400 hover:text-white">Benefits</a></li>
                        <li><a href="index.html#faq" class="text-gray-400 hover:text-white">FAQ</a></li>
                    </ul>
                </div>
                <div>
                    <h4 class="text-lg font-bold text-white mb-6">Support</h4>
                    <ul class="space-y-3">
                        <li><a href="privacy.html" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
                        <li><a href="terms.html" class="text-gray-400 hover:text-white">Terms of Service</a></li>
                    </ul>
                </div>
                <div>
                    <h4 class="text-lg font-bold text-white mb-6">Contact</h4>
                    <ul class="space-y-4">
                        <li class="flex items-start">
                            <i class="fas fa-envelope text-gray-500 mr-3 mt-1"></i>
                            <a href="mailto:admin@led.com" class="text-gray-400 hover:text-white">admin@led.com</a>
                        </li>
                    </ul>
                </div>
            </div>
            <div class="border-t border-gray-800 my-12"></div>
            <div class="flex flex-col md:flex-row items-center justify-between gap-6">
                <p class="text-gray-500 text-sm">
                    &copy; 2024 Photography Is Us. All rights reserved.
                </p>
                <div class="flex items-center space-x-6">
                    <a href="privacy.html" class="text-gray-500 hover:text-gray-400 text-sm">Privacy Policy</a>
                    <a href="terms.html" class="text-gray-500 hover:text-gray-400 text-sm">Terms of Service</a>
                </div>
            </div>
        </div>
    </footer>
</body>
</html>
```

### Step 2: Update Footer Links in index.html

Now update the links in your `index.html` footer to point to these new pages.

**Location**: Lines 799-805

**Current code:**
```html
<a href="#" class="text-gray-500 hover:text-gray-400 smooth-transition text-sm">Privacy Policy</a>
<a href="#" class="text-gray-500 hover:text-gray-400 smooth-transition text-sm">Terms of Service</a>
<a href="#" class="text-gray-500 hover:text-gray-400 smooth-transition text-sm">Cookie Settings</a>
```

**Replace with:**
```html
<a href="privacy.html" class="text-gray-500 hover:text-gray-400 smooth-transition text-sm">Privacy Policy</a>
<a href="terms.html" class="text-gray-500 hover:text-gray-400 smooth-transition text-sm">Terms of Service</a>
<a href="#" class="text-gray-500 hover:text-gray-400 smooth-transition text-sm cursor-not-allowed opacity-50">Cookie Settings</a>
```

### Step 3: Update Additional Footer Links

**Location**: Lines 740-765 (Support section)

**Current code:**
```html
<li>
    <a href="#" class="text-gray-400 hover:text-white smooth-transition">Contact Us</a>
</li>
```

**Update all support links:**
```html
<li>
    <a href="#contact" class="text-gray-400 hover:text-white smooth-transition">Contact Us</a>
</li>
<li>
    <a href="privacy.html" class="text-gray-400 hover:text-white smooth-transition">Privacy Policy</a>
</li>
<li>
    <a href="terms.html" class="text-gray-400 hover:text-white smooth-transition">Terms of Service</a>
</li>
```

### Step 4: File Structure

Your website folder should now look like this:

```
your-website-folder/
├── index.html          (Main landing page)
├── privacy.html        (Privacy Policy page)
├── terms.html          (Terms of Service page)
└── README.md           (Optional - documentation)
```

### Step 5: Test Your Links

1. Open `index.html` in your browser
2. Scroll to the footer
3. Click on "Privacy Policy" - it should open `privacy.html`
4. Click on "Terms of Service" - it should open `terms.html`
5. From those pages, you should be able to click links back to `index.html`

---

## Troubleshooting

### Problem: Links Don't Work

**Symptom:** Clicking a link does nothing or shows a 404 error.

**Solution:**
1. Check the `href` attribute matches the actual URL or file name
2. Ensure file names match exactly (case-sensitive on some servers)
3. For external links, include the full URL with `https://`

**Example of correct links:**
```html
<!-- Internal link to section -->
<a href="#features">Features</a>

<!-- Internal link to file -->
<a href="privacy.html">Privacy</a>

<!-- External link -->
<a href="https://example.com">External Site</a>
```

---

### Problem: Responsive Design Breaks on Mobile

**Symptom:** Page looks bad on phone or tablet.

**Solution:**
1. Check that you have the viewport meta tag in the `<head>`:
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

2. Ensure you're using responsive Tailwind classes:
```html
<!-- Good - responsive -->
<h1 class="text-2xl md:text-3xl lg:text-4xl">Heading</h1>

<!-- Bad - only works on large screens -->
<h1 class="lg:text-4xl">Heading</h1>
```

3. Test on actual devices or use browser developer tools (F12 key)

---

### Problem: Colors Don't Match

**Symptom:** Changed a color class but it doesn't appear.

**Solution:**
1. Clear browser cache (Ctrl+Shift+Delete or Cmd+Shift+Delete)
2. Verify the Tailwind class name is correct:
   - `bg-blue-600` (correct)
   - `bg-blue` (incorrect - missing number)
   - `blue-600` (incorrect - missing `bg-` or `text-`)

3. Check that you're using valid Tailwind colors:
   - Valid: `50`, `100`, `200`, `300`, `400`, `500`, `600`, `700`, `800`, `900`
   - Invalid: `150`, `250`, `350`

---

### Problem: Newsletter Form Doesn't Work

**Symptom:** Submitting the form does nothing or shows an error.

**Solution:**
The current form only shows a "Subscribed!" message. To make it actually work, you need a backend service. Options:

**Option 1: Use Mailchimp (Free)**
1. Go to [Mailchimp.com](https://mailchimp.com)
2. Create a free account
3. Set up an audience and get the form action URL
4. Update the form in your HTML:

```html
<form action="https://your-mailchimp-url" method="post" class="flex flex-col sm:flex-row gap-3 max-w-2xl mx-auto">
    <input 
        type="email" 
        name="EMAIL"
        placeholder="Enter your email address" 
        required
        class="flex-1 px-6 py-3 md:py-4 bg-white text-gray-900 rounded-full placeholder-gray-500 focus:outline-none focus:ring-2 focus:ring-gray-400 text-base"
    >
    <button 
        type="submit"
        class="btn-primary px-8 py-3 md:py-4 bg-gray-100 text-gray-900 font-semibold rounded-full hover:bg-gray-200 smooth-transition whitespace-nowrap"
    >
        Subscribe
    </button>
</form>
```

**Option 2: Use ConvertKit (Recommended for creators)**
Similar process - sign up, get form code, integrate it.

---

### Problem: Images Don't Load

**Symptom:** Hero section or benefit sections show no images.

**Solution:**
The current images use Unsplash URLs. If they don't load:

1. Check your internet connection
2. The Unsplash URL might have changed
3. Replace with your own image:

```html
<!-- Current (Unsplash) -->
<section class="relative w-full h-screen md:h-[600px] bg-cover bg-center flex items-center justify-center overflow-hidden" style="background-image: url('https://images.unsplash.com/photo-1504093376055-b3094b674dcb?w=1600&h=900&fit=crop&q=80');">

<!-- Your own image -->
<section class="relative w-full h-screen md:h-[600px] bg-cover bg-center flex items-center justify-center overflow-hidden" style="background-image: url('your-image.jpg');">
```

**To add your own image:**
1. Save your image in the same folder as `index.html`
2. Reference it by filename:
```html
style="background-image: url('my-photo.jpg');"
```

---

### Problem: Accordion (FAQ) Doesn't Open/Close

**Symptom:** Clicking FAQ questions doesn't expand answers.

**Solution:**
1. Check that JavaScript is enabled in your browser
2. Verify the `onclick="toggleAccordion(this)"` is present on the button
3. Check browser console for errors (F12 → Console tab)

The accordion JavaScript code is at the bottom of `index.html` (lines 838-863). Make sure it's not removed.

---

### Problem: Mobile Menu Doesn't Work

**Symptom:** Hamburger menu doesn't open on mobile.

**Solution:**
1. Check that the button has `id="mobileMenuBtn"`
2. Verify the menu div has `id="mobileMenu"`
3. Ensure JavaScript code is present (lines 838-863)
4. Test on actual mobile device or use browser's mobile view (F12)

---

### Problem: Text Overflows Container

**Symptom:** Long text runs off the edge of the screen.

**Solution:**
Add `max-w-` class to constrain width:

```html
<!-- Before (might overflow) -->
<h1 class="text-4xl font-bold">Your very long heading text</h1>

<!-- After (constrained) -->
<h1 class="text-4xl font-bold max-w-4xl">Your very long heading text</h1>
```

Or use `break-words` or `truncate`:
```html
<!-- Allow text to wrap -->
<p class="break-words">Long text</p>

<!-- Truncate with ellipsis -->
<p class="truncate">Long text that gets cut off...</p>
```

---

## Best Practices

### 1. Always Keep Backups
Before making changes:
```bash
# Copy your file
cp index.html index.html.backup
```

### 2. Test Changes in Multiple Browsers
- Chrome
- Firefox
- Safari
- Edge

### 3. Test on Multiple Devices
- Desktop (1920px)
- Tablet (768px)
- Mobile (375px)

### 4. Use Browser Developer Tools
Press `F12` to open developer tools:
- **Elements tab**: Inspect HTML and CSS
- **Console tab**: See JavaScript errors
- **Responsive Design Mode**: Test different screen sizes

### 5. Validate Your HTML
Use [W3C Validator](https://validator.w3.org/) to check for errors:
1. Go to the website
2. Paste your HTML
3. Fix any reported errors

### 6. Keep Your Links Updated
Maintain a list of all external links:
- Shop URL
- Contact email
- Social media
- Policy pages

Update them all if any change.

### 7. Organize Your File Structure
```
website/
├── index.html
├── privacy.html
├── terms.html
├── images/
│   ├── logo.png
│   ├── hero.jpg
│   └── feature-1.jpg
└── css/
    └── custom.css (if you add custom styles)
```

### 8. Use Descriptive Link Text
**Bad:**
```html
<a href="privacy.html">Click here</a>
```

**Good:**
```html
<a href="privacy.html">Read our Privacy Policy</a>
```

This helps both users and search engines understand where the link goes.

### 9. Keep Content Updated
- Update testimonials regularly
- Refresh product information
- Update contact details
- Check all links monthly

### 10. Monitor Performance
- Keep image file sizes small (compress before uploading)
- Minimize the number of external scripts
- Test page load speed at [GTmetrix](https://gtmetrix.com/)

---

## Quick Reference Guide

### Common Tasks

**Change brand name:**
- Line 113: Update `<span>Photography Is Us</span>`
- Line 161: Update `<h1>Photography Is Us</h1>`
- Line 718: Update `<span>Photography Is Us</span>`

**Update shop link:**
- Find all instances of `https://led.com`
- Replace with your shop URL
- Use `Ctrl+F` to find all (7 instances)

**Change button color:**
- Find `bg-gray-900` in button classes
- Replace with `bg-blue-600` or your preferred color
- Also update `hover:bg-gray-800` to `hover:bg-blue-700`

**Add new section:**
1. Copy an existing section (e.g., features)
2. Paste it in desired location
3. Update all text and IDs
4. Add link to navigation menu

**Update footer:**
- Company info: Lines 717-730
- Quick links: Lines 732-742
- Support links: Lines 744-754
- Contact: Lines 756-785

---

## Getting Help

### Resources
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [Font Awesome Icons](https://fontawesome.com/icons)
- [MDN Web Docs](https://developer.mozilla.org/) (HTML/CSS reference)
- [Stack Overflow](https://stackoverflow.com/) (Ask questions)

### Common Questions

**Q: How do I change the logo?**
A: Replace the `<i class="fas fa-camera"></i>` with a different Font Awesome icon or add an `<img>` tag.

**Q: Can I add more sections?**
A: Yes! Copy an existing section, update the ID