# TNT Dental — New Client Site Checklist

Use this checklist every time a new dental client site is sold.
Estimated setup time: 1–2 hours.

---

## Step 1 — Create the Repo (5 mins)

- [ ] Go to the `tnt-dental-template` repo on GitHub
- [ ] Click **"Use this template"** → **"Create a new repository"**
- [ ] Name the repo after the client e.g. `brightsmiles-dental`
- [ ] Set visibility to **Private**
- [ ] Click **"Create repository"**

---

## Step 2 — Update Site Content (30–45 mins)

Open `src/content/site.json` and update every field:

- [ ] `practiceName` — exact name of the practice
- [ ] `tagline` — their hero headline (keep under 8 words)
- [ ] `subtext` — supporting line under the headline
- [ ] `phone` — main contact number
- [ ] `email` — main contact email
- [ ] `address` — full street address
- [ ] `hours` — office hours
- [ ] `acceptingPatients` — set to `true` or `false`
- [ ] `googleRating` — pull from their Google Business profile
- [ ] `reviewCount` — total number of Google reviews
- [ ] `patientCount` — ask the client
- [ ] `yearsInPractice` — ask the client

---

## Step 3 — Update Services (15 mins)

Open `src/content/services.json`:

- [ ] Remove any services the practice does not offer
- [ ] Add any services not in the default list
- [ ] Make sure descriptions match the client's tone and offerings

---

## Step 4 — Update Team (15 mins)

Open `src/content/team.json`:

- [ ] Replace placeholder names, roles, and bios with real staff
- [ ] Add or remove team members as needed
- [ ] Add photo filenames once images are provided (e.g. `dr-chen.jpg`)
- [ ] Place photo files in `public/images/team/`

---

## Step 5 — Brand Colors (5 mins)

Open `src/styles/global.css` and update the `:root` variables:

- [ ] `--color-teal` — client's primary brand color
- [ ] `--color-navy` — client's dark/background color
- [ ] `--color-gold` — client's accent color (optional)

---

## Step 6 — Connect to CloudCannon (10 mins)

- [ ] Log in to CloudCannon
- [ ] Click **"Add Site"** → **"Connect a GitHub repo"**
- [ ] Select the client repo
- [ ] Set build command to `npm run build`
- [ ] Set output directory to `dist`
- [ ] Click **"Build Site"**
- [ ] Confirm the site builds without errors

---

## Step 7 — Set Up Client Domain (10 mins)

- [ ] Add the client's custom domain in CloudCannon site settings
- [ ] Update DNS records with the client's domain registrar
- [ ] Confirm SSL certificate is issued
- [ ] Test the live URL

---

## Step 8 — Client Handoff

- [ ] Share CloudCannon login credentials with the client
- [ ] Walk the client through editing content in CloudCannon
- [ ] Send the client the CloudCannon editing guide
- [ ] Confirm contact form is routing to the correct email

---

## Notes

Use this space for any client-specific notes, special requests, or deviations from the standard template.