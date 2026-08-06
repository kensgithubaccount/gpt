# Sophie + Ken — wedding website

A Vite/React editorial wedding website. Run `npm install && npm run dev`.

## Editing content

Confirmed facts and all editable collections live in `src/content.js`. Entries under `editorNotes` are intentionally unpublished placeholders. Replace only with approved details. `visibility` flags support hiding unfinished modules before launch.

The RSVP screen is deliberately disconnected in this preview: a public client bundle must never contain the guest list. Connect the lookup action to a rate-limited server endpoint backed by encrypted private storage; return only the matching household after server-side normalization. Add CSRF protection, a honeypot or Turnstile, signed update tokens, audit logging, an authenticated admin route and CSV export before launch.

## Launch checklist

- Add confirmed contacts, RSVP deadline, hotels, recommendations, accessibility and photography guidance.
- Connect server-side RSVP lookup/submission and transactional email.
- Set preview access at the hosting layer (Vercel Deployment Protection, Cloudflare Access, or HTTP Basic Auth).
- Replace CSS-drawn editorial illustrations with final approved artwork without changing their supplied accessible descriptions.
- Export `public/social.svg` to PNG if the chosen social platform does not accept SVG previews.

## Confirmation email template

**Subject:** Your response for Sophie + Ken — June 5, 2027

You're in.

We'll see you in New York on June 5. Your response has been recorded. You can return to the RSVP page with the private update link below should your plans change.

`{{ secure_update_url }}`

New York Athletic Club · 180 Central Park South · Arrival at 5:30 PM
