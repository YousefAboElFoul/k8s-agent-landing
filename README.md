# K8s Self-Healing Agent - Landing Website

A professional, modern website for K8s Self-Healing Agent - an AI-powered platform for automatic Kubernetes pod failure detection and resolution.

## 🌐 Website Structure

### Pages
- **index.html** - Professional homepage with hero section, features, benefits, and CTA
- **pages/booking.html** - Interactive demo booking system with calendar and time slots
- **pages/pricing.html** - Detailed pricing plans (Open Source, Hosted, Enterprise) with feature comparison
- **pages/about.html** - Company story, mission, values, team, and testimonials
- **pages/contact.html** - Contact form, office locations, and support information
- **css/styles.css** - Professional styling system with gradient themes and responsive design

## ✨ Key Features

### Professional Design
- Modern gradient color scheme (Indigo to Purple)
- Responsive design for all devices
- Smooth scrolling and transitions
- Professional typography and spacing

### Interactive Elements
- **Booking System**: Calendar picker with available time slots, form validation
- **Contact Forms**: Multiple contact forms with success messages
- **Feature Cards**: Grid-based card layouts with hover effects
- **FAQ Sections**: Expandable FAQ items throughout

### SEO & Accessibility
- Proper semantic HTML structure
- Meta tags for each page
- Clear navigation hierarchy
- Accessible form labels and inputs

## 🎨 Design System

### Colors
- Primary: Indigo (`#4f46e5`)
- Secondary: Purple (`#7c3aed`)
- Success: Green (`#10b981`)
- Danger: Red (`#ef4444`)
- Dark: `#1f2937`
- Light: `#f9fafb`

### Components
- **Cards**: Information cards with hover effects
- **Buttons**: Primary (gradient), Secondary (outline), CTA
- **Forms**: Styled input fields, textareas, selects with focus states
- **Grids**: Responsive grid layouts (1, 2, 3 columns)
- **Sections**: Full-width sections with alternating backgrounds

## 🚀 Getting Started

### Local Development
Simply open `index.html` in a web browser. No build process or dependencies required.

```bash
# If using Python's simple HTTP server:
python -m http.server 8000

# If using Node.js http-server:
npx http-server
```

Then visit `http://localhost:8000`

### Project Layout
```
k8s-agent-landing/
├── index.html           # Homepage
├── css/
│   └── styles.css      # Global styles
├── pages/
│   ├── about.html      # About page
│   ├── booking.html    # Demo booking page
│   ├── contact.html    # Contact page
│   └── pricing.html    # Pricing page
└── README.md           # This file
```

## 📋 Page Details

### Homepage (index.html)
- **Hero Section**: Compelling headline and CTA buttons
- **Problems Section**: Shows pain points the product solves
- **Features Section**: 6 key features with icons
- **Process Section**: 4-step workflow visualization
- **CTA Section**: Call-to-action with booking link
- **Footer**: Complete footer with links and info

### Booking Page (pages/booking.html)
- **Interactive Calendar**: Selects available dates (weekdays only, future dates only)
- **Time Slots**: 13 available appointment times (9 AM - 5 PM EST)
- **Contact Form**: Collects name, email, phone, company, role, cluster count, interests
- **Form Validation**: Ensures date/time selection before submission
- **Success Message**: Confirmation after booking
- **Info Cards**: Benefits of the demo
- **FAQ Section**: Common questions about demos

### Pricing Page (pages/pricing.html)
- **3 Pricing Tiers**: Open Source ($0), Hosted ($99/cluster/mo), Enterprise (Custom)
- **Feature List**: Checkmarks for included features
- **Add-ons Section**: Premium features available separately
- **Comparison Table**: Full feature comparison across plans
- **FAQ Section**: Pricing-related questions with expand/collapse

### About Page (pages/about.html)
- **Company Story**: Background and mission
- **Mission & Values**: 6 core values with descriptions
- **Team Section**: Founding team members with bios
- **Why Choose Us**: 6 competitive advantages
- **Customer Testimonials**: 4 customer quotes
- **Tech Stack**: Technologies used (K8s, Go, Python, etc.)

### Contact Page (pages/contact.html)
- **Contact Cards**: Sales, support, partnerships with emails
- **Contact Form**: Subject line with predefined options
- **Office Locations**: SF office and remote-first info
- **FAQ Section**: Support and communication FAQs
- **Social Links**: GitHub, Twitter, LinkedIn, Slack community

## 🎯 Customization Guide

### Update Company Info
Edit footer and contact page with actual company details:
- Replace email addresses
- Update office locations
- Add actual social media links
- Update company name if needed

### Modify Pricing
Update `pages/pricing.html`:
- Change price amounts
- Add/remove features
- Modify plan names
- Update add-on pricing

### Update Team
Edit `pages/about.html`:
- Add/remove team members
- Update bios
- Replace placeholder circles with actual photos

### Customize Colors
Edit `css/styles.css` in the `:root` section:
```css
:root {
  --primary-color: #your-color;
  --secondary-color: #your-color;
  /* etc */
}
```

## 📱 Responsive Breakpoints

- Desktop: 1200px and above
- Tablet: 768px - 1200px
- Mobile: Below 768px

All layouts automatically adapt to screen size using CSS Grid and Flexbox.

## 🔧 Booking System Technical Details

The booking system uses vanilla JavaScript with:
- Calendar rendering for 42 days view
- Date validation (no past dates, no weekends)
- Time slot management
- Form data collection and validation
- Success/error messaging

To integrate with a backend:
1. Modify the `handleSubmit()` function in `pages/booking.html`
2. Add API call to send `formData` to your server
3. Connect to email service for confirmations
4. Add calendar service integration (Google Calendar, Calendly, etc.)

## 📧 Contact Form Integration

Both contact forms (`pages/contact.html` and `pages/booking.html`) need backend integration:
1. Add form submission handler to POST to your backend
2. Integrate with email service (SendGrid, Mailgun, etc.)
3. Add confirmation emails
4. Store inquiries in database

## 🔐 Security Notes

- Forms currently log to console and show success messages
- No data is sent to a server (needs backend integration)
- For production, ensure:
  - HTTPS for all connections
  - Server-side form validation
  - CSRF protection
  - Email verification
  - Rate limiting on forms

## 🎓 Best Practices Implemented

✅ Semantic HTML5  
✅ Mobile-first responsive design  
✅ CSS Grid and Flexbox layouts  
✅ Form validation and accessibility  
✅ Progressive enhancement  
✅ Performance optimized  
✅ No external dependencies  
✅ Easy to customize and extend  

## 🚀 Deployment

### Static Hosting Options
- GitHub Pages (free)
- Netlify (free tier available)
- Vercel (free tier available)
- AWS S3 + CloudFront
- Any static hosting service

### Steps to Deploy
1. Push to GitHub repository
2. Enable GitHub Pages or connect to Netlify/Vercel
3. Configure custom domain
4. Enable HTTPS
5. Add email backend for forms

## 📞 Support & Next Steps

### To Start Your Business
1. ✅ Website is ready for visitors
2. Update company information (emails, locations, team)
3. Set up email service for booking/contact forms
4. Connect booking calendar to your availability system
5. Set up analytics (Google Analytics, etc.)
6. Create payment/subscription system
7. Build product documentation

### For Production Launch
- [ ] Update all placeholder content
- [ ] Add actual team photos
- [ ] Set up email notifications
- [ ] Integrate payment processing
- [ ] Add analytics
- [ ] Set up automated responses
- [ ] Configure email forwarding
- [ ] Test all forms and links

---

**Ready to launch your Kubernetes reliability business! 🚀**