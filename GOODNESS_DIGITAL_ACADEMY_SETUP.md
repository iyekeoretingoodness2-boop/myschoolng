# Goodness Digital Service — project notes

The current `index.html` is a static public landing page. It has no payment system and does not collect student account information.

## Current features
- Mobile-friendly Goodness Digital Service branding
- Six free-to-explore digital-skills topic cards
- Learning outline popups
- WhatsApp contact link

## Not implemented yet
- Hosted video lessons or downloadable course materials
- Secure account registration and login
- Admin dashboard and course management
- Cross-device student progress
- Private messages, group chat, or media uploads

These require a backend and access-control rules. Do not claim these features are live until they are built and tested. Firebase Storage may require a paid billing plan, so avoid relying on it without the owner's approval.

## Security
This frontend contains no passwords, secret keys, or privileged admin operations. Do not add admin credentials or service-account keys to browser code.
