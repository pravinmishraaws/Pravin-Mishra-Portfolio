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


Perfect — this is a **documentation task**, not coding gymnastics.
I’ll give you a **clean, professional README section** you can paste almost verbatim, plus a **tiny JS snippet** that matches the assignment *exactly*.

You can use **Option A (JS)** — it looks more “engineering-minded” and is still beginner-friendly.

---

## 📌 Footer Version & Deploy Date

This project includes a visible footer on the homepage to provide basic deployment provenance.

### Footer Requirement

The footer displays:

* Application name and version
* Deployment date
* Author

Example footer text:

```
Pravin Mishra Portfolio v1.0 — Deployed on 02 Feb 2026 — By <Your Name>
```

---

## 🛠 How the Deploy Date Is Generated

The deploy date is generated **dynamically at runtime** using a small JavaScript snippet.
When the page loads, JavaScript calculates the current date and injects it into the footer in `DD Mon YYYY` format.

This ensures the footer always reflects the date of the latest deployment without hard-coding the value.

---

## 💻 Code Snippet

### Footer HTML

```html
<footer>
  <p>
    Pravin Mishra Portfolio v1.0 — Deployed on
    <span id="deployDate"></span> — By <Your Name>
  </p>
</footer>
```

### JavaScript (Dynamic Date)

```html
<script>
  const deployDate = new Date();
  const options = { day: '2-digit', month: 'short', year: 'numeric' };
  document.getElementById('deployDate').textContent =
    deployDate.toLocaleDateString('en-GB', options);
</script>
```

---

## ✅ Verification

* The footer is visible on the live EC2 deployment.
* The deploy date updates automatically on each deployment.
* Changes are tracked through Git commits and Jira sprint tasks.




















