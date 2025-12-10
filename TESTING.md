# 🧪 Website Testing Guide

## Quick Test Checklist

Run through this checklist to verify everything works before launch.

### Page Loads
- [ ] `index.html` loads and displays correctly
- [ ] All navigation links work
- [ ] All pages load (home, pricing, about, booking, contact)
- [ ] No 404 errors in console
- [ ] No CSS errors (styling should be applied)

### Navigation
- [ ] Header navigation links go to correct pages
- [ ] Footer links work
- [ ] Logo links back to home
- [ ] "Book a Demo" buttons go to booking page
- [ ] Back buttons work (if added)

### Homepage (index.html)
- [ ] Hero section displays compelling headline
- [ ] CTAs are visible and clickable
- [ ] Trust badges show
- [ ] Problem cards display 2x2 grid
- [ ] Feature cards display 3x2 grid
- [ ] Process section shows 4 steps
- [ ] All buttons have proper styling and hover effects
- [ ] Footer displays correctly

### Booking Page (pages/booking.html)
- [ ] Calendar loads with current month
- [ ] Previous/Next month buttons work
- [ ] Can select available dates (no past dates, no weekends)
- [ ] Time slots appear after date selection
- [ ] Can select time slots
- [ ] Form fields are accessible
- [ ] Form validates (try submitting without date/time - should show error)
- [ ] Success message appears after submission
- [ ] Form resets after successful submission

**Test Cases:**
1. Try to submit without date - should alert
2. Try to submit without time - should alert
3. Try to submit without required fields - should alert
4. Complete booking successfully - success message appears

### Pricing Page (pages/pricing.html)
- [ ] 3 pricing cards display correctly
- [ ] Featured (Hosted) plan stands out
- [ ] Add-ons section displays 3 add-on cards
- [ ] Feature comparison table scrolls horizontally on mobile
- [ ] FAQ items expand/collapse on click
- [ ] All buttons have correct links
- [ ] Pricing amounts are clearly visible

**Check:**
- Feature checkmarks (✓) show for included features
- Feature crosses (✗) show for excluded features
- "Most Popular" badge on Hosted plan

### About Page (pages/about.html)
- [ ] Company story reads well
- [ ] Mission & Values cards display (6 cards)
- [ ] Team member cards show (3 members minimum)
- [ ] "We're hiring" section is visible
- [ ] Testimonials display (4 testimonials)
- [ ] Tech stack section shows technologies
- [ ] All images/colors display correctly

### Contact Page (pages/contact.html)
- [ ] Contact info cards display (3 cards)
- [ ] Contact form loads correctly
- [ ] Form fields are properly labeled
- [ ] Subject dropdown works
- [ ] Form validates required fields
- [ ] Success message appears after submission
- [ ] Office locations section displays
- [ ] FAQ items expand/collapse
- [ ] Social media links visible

**Test Cases:**
1. Try submit without required fields - should prevent
2. Try invalid email - should show HTML5 validation
3. Submit form - success message appears
4. Form should reset after submission

### Mobile Responsiveness (Test in DevTools)
- [ ] Test at 375px width (iPhone SE)
- [ ] Test at 768px width (iPad)
- [ ] Test at 1024px width (iPad Pro)
- [ ] All text is readable
- [ ] All buttons are easily clickable
- [ ] Navigation adapts for small screens
- [ ] Cards stack vertically on mobile
- [ ] Images/icons scale properly
- [ ] No horizontal scrolling (except intentional)

**Key points:**
- Navigation should be accessible on mobile
- Touch targets should be at least 44x44px
- Forms should not be cramped
- Calendar should work on touch devices

### Form Testing

#### Booking Form
- [ ] First name - required, text input
- [ ] Last name - required, text input
- [ ] Email - required, email validation
- [ ] Phone - required, tel input
- [ ] Company - required, text input
- [ ] Role - required, text input
- [ ] Clusters - optional, dropdown
- [ ] Interests - optional, textarea
- [ ] Terms checkbox - required

#### Contact Form
- [ ] First name - required
- [ ] Last name - required
- [ ] Email - required, email validation
- [ ] Phone - optional
- [ ] Company - required
- [ ] Subject - required, dropdown
- [ ] Message - required, textarea
- [ ] Subscribe checkbox - optional
- [ ] Submit button enables after form valid

### Visual Design
- [ ] Color scheme is consistent
- [ ] Gradients render properly
- [ ] Hover effects work on all interactive elements
- [ ] Shadows and borders look professional
- [ ] Font sizes are readable
- [ ] Line spacing is comfortable
- [ ] Card spacing is consistent
- [ ] No overlapping text or images

### Performance
- [ ] Pages load quickly (< 2 seconds)
- [ ] No console errors
- [ ] No console warnings
- [ ] Images are optimized
- [ ] No broken images
- [ ] CSS is loaded and applied

### Browser Compatibility
Test in:
- [ ] Chrome (latest)
- [ ] Firefox (latest)
- [ ] Safari (latest)
- [ ] Edge (latest)

All pages should work and look consistent.

### Accessibility
- [ ] All form labels are associated with inputs
- [ ] All images have alt text (or are decorative with alt="")
- [ ] Color contrast is sufficient (WCAG AA minimum)
- [ ] Can navigate with keyboard (Tab key)
- [ ] Focus indicators are visible
- [ ] Form errors are clearly marked

### Links & CTAs
Check all these links work:
- [ ] Home logo
- [ ] Navigation links
- [ ] All "Book a Demo" buttons
- [ ] Footer links
- [ ] Email links (mailto:)
- [ ] External links (should open in new tab)

### Content Quality
- [ ] No spelling errors
- [ ] No grammar issues
- [ ] Professional tone throughout
- [ ] Compelling value propositions
- [ ] Clear CTAs
- [ ] Consistent branding
- [ ] No placeholder text remaining

### SEO Basics
- [ ] Each page has unique `<title>` tag
- [ ] Each page has `<meta description>`
- [ ] Headings are structured (H1, H2, H3)
- [ ] Images have alt text
- [ ] URLs are descriptive
- [ ] Links have descriptive anchor text

## Testing Tools

### Browser Tools
- **Chrome DevTools** - F12
- **Firefox DevTools** - F12
- **Safari DevTools** - Cmd+Option+I

### Online Tools
- **Mobile View Tester** - https://responsivedesignchecker.com/
- **Lighthouse** - Built into Chrome DevTools
- **WebAIM Contrast Checker** - https://webaim.org/resources/contrastchecker/

## Common Issues & Fixes

### Pages Not Styled
**Problem:** HTML loads but CSS isn't applied
**Fix:** Check CSS file path in HTML `<link>` tag
```html
<link rel="stylesheet" href="../css/styles.css">
```
Make sure paths are relative and correct for each page.

### Forms Not Working
**Problem:** Submit button does nothing
**Fix:** JavaScript form handling is client-side only
To save data, you need backend integration
```javascript
// Currently shows success but doesn't send data
// You need to add API call here
```

### Calendar Issues
**Problem:** Calendar not showing dates
**Fix:** JavaScript might be disabled
Make sure you can see JavaScript running in console

### Mobile Layout Broken
**Problem:** Content overflows or doesn't wrap
**Fix:** Check viewport meta tag exists in `<head>`
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

### Links in Navbar Not Working
**Problem:** Pages aren't found
**Fix:** Check relative paths are correct
From `pages/booking.html` linking to `../index.html`

## Testing Scenarios

### Scenario 1: New Visitor Journey
1. Land on homepage
2. Read about features
3. Click "Book a Demo"
4. Schedule demo
5. Get confirmation

**Expected:** Smooth flow, all buttons work, forms submit

### Scenario 2: Pricing Investigation
1. Go to pricing page
2. Compare plans
3. Read FAQ
4. Click CTA for most popular plan

**Expected:** Easy comparison, FAQs helpful, CTA redirects properly

### Scenario 3: Contact Path
1. Go to contact page
2. Look for support info
3. Submit contact form
4. Get success message

**Expected:** Contact options clear, form validates, success shown

### Scenario 4: Mobile Browsing
1. Open site on phone
2. Navigate between pages
3. Try booking form on mobile
4. Submit contact form

**Expected:** Everything works on small screen, forms are usable

## Performance Metrics to Check

Using Chrome DevTools Lighthouse:
- [ ] Performance score > 80
- [ ] Accessibility score > 90
- [ ] Best Practices score > 90
- [ ] SEO score > 90

(Your static site should score very high!)

## Sign-Off Checklist

Before deploying:
- [ ] All test items above completed
- [ ] No errors in console
- [ ] Mobile tested on real device (not just DevTools)
- [ ] Navigation works end-to-end
- [ ] Forms validated properly
- [ ] Content reviewed and verified accurate
- [ ] Links tested and working
- [ ] Performance acceptable
- [ ] Accessibility verified

## Ready to Deploy?

If you checked everything above, you're ready! 🚀

See `QUICK_START.md` for deployment instructions.
