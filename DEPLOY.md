# 🚀 Deployment Checklist

Complete this before going live with your website.

## Pre-Deployment (Do This First)

### Content Review
- [ ] Update all company names/references
- [ ] Replace placeholder email addresses
- [ ] Update phone numbers
- [ ] Add office locations
- [ ] Add team member names and bios
- [ ] Update customer testimonials (or mark as examples)
- [ ] Check all spelling and grammar
- [ ] Verify all URLs and external links work
- [ ] Remove any "TODO" or placeholder text

### Testing
- [ ] Run through TESTING.md checklist
- [ ] Test on mobile device (not just DevTools)
- [ ] Test in multiple browsers
- [ ] Check all forms validate
- [ ] Verify all links work
- [ ] Test booking calendar
- [ ] Test contact/booking forms

### Branding
- [ ] Logo/wordmark finalized
- [ ] Color scheme finalized
- [ ] Company name consistent throughout
- [ ] Messaging aligned with business goals

## Domain Setup

### Choose Your Domain
- [ ] Domain name decided
- [ ] Domain purchased (.com, .io, .cloud, etc.)
- [ ] Domain registrar account created

### DNS Configuration
- [ ] DNS records configured for your hosting
- [ ] A records point to hosting provider
- [ ] CNAME records set if needed
- [ ] DNS propagation complete (can take 24-48 hours)

**Check DNS:** Use whatsmydns.net to verify

## Hosting Deployment

### Option 1: GitHub Pages (Easiest)

```bash
# Ensure you're in repo root
git add .
git commit -m "Website launch"
git push origin main
```

Then in GitHub:
1. Go to Settings → Pages
2. Source: Deploy from branch
3. Branch: main, folder: / (root)
4. Save
5. Wait 2-3 minutes for deployment

**Verification:**
- [ ] Site accessible at `https://username.github.io/repo-name`
- [ ] HTTPS enabled automatically
- [ ] All pages load

### Option 2: Netlify

1. [ ] Connect GitHub repo
2. [ ] Build settings:
   - Build command: (leave empty)
   - Publish directory: `/`
3. [ ] Deploy
4. [ ] Custom domain:
   - Domain settings → Add custom domain
   - Follow DNS instructions
5. [ ] HTTPS:
   - Should be automatic with Netlify certificate

**Verification:**
- [ ] Site accessible at netlify domain
- [ ] All pages load
- [ ] HTTPS works

### Option 3: Vercel

1. [ ] Import GitHub repo
2. [ ] Framework: Static
3. [ ] Deploy
4. [ ] Production domain:
   - Settings → Domains
   - Add custom domain
5. [ ] HTTPS: Automatic

**Verification:**
- [ ] Site accessible at vercel domain
- [ ] All pages load
- [ ] HTTPS works

## SSL/HTTPS

- [ ] HTTPS enabled on custom domain
- [ ] SSL certificate installed
- [ ] All content loads over HTTPS (no mixed content warnings)
- [ ] Redirects from HTTP to HTTPS work
- [ ] Security headers configured (if possible)

**Test:** Check padlock icon in browser address bar

## Email Configuration

### Email Service Setup
- [ ] Service chosen (Gmail, SendGrid, Mailgun, Formspree, etc.)
- [ ] Email account created
- [ ] SMTP configured if needed
- [ ] Email authentication working

### Forms Integration
- [ ] Booking form sends confirmation email
- [ ] Contact form sends to admin email
- [ ] Auto-responder emails working
- [ ] Email templates created
- [ ] Test emails sent and received

### Email Addresses
- [ ] sales@ email working
- [ ] support@ email working
- [ ] partners@ email working
- [ ] product@ email working
- [ ] contact form submissions forwarded

## Analytics Setup

### Google Analytics
- [ ] Analytics account created
- [ ] Property created for domain
- [ ] Tracking code added to all pages
- [ ] Code placed before `</head>` tag
- [ ] Verification shows data coming in
- [ ] Goal tracking set up:
  - [ ] Form submissions
  - [ ] Booking completions
  - [ ] Page views

**Verification:** Check real-time reports in Analytics

### Other Analytics (Optional)
- [ ] Hotjar (heatmaps/recordings)
- [ ] Segment (event tracking)
- [ ] Mixpanel (advanced analytics)

## Performance Optimization

- [ ] Images compressed
- [ ] CSS minified (optional, not needed for small site)
- [ ] Lazy loading enabled if images added
- [ ] Cache headers configured (if server supports)
- [ ] PageSpeed score checked (aim for >80)
- [ ] Core Web Vitals checked

**Check:** https://pagespeed.web.dev/

## SEO Configuration

- [ ] Sitemap created and submitted
- [ ] robots.txt file created (if needed)
- [ ] Meta descriptions on all pages
- [ ] Unique titles on all pages
- [ ] Heading hierarchy correct
- [ ] Open Graph tags added (for social sharing)
- [ ] Twitter Card tags added
- [ ] Google Search Console connected
- [ ] Bing Webmaster Tools connected

**Google Search Console:**
1. [ ] Verify domain ownership
2. [ ] Submit sitemap
3. [ ] Check for errors
4. [ ] Monitor search performance

## Security

- [ ] HTTPS enabled
- [ ] No sensitive data in code
- [ ] Forms validated server-side (if backend)
- [ ] CORS headers configured (if needed)
- [ ] Security headers set:
  - [ ] Content-Security-Policy
  - [ ] X-Frame-Options: DENY
  - [ ] X-Content-Type-Options: nosniff
- [ ] Robots.txt configured
- [ ] Humans.txt created (optional)

## Monitoring & Alerts

- [ ] Uptime monitoring set up (Pingdom, UptimeRobot)
- [ ] Error monitoring set up (Sentry, LogRocket)
- [ ] Email alerts configured for downtime
- [ ] Backup strategy in place
- [ ] Regular backup schedule set

## Social Media

- [ ] Links on website point to social profiles
- [ ] Social media accounts created:
  - [ ] Twitter/X
  - [ ] LinkedIn
  - [ ] GitHub
  - [ ] Slack Community
- [ ] Social profiles filled out with brand info
- [ ] Links to website in bios

## Third-Party Services

### Booking Integration (Choose One)
- [ ] Calendly API integrated, OR
- [ ] Google Calendar API integrated, OR
- [ ] Custom backend built
- [ ] Confirmation emails working
- [ ] Calendar synced

### Payment System (If Charging)
- [ ] Stripe account created
- [ ] Stripe keys configured
- [ ] Payment page created
- [ ] Subscription plans set up
- [ ] Test transaction completed
- [ ] Webhook configured for confirmations

### Email Service (If Not Gmail)
- [ ] SendGrid/Mailgun account created
- [ ] API keys configured
- [ ] SMTP credentials working
- [ ] Test email sent

## Documentation & Support

- [ ] Support email monitored
- [ ] Contact form responses checked
- [ ] FAQ section reviewed
- [ ] Help documentation created
- [ ] Support process documented

## Marketing Preparation

- [ ] Announcement email drafted
- [ ] Social media announcement planned
- [ ] Launch blog post created (optional)
- [ ] Press release created (optional)
- [ ] Beta users invited
- [ ] Early access list prepared

## Launch Day Tasks

- [ ] Final content review
- [ ] All links verified one more time
- [ ] Test forms on live site
- [ ] Check analytics is tracking
- [ ] Announce on social media
- [ ] Send launch email
- [ ] Monitor for errors
- [ ] Respond to initial inquiries

## Post-Launch (First Week)

- [ ] Monitor uptime
- [ ] Check analytics for issues
- [ ] Review error logs
- [ ] Respond to user feedback
- [ ] Fix any reported bugs
- [ ] Iterate on based on early feedback

## Post-Launch (First Month)

- [ ] Analyze traffic patterns
- [ ] Optimize based on analytics
- [ ] Add customer testimonials as they arrive
- [ ] Update case studies
- [ ] Collect and respond to feedback
- [ ] Plan next features/improvements

## Ongoing Maintenance

- [ ] Weekly: Check uptime
- [ ] Weekly: Monitor analytics
- [ ] Monthly: Backup verification
- [ ] Monthly: Security updates
- [ ] Monthly: Analytics review
- [ ] Quarterly: Content refresh
- [ ] Quarterly: Security audit
- [ ] Annually: Compliance review

## Sign-Off

Before launching, confirm:
- [ ] All required items completed
- [ ] Site fully tested
- [ ] Performance acceptable
- [ ] Security verified
- [ ] Analytics tracking
- [ ] Support ready
- [ ] Team informed
- [ ] Stakeholders approved

**Launch authorized by:** _________________ **Date:** _____________

---

## Common Deployment Issues & Solutions

### Issue: Forms not sending
**Solution:** Implement backend or use Formspree/EmailJS

### Issue: HTTPS not working
**Solution:** Ensure DNS properly configured, wait 24 hours, force HTTPS redirect

### Issue: Pages not indexing in Google
**Solution:** Submit sitemap in Google Search Console, verify domain ownership

### Issue: Site not live after deployment
**Solution:** Check DNS propagation, verify branch is set correctly in settings

### Issue: Emails going to spam
**Solution:** Configure SPF, DKIM, DMARC records, use reputable email service

## Need Help?

- **Netlify Docs:** https://docs.netlify.com/
- **Vercel Docs:** https://vercel.com/docs
- **GitHub Pages:** https://pages.github.com/
- **Google Analytics:** https://analytics.google.com/analytics/web/provision/
- **Email Issues:** Check your email service provider docs

---

**You're ready to launch! 🚀**

Start with the "Pre-Deployment" section and work your way down. Good luck!
