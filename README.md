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

✅ This proof must be visible in your browser screenshot submission.

---

## Footer Version & Deploy Date (Week 5 Assignment)

The homepage, privacy, and terms pages display a footer with the site version, deploy date, and author name:

Pravin Mishra Portfolio v1.0 — Deployed on 03 Aug 2026 — By Ekweozor Victoria Nkemakonam

Approach used: Deployment-time update.

The deploy date is not generated automatically by code. Instead, the date is updated manually in the footer text each time a new deployment is made, using a simple find-and-replace command before deploying:

sed -i 's/Deployed on OLD_DATE/Deployed on NEW_DATE/' index.html privacy.html terms.html

This keeps the implementation simple and avoids adding JavaScript dependencies for a static site, while still ensuring the footer accurately reflects the date of each deployment.
