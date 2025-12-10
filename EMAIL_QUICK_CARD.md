# ⚡ Email Setup Quick Card

## What Changed
✅ Homepage is now emoji-free and more professional  
✅ Booking form is ready to send emails to yousefaboelfoul@gmail.com  
✅ Contact form is ready to send emails to yousefaboelfoul@gmail.com  

---

## To Enable Email (5 minutes)

### 1. Go to EmailJS
https://www.emailjs.com/ → Sign Up Free

### 2. Get Public Key
Account → Copy Public Key

### 3. Create Email Service
Email Services → Add Service → Gmail → Connect Account

### 4. Create Template
Email Templates → Create New → Name: `demo_booking_notification`

### 5. Add to Code

**File: `pages/booking.html`** (Find and replace)

Line ~9:
```javascript
emailjs.init("YOUR_EMAILJS_PUBLIC_KEY");
```
→ Replace `YOUR_EMAILJS_PUBLIC_KEY` with your actual key

Line ~265:
```javascript
emailjs.send("YOUR_SERVICE_ID", "YOUR_TEMPLATE_ID", templateParams)
```
→ Replace with your Service ID and Template ID

**File: `pages/contact.html`** (Same changes)

### 6. Test
- Fill out booking/contact form
- Submit
- Check your email inbox

---

## Email Details

**Send To:** yousefaboelfoul@gmail.com  
**For:** Demo bookings + Contact forms  
**Cost:** Free (200/month)  
**Time:** 5 minutes  

---

## What You'll Receive

### Demo Booking Email:
- Customer name, email, phone
- Company, job title
- Clusters managed
- Requested date/time
- Their interests

### Contact Email:
- Name, email, phone
- Company
- Subject
- Full message
- Subscribe preference

---

## Without Email Setup

✓ Forms still work  
✓ Data saved locally (console)  
✓ Success message shows  
✓ Form resets  
✗ No email notification  

---

## With Email Setup

✓ Forms still work  
✓ Data saved locally (console)  
✓ Success message shows  
✓ **EMAIL SENT TO YOUR INBOX**  
✓ Easy customer follow-up  

---

## Troubleshooting

**Email not arriving?**
- Check spam/junk folder
- Verify Gmail is authenticated
- Check console for errors

**Can't find Public Key?**
- Log in to EmailJS
- Go to Account section
- It's listed there

**Want something simpler?**
- Use Formspree instead (formspree.io)
- No code changes needed
- Just update form action

---

## Files to Read

1. **EMAIL_SETUP.md** - Full detailed guide
2. **CHANGES_MADE.md** - What was updated
3. **This card** - Quick reference

---

## Status

| Feature | Status |
|---------|--------|
| Homepage | ✅ Professional (no emojis) |
| Booking Form | ⚠️ Ready (needs email key) |
| Contact Form | ⚠️ Ready (needs email key) |
| Email Service | ⏳ Free tier available |

---

## Your Inbox

```
yousefaboelfoul@gmail.com
├── Demo Bookings
├── Contact Forms
└── Customer Inquiries
```

All organized and ready for follow-up!

---

**Ready?** Start with EMAIL_SETUP.md
