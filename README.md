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

## Footer Dynamic Date Implementation

### Footer Requirement

The footer must display the current year and deploy date automatically without manual updates.

---

### How the date is generated

* A <span> is placed in the footer to hold the date.
* When the page loads, JavaScript runs automatically.
* JavaScript gets today’s date from the browser.
* The date is turned into a readable format (DD Mon YYYY).
* The final date is shown in the footer.
---

### Implementation (Code Snippet)

#### Footer HTML

```html
<div class="footer-bottom">
  <p>© <span id="year"></span> Pravin Mishra. All rights reserved.</p>
  <p>Crafted with <span>cloud</span> excellence by Pravin Mishra</p>
  <p>Pravin Mishra Portfolio v1.0 — <span id="deployDate"></span> — By Ntando Mvubu</p>
</div>
```

#### JavaScript

```html
<script>
  const today = new Date();

  const day = String(today.getDate()).padStart(2, "0");
  const month = today.toLocaleString("en-US", { month: "short" });
  const year = today.getFullYear();

  document.getElementById("deployDate").textContent =
    `${day} ${month} ${year}`;
</script>
```

---

### Result

Each time the page loads, the footer automatically displays the current date in a readable format, removing the need for manual updates.

---
