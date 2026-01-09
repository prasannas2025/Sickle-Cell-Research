# Sickle Cell Patient Registration Portal

A simple, responsive website for registering patients with Sickle Cell Disease (SCD) or Sickle Cell Trait (SCT). Designed for GitHub Pages hosting, using HTML, CSS, and JavaScript. The form can submit to a serverless form handler such as [Formspree](https://formspree.io) or [Netlify Forms](https://docs.netlify.com/forms/).

## Included files
- `index.html` — Main site and registration form
- `assets/css/styles.css` — Custom styles (color theme: blue / white / grey)
- `assets/js/main.js` — Client-side validation and submission handler

## Features
- Registration form fields:
  - Patient Name (required)
  - Age (required)
  - Gender (Male / Female / Other) (required)
  - Disease or Trait (Sickle Cell Disease / Sickle Cell Trait) (required)
  - Location (City, District, State) (required)
  - Contact Number (required)
  - Email Address (optional)
  - Additional Notes (optional)
  - Submit button text: "Submit Registration"
- Confirmation message on success: "Thank you for registering! Your information has been securely recorded."
- Responsive layout (Bootstrap)
- Accessible form labels and ARIA attributes

## Setup

1. Host the site on GitHub Pages
   - Option A — Repository root (recommended for user/organization pages): Push files to the `main` branch and enable GitHub Pages in repository settings (choose root).
   - Option B — `gh-pages` branch: Push built files to `gh-pages` and enable Pages.

2. Configure form submission
   - Form handler: The site uses client-side fetch to send form data. By default the request uses the constant `FORM_ENDPOINT` in `assets/js/main.js`.
   - Formspree:
     1. Create a free form endpoint at [Formspree](https://formspree.io).
     2. Replace the `FORM_ENDPOINT` placeholder with your Formspree endpoint (e.g. `https://formspree.io/f/xyzabc`).
   - Netlify Forms (alternative):
     - If using Netlify, you can add the `data-netlify="true"` attribute to the `<form>` element and deploy to Netlify. Modify or remove the JS submit handler as desired.

3. Customize
   - Update the `Resources` and `Contact` sections inside `index.html`.
   - Replace hero image or icons as needed.

## Security & Privacy
- This site collects personally identifying information. If using a third-party form service, ensure compliance with local privacy laws and obtain consent where required.
- For production use, consider using an authenticated backend and secure storage for patient data.

## Notes
- The UI uses [Bootstrap 5](https://getbootstrap.com/), [Bootstrap Icons](https://icons.getbootstrap.com/), and Google Fonts.
- Replace the `FORM_ENDPOINT` constant in `assets/js/main.js` before going live.

If you want, I can:
- Add serverless backend examples (AWS Lambda / Netlify Functions) for secure storage.
- Integrate an email notification on registration.
- Add localization or accessibility audit fixes.
# Sickle-Cell-Research
