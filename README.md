# Medico Clinic Website

A multi-page clinic website built with HTML, CSS, JavaScript, and Bootstrap. It provides a front-end starting point for presenting a clinic, its services, departments, and doctors.

## Pages and assets

- `index.html`: home page and appointment-style form.
- `about.html`: clinic introduction.
- `services.html` and `dep.html`: services and departments.
- `doctor.html`: doctor/team page.
- `contact.html`: contact information and contact form.
- `css/`, `js/`, `img/`, and `sass/`: styling, scripts, images, and Sass sources.
- `contact_process.php`: PHP email handler.
- `182 Medico -DOC/`: bundled template documentation.

## Preview locally

```bash
git clone https://github.com/CaptainVish/Medico-clinic-website.git
cd Medico-clinic-website
python3 -m http.server 8000 --bind 127.0.0.1
```

Open `http://localhost:8000/`. This serves the static pages; it does **not** execute PHP or send email. No Node/npm build is required to view the committed HTML and CSS.

To test PHP locally after reviewing the form handler, use a configured PHP environment instead:

```bash
php -S 127.0.0.1:8000
```

PHP's `mail()` also needs a working mail configuration. Do not submit forms until their destinations have been reviewed and replaced with your own test endpoints.

## Customize

1. Replace sample clinic details, doctors, images, and page text.
2. Update navigation links and contact information consistently across pages.
3. Edit the committed CSS or compile your changes from the Sass sources with your chosen Sass workflow.
4. Review mobile layouts, accessibility, and all form behavior before publishing.

## Forms and known limitations

The contact handler contains a template recipient, unrelated template message text, and an undefined `$csubject` variable. Configure and correct it before enabling email. The newsletter forms also reference an external template subscription destination; replace or remove that wiring before accepting submissions.

The appointment section is a front-end form, not evidence of a working booking system. There is no documented appointment database or scheduling backend in this repository. Add and test those integrations separately if needed.

Do not collect patient or medical information with this demo as-is. Form security, validation, privacy handling, and email delivery were not audited or tested during the README update.

## Template credits

The HTML identifies a Colorlib template and includes attribution/license comments. Preserve the original template and third-party asset notices, and review the bundled documentation before redistributing or changing attribution. This repository's customizations do not replace the original asset terms.
