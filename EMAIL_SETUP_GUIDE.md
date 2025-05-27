# Email Setup Guide - Direct Email Sending

This guide will help you set up direct email sending from your landing page without requiring users to open their email client.

## 🚀 Option 1: EmailJS (Recommended - Free & Easy)

### Step 1: Create EmailJS Account
1. Go to [https://www.emailjs.com/](https://www.emailjs.com/)
2. Sign up for a free account
3. Verify your email address

### Step 2: Connect Your Email Service
1. In EmailJS dashboard, go to **Email Services**
2. Click **Add New Service**
3. Choose your email provider:
   - **Gmail** (recommended)
   - **Outlook**
   - **Yahoo**
   - Or any SMTP service
4. Follow the connection wizard
5. Note down your **Service ID**

### Step 3: Create Email Template
1. Go to **Email Templates**
2. Click **Create New Template**
3. Use this template content:

```
Subject: Demo Request from {{company_name}}

New Demo Request Received:

Company Name: {{company_name}}
Company Website: {{company_website}}
Email Address: {{email}}
Phone Number: {{phone}}

Please contact this prospect within 24 hours to schedule their AI demo.

Best regards,
AI Evolution Group Website
```

4. Save and note down your **Template ID**

### Step 4: Get Your Public Key
1. Go to **Account** → **General**
2. Copy your **Public Key**

### Step 5: Update Your Website
Replace these values in your `index.html`:

```javascript
// Replace YOUR_PUBLIC_KEY with your actual public key
emailjs.init("YOUR_PUBLIC_KEY");

// Replace YOUR_SERVICE_ID and YOUR_TEMPLATE_ID
emailjs.send('YOUR_SERVICE_ID', 'YOUR_TEMPLATE_ID', data)
```

### Example:
```javascript
emailjs.init("user_abc123def456");
emailjs.send('service_gmail', 'template_demo_request', data)
```

---

## 🔧 Option 2: Formspree (Alternative)

### Step 1: Create Formspree Account
1. Go to [https://formspree.io/](https://formspree.io/)
2. Sign up for free account
3. Create a new form

### Step 2: Update JavaScript
Replace the EmailJS code with:

```javascript
function submitDemoForm(event) {
    event.preventDefault();
    
    const form = document.getElementById('demoForm');
    const formData = new FormData(form);
    
    fetch('https://formspree.io/f/YOUR_FORM_ID', {
        method: 'POST',
        body: formData,
        headers: {
            'Accept': 'application/json'
        }
    }).then(response => {
        if (response.ok) {
            // Show success
            form.style.display = 'none';
            document.getElementById('successState').style.display = 'block';
        }
    });
}
```

---

## 🛠️ Option 3: Netlify Forms (If hosting on Netlify)

### Step 1: Add to Form Tag
```html
<form id="demoForm" netlify onsubmit="submitDemoForm(event)">
```

### Step 2: Simple JavaScript
```javascript
function submitDemoForm(event) {
    // Let Netlify handle the form submission
    // Just show success message after delay
    setTimeout(() => {
        document.getElementById('demoForm').style.display = 'none';
        document.getElementById('successState').style.display = 'block';
    }, 1000);
}
```

---

## 📧 Email Template Variables

Your email template can use these variables:
- `{{company_name}}` - Company name from form
- `{{company_website}}` - Company website URL
- `{{email}}` - Contact email address
- `{{phone}}` - Phone number
- `{{to_email}}` - Your receiving email (aievolutiongroup@gmail.com)

---

## 🔒 Security Notes

1. **EmailJS Public Key**: Safe to expose in frontend code
2. **Rate Limiting**: EmailJS has built-in spam protection
3. **Email Validation**: Form includes client-side validation
4. **Fallback**: If EmailJS fails, falls back to mailto

---

## 🎯 Recommended: EmailJS Setup

**Why EmailJS?**
- ✅ Free tier (200 emails/month)
- ✅ No backend server needed
- ✅ Works with any email provider
- ✅ Built-in spam protection
- ✅ Easy setup and maintenance

**Quick Setup Checklist:**
- [ ] Create EmailJS account
- [ ] Connect Gmail/email service
- [ ] Create email template
- [ ] Copy Public Key, Service ID, Template ID
- [ ] Update website code
- [ ] Test the form

Once set up, emails will be sent directly from your Gmail to aievolutiongroup@gmail.com without requiring users to open their email client! 