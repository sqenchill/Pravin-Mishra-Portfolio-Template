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
## Footer Requirement
The portfolio footer displays version, deploy date, and author:

**Pravin Mishra Portfolio v1.0 — Deployed on <DD Mon YYYY> — By Sonny Enchill**

## How the Deploy Date is Generated
The deploy date is generated automatically on page load using JavaScript and inserted into the footer element with `id="deployDate"` in **DD Mon YYYY** format.

### Footer Snippet
```html
<!-- Bottom -->
      <div class="footer-bottom" style="text-align:center; padding:20px 10px;">
        <p>© <span id="year"></span> Pravin Mishra. All rights reserved.</p>
        <p>Crafted with <span>cloud</span> excellence by Pravin Mishra</p>
        <p>Pravin Mishra Portfolio v1.0 — Deployed on <span id="deployDate"></span> — By Sonny Enchill</p>
      </div>

    </div>
  </footer>


  <script>
    (function () {
      const el = document.getElementById("deployDate");
      if (!el) return;

      const now = new Date();
      const months = ["Jan","Feb","Mar","Apr","May","Jun","Jul","Aug","Sep","Oct","Nov","Dec"];
      const dd = String(now.getDate()).padStart(2, "0");
      const mon = months[now.getMonth()];
      const yyyy = now.getFullYear();

      el.textContent = `${dd} ${mon} ${yyyy}`;
    })();
  </script>

✅ This proof must be visible in your browser screenshot submission.
