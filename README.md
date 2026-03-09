# TNT Dental — Site Template

A plug-and-play landing page template for dental practice websites.
Built with Astro, Tailwind CSS v4, and CloudCannon CMS.

---

## How It Works

All client-specific content lives in JSON files under `src/content/`.
Components read from those files automatically — no code changes needed
for a new client site. Brand colors are controlled by CSS variables in
`src/styles/global.css`.
```
src/content/
├── site.json       ← practice info, phone, address, hero text, colors
├── services.json   ← list of services offered
└── team.json       ← team member names, roles, bios, photos
```

---

## Setting Up a New Client Site

### 1. Clone the template

Go to the `tnt-dental-template` repo on GitHub and click:
**"Use this template"** → **"Create a new repository"**

Name it after the client e.g. `brightsmiles-dental` and set it to Private.

### 2. Install dependencies
```bash
npm install
```

### 3. Fill in client content

Edit the three content files:

**`src/content/site.json`**
```json
{
  "practiceName": "Client Practice Name",
  "tagline": "Their Hero Headline Here",
  "subtext": "Supporting line under the headline.",
  "phone": "(555) 000-0000",
  "email": "hello@theirpractice.com",
  "address": "123 Main St, City, ST 00000",
  "hours": "Mon-Fri 8am-6pm, Sat 9am-2pm",
  "acceptingPatients": true,
  "googleRating": "4.9",
  "reviewCount": "200+",
  "patientCount": "2,000+",
  "yearsInPractice": "10+"
}
```

**`src/content/services.json`**
```json
[
  {
    "title": "Service Name",
    "description": "Short description of the service."
  }
]
```

**`src/content/team.json`**
```json
[
  {
    "name": "Dr. Full Name",
    "role": "Job Title",
    "bio": "Short bio."
  }
]
```

### 4. Update brand colors

Open `src/styles/global.css` and update the `:root` variables:
```css
:root {
  --color-teal:  #00BFA6;  /* primary brand color */
  --color-navy:  #0B1F3A;  /* dark/background color */
  --color-gold:  #F5A623;  /* accent color */
}
```

### 5. Add team photos

Place photo files in `public/images/team/` and update the `photo`
field in `team.json` with the filename e.g. `dr-chen.jpg`.

### 6. Run locally
```bash
npm run dev
```

### 7. Deploy via CloudCannon

- Connect this repo to a new CloudCannon project
- Set build command: `npm run build`
- Set output directory: `dist`
- Add the client's custom domain in CloudCannon site settings

For the full step-by-step launch process see `CLIENT-SETUP.md`.

---

## Project Structure
```
src/
├── components/
│   ├── sections/       ← full page sections (Hero, Services, Team...)
│   └── ui/             ← small reusable pieces (Button, Badge)
├── content/            ← all client data lives here
│   ├── site.json
│   ├── services.json
│   └── team.json
├── layouts/
│   └── Layout.astro    ← base HTML wrapper
├── pages/
│   └── index.astro     ← wires all components together
└── styles/
    └── global.css      ← design tokens and base styles
```

---

## Making Global Updates

When a component needs to change across all client sites:

1. Update the component in this template repo
2. For existing client sites — manually pull the updated component
   into each repo, or copy it across

> Once the component library is extracted into a separate npm package
> (`@tnt-dental/ui`), updates will propagate to all sites automatically
> via a version bump.

---

## Built With

- [Astro](https://astro.build) v5
- [Tailwind CSS](https://tailwindcss.com) v4
- [CloudCannon](https://cloudcannon.com)
- [DM Sans](https://fonts.google.com/specimen/DM+Sans) + [Playfair Display](https://fonts.google.com/specimen/Playfair+Display)