# Stallion Connect Pvt Ltd — Website (single-page edition)

Company website for **Stallion Connect Pvt Ltd**: call centre, BPO, sales, customer support, recruitment and back-office services.

The whole site is one self-contained file, `index.html`: all CSS and JavaScript are inline and there is no build step. Sections: Home, About, Services, Industries, Careers and Contact, linked from the navigation bar.

- **Scrolling** is the browser's own. Lenis smooth scrolling was removed because it made the page lag.
- **Background videos** load from CloudFront, each only as it nears the screen, and pause off-screen. Their stills are compressed WebP files in `assets/img/` (`still-*.webp`). **Photos** are free Unsplash images linked from `images.unsplash.com`; swap them for the company's own photos when available.
- **The logo** is embedded in the page as a data URI. The original logo files remain in `assets/img/`.

## Run locally

Open `index.html` in a browser, or serve the folder:

```bash
python -m http.server 5500
```

## Before launch

- **Forms** run in demo mode and send nothing. Set `FORM_ENDPOINT` near the top of the script in `index.html` (for example a Formspree form URL) to receive enquiries and job applications by email.
- **Placeholders** are marked `TODO` in the HTML: office address, phone number, social media links, the "24×7" figure, careers perks and job openings.
