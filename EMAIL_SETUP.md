# 📧 Email Setup Guide - K8s Agent Booking

## Enable Email Notifications for Demo Bookings

Your website is configured to send booking notifications to **yousefaboelfoul@gmail.com**. Follow these steps to activate email functionality.

## Quick Setup (5 minutes)

### Step 1: Create EmailJS Account
1. Go to https://www.emailjs.com/
2. Click "Sign Up Free"
3. Create account (free tier includes 200 emails/month)
4. Verify your email

### Step 2: Get Your Public Key
1. Log in to EmailJS dashboard
2. Go to "Account" section
3. Copy your **Public Key**
4. Keep it safe - you'll need it shortly

### Step 3: Create Email Service
1. In EmailJS dashboard, click "Email Services"
2. Click "Add Service"
3. Choose your email provider:
   - **Gmail**: Select "Gmail"
   - **Other Email**: Select appropriate service
4. Click "Connect Account"
5. Follow Gmail authentication
6. Copy your **Service ID**

### Step 4: Create Email Template
1. Go to "Email Templates"
2. Click "Create New Template"
3. Name it: `demo_booking_notification`
4. Set "To Email": `{{to_email}}`
5. Set "From Name": `{{from_name}}`
6. Create subject: `New Demo Booking - {{from_name}}`
7. Create body template:

```
Hi Team,

New demo booking received:

Name: {{from_name}}
Email: {{from_email}}
Phone: {{phone}}
Company: {{company}}
Role: {{role}}
Clusters Managed: {{clusters}}
Demo Date: {{selected_date}}
Demo Time: {{selected_time}}
Interest Details: {{interests}}

Message: {{message}}

To respond, reply to: {{from_email}}

---
K8s Agent Booking System
```

8. Copy your **Template ID**

### Step 5: Update Website Code

Edit `pages/booking.html` and find this section (near the top):

```javascript
emailjs.init("YOUR_EMAILJS_PUBLIC_KEY");
```

Replace with your actual public key:
```javascript
emailjs.init("abc123def456..."); // Your actual key
```

Then find this line further down:
```javascript
emailjs.send("YOUR_SERVICE_ID", "YOUR_TEMPLATE_ID", templateParams)
```

Replace with your actual IDs:
```javascript
emailjs.send("service_abc123", "template_xyz789", templateParams)
```

### Step 6: Test the Booking
1. Go to your website booking page
2. Fill out a test booking
3. Submit the form
4. Check your email inbox at yousefaboelfoul@gmail.com
5. You should receive the booking notification

## What Gets Sent in the Email

When someone books a demo, you'll receive an email with:
- Customer name and email
- Phone number
- Company name
- Job title
- Number of Kubernetes clusters
- Requested demo date and time
- Their specific interests/needs

## Security Notes

- Your Public Key is safe to expose (it's meant to be public)
- Never share your Private Key
- EmailJS handles all security
- Emails are sent securely via SMTP

## Troubleshooting

### Email not arriving?
1. Check spam/junk folder
2. Verify Gmail is authenticated in EmailJS
3. Check EmailJS console for errors
4. Verify template is published

### Template not working?
1. Make sure all {{placeholders}} match the code
2. Check template is in "Publish" mode
3. Try sending test email from EmailJS dashboard

### Console shows errors?
1. Check your Public Key is correct
2. Check Service ID is correct
3. Check Template ID is correct
4. Verify all IDs are enclosed in quotes

## Alternative: Use Formspree (Even Easier)

If you prefer a simpler setup:

1. Go to https://formspree.io/
2. Sign up free
3. Create new form
4. Get your form endpoint: `https://formspree.io/f/YOUR_ID`
5. Update the form action in booking.html
6. That's it!

## Free Email Tier Limits

**EmailJS Free Plan:**
- 200 emails/month
- Unlimited contacts
- Perfect for early stage

**Upgrade when needed:**
- $2.50/month for 1000 emails
- $10/month for 10,000 emails

## Testing Without Setup

The booking form currently:
✓ Records all bookings locally (console)
✓ Shows success message to user
✓ Resets form after submission
✓ Ready for email when configured

Email is optional but recommended for:
- Receiving booking notifications
- Responding to customers promptly
- Tracking demo interest

## Questions?

- EmailJS Help: https://www.emailjs.com/docs/
- Email Service Setup: https://www.emailjs.com/docs/tutorial/creating-email-service/
- Template Help: https://www.emailjs.com/docs/tutorial/creating-email-template/

---

**Estimated Time to Enable:** 5-10 minutes  
**Cost:** Free (200/month included)  
**Result:** Automatic booking notifications to your inbox
