# DMI Portfolio Website (Static HTML/CSS)

This repository contains a clean, professional-looking **static portfolio website** used in **DevOps Micro Internship (DMI)** Week 1 to practice:
- Linux basics
- Nginx hosting
- Deployment proof / ownership
- Production-style checks

✅ Students deploy this website on an Ubuntu VM using Nginx and keep it live for 24 hours.

---

## Who is this for?
- DMI students (beginner → intermediate)
- Anyone learning how to host a static site with Nginx on Linux

---

## What you will build
A portfolio-style website hosted on:
- **Ubuntu VM**
- **Nginx**
- Accessible via: `http://<public-ip>`

---

## Mandatory Ownership Proof (DMI Rule)
Before you deploy, you MUST edit the footer and add your details:

Original:

```html
<p>Crafted with <span>cloud</span> excellence by Pravin Mishra</p>
```

Add this line (example):

```html
<p><strong>Deployed by:</strong> DMI Cohort 2 | Rahul Sharma | Group 4 | Week 1 | 16-01-2026</p>
```

## Make Deploy Date Dynamic 
Add a <span id="deployDate"></span> in footer where date goes

Add JS that sets today’s date in DD Mon YYYY format

## Footer Requirement
The date is shown to provide visibility into when the site was last deployed and helps demonstrate basic production awareness and transparency.

## How the Date Is Generated
The deployment date is generated dynamically using JavaScript at runtime. When the page loads, the script retrieves the current date and formats it using the en-GB locale with a fixed UTC timezone to ensure consistent display across different user locations.

This approach is suitable for learning projects and demonstrations, where a lightweight and simple solution is preferred. The date will update whenever the application is redeployed or the page is refreshed.

## HTML (Footer)
<footer>
  <span>Deployed on: </span>
  <span id="deployDate"></span>
</footer>

## JavaScript (Date Formatting Logic)
<script>
  const deployDate = new Date();

  const formattedDate = deployDate.toLocaleDateString('en-GB', {
    day: '2-digit',
    month: 'short',
    year: 'numeric',
    timeZone: 'UTC'
  });

  document.getElementById('deployDate').textContent = formattedDate;
</script>


✅ This proof must be visible in your browser screenshot submission.