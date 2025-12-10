# 🌐 Website Architecture & Navigation Map

## Site Structure Diagram

```
K8s Agent Website
├── Homepage (index.html)
│   ├── Hero Section
│   ├── Problems Section
│   ├── Features Section
│   ├── Process Section
│   ├── Call-to-Action
│   └── Footer (all pages)
│
├── Booking Page (pages/booking.html)
│   ├── Calendar Selector
│   ├── Time Slot Selection
│   ├── Contact Form
│   ├── Info Cards
│   └── FAQ Section
│
├── Pricing Page (pages/pricing.html)
│   ├── 3 Pricing Tiers
│   ├── Add-ons Section
│   ├── Feature Comparison Table
│   ├── FAQ Section
│   └── CTA Section
│
├── About Page (pages/about.html)
│   ├── Company Story
│   ├── Mission & Values
│   ├── Team Section
│   ├── Hiring Section
│   ├── Testimonials
│   ├── Tech Stack
│   └── CTA Section
│
├── Contact Page (pages/contact.html)
│   ├── Contact Info Cards
│   ├── Contact Form
│   ├── Office Locations
│   ├── FAQ Section
│   ├── Social Links
│   └── CTA Section
│
└── CSS Styling (css/styles.css)
    ├── Global Styles
    ├── Navigation
    ├── Buttons & CTAs
    ├── Cards & Grids
    ├── Forms
    ├── Footer
    └── Responsive Breakpoints
```

## Navigation Flow

```
┌─────────────────────────────────────────┐
│         K8s Agent Logo / Home           │
├─────────────────────────────────────────┤
│ Features | Pricing | About | Contact    │
│                   [Book Demo] ← CTA     │
└─────────────────────────────────────────┘
            │
    ┌───────┼───────┬──────────┬─────────┐
    ▼       ▼       ▼          ▼         ▼
  HOME   PRICING ABOUT    CONTACT    BOOKING
  │        │       │         │         │
  └────┬───┴───┬───┴─────┬───┴────┬────┘
       │       │         │        │
    More    Compare   Story    Demo
    Info    Features   Team    Calendar
```

## Page Content Hierarchy

### Homepage
```
K8s Agent
├─ Hero (5 main sections)
│  ├─ Headline
│  ├─ Subheading
│  ├─ [Book Demo] [Learn More]
│  └─ Trust Badges
├─ Problems (4 pain points)
├─ Features (6 features)
├─ Process (4 steps)
└─ CTA Section
```

### Booking Page
```
Book Your Free Demo
├─ Calendar
│  ├─ Previous/Next
│  └─ Date Selection
├─ Time Slots (13 options)
├─ Contact Form
│  ├─ Name, Email, Phone
│  ├─ Company, Role, Clusters
│  ├─ Interests, Checkbox
│  └─ [Submit]
├─ Info Cards (3)
└─ FAQ (4 items)
```

### Pricing Page
```
Simple, Transparent Pricing
├─ 3 Pricing Cards
│  ├─ Open Source ($0)
│  ├─ Hosted ($99) ← Featured
│  └─ Enterprise (Custom)
├─ Add-ons (3 options)
├─ Feature Comparison Table
└─ FAQ (8 items)
```

### About Page
```
About K8s Self-Healing Agent
├─ Company Story
├─ Mission & Values (6)
├─ Team (3 members)
├─ Why Choose Us (6)
├─ Testimonials (4)
└─ Tech Stack (6 technologies)
```

### Contact Page
```
Get in Touch
├─ Contact Cards (3)
│  ├─ Sales
│  ├─ Support
│  └─ Partnerships
├─ Contact Form
├─ Office Locations (2)
├─ FAQ (6 items)
├─ Social Links (4)
└─ CTA Section
```

## User Journey Maps

### Visitor → Customer
```
Land on Homepage
    ↓
Read Problems/Features
    ↓
Click "Book Demo"
    ↓
Fill Booking Form
    ↓
Success Message
    ↓
Check Email
    ↓
Attend Demo
    ↓
Start Free Trial
```

### Pricing Research
```
Homepage
    ↓
Click "Pricing"
    ↓
Compare Plans
    ↓
Read FAQ
    ↓
Click CTA (Book Demo / Start Trial)
    ↓
Booking/Trial
```

### Support Seeker
```
Contact Page
    ↓
Read Support Options
    ↓
Submit Contact Form
    ↓
Check Email
    ↓
Get Response
```

## Component Inventory

### Buttons/CTAs
- Primary: Gradient background
- Secondary: Outline style
- Text links: Colored, no background

### Cards
- Feature Cards: Icon, heading, description
- Pricing Cards: Price, features list, CTA
- Info Cards: Icon, heading, description
- Testimonial Cards: Quote, attribution, company

### Forms
- Text inputs: Name, email, company, etc.
- Textarea: Message/interests
- Select/dropdown: Subject, clusters
- Checkbox: Agreement/subscription

### Sections
- Hero: Full-width, gradient background
- Content: Max-width 1200px, centered
- Cards: Grid layout (1, 2, or 3 columns)
- Footer: Multiple columns, links

## Responsive Breakpoints

```
Mobile (<768px)
├─ Stacked layout
├─ Full-width cards
├─ Single column forms
└─ Hamburger nav (if added)

Tablet (768px - 1024px)
├─ 2-column grids
├─ Flexible cards
├─ Readable forms
└─ Full nav

Desktop (1024px+)
├─ 3-column grids
├─ Max-width containers
├─ Hover effects
└─ Full nav
```

## Data Flow

### Booking Form
```
User Input
    ↓
JavaScript Validation
    ↓
Success Message (Client-side)
    ↓
[Needs: Backend/Email Service]
    ↓
Confirmation Email
    ↓
Calendar Sync (optional)
```

### Contact Form
```
User Input
    ↓
JavaScript Validation
    ↓
Success Message (Client-side)
    ↓
[Needs: Backend/Email Service]
    ↓
Admin Email Notification
```

## Interactive Elements Map

```
Homepage
├─ Navigation: Links to all pages
├─ Hero CTAs: [Book Demo] [Learn More]
├─ Card Hover: Elevation effect
├─ Footer Links: All pages + social
└─ Trust Badges: Display info

Booking
├─ Calendar: Date selection
├─ Time Slots: Time selection
├─ Form: Input validation
├─ Success: Message display
└─ FAQ: Expand/collapse

Pricing
├─ Cards: Hover effect
├─ Featured: Scale & highlight
├─ Table: Horizontal scroll on mobile
├─ FAQ: Expand/collapse
└─ CTAs: Navigation

About
├─ Cards: Hover effect
├─ Team: Display member info
├─ Testimonials: Cards
└─ CTAs: Navigation

Contact
├─ Cards: Hover effect
├─ Form: Input validation
├─ FAQ: Expand/collapse
├─ Social: Links
└─ CTAs: Navigation
```

## Technical Stack

```
Frontend
├─ HTML5: Semantic structure
├─ CSS3: Flexbox, Grid, Gradients
├─ JavaScript: Vanilla (no frameworks)
├─ Responsive: Mobile-first design
└─ Performance: No external deps

Backend (To Be Built)
├─ Server: Node.js / Python / etc.
├─ Database: PostgreSQL / MongoDB / etc.
├─ Email: SendGrid / Mailgun / etc.
├─ Calendar: Google Calendar / Calendly API
└─ Payment: Stripe / Paddle / etc.

Hosting Options
├─ Static: GitHub Pages / Netlify / Vercel
├─ Custom: Any web host with HTTPS
└─ CDN: Optional for performance
```

## SEO Structure

```
HTML Head (All Pages)
├─ <title>: Unique per page
├─ <meta name="description">: 160 chars
├─ <meta name="viewport">: Responsive
├─ Canonical URLs: No duplicates
└─ Open Graph: Social sharing

HTML Body
├─ <h1>: One per page
├─ <h2>: Section headings
├─ <h3>: Subsection headings
├─ <img alt="">: All images
├─ <a>: Descriptive text
└─ <form>: Proper labels
```

## Customization Points

```
Content Updates
├─ All pages: Company name, emails
├─ Pricing page: Prices, features
├─ About page: Team, testimonials
├─ Contact page: Office, phone
└─ Footer: All pages

Design Updates
├─ Colors: css/styles.css :root
├─ Fonts: Typography in css
├─ Logo: Navbar image/text
├─ Spacing: Padding/margin values
└─ Gradients: Color combinations

Functional Updates
├─ Forms: Email integration
├─ Booking: Calendar API
├─ Payment: Stripe integration
├─ Analytics: Google Analytics
└─ CRM: Lead capture
```

---

This diagram shows the complete architecture and how everything connects together!
