# Goodness Digital Academy — Firebase setup

This repository is still based on the existing MySchoolNG Firebase project. These files are **prepared rules**, not published rules. Review and test them before deploying; do not paste them into production until the existing MySchoolNG app has been tested against them.

## Project
- Firebase project ID: `myschoolng-4f9d7`
- Existing web app ID: `1:678124473888:web:d78e294dd8cb51cb0c7645`

## Files
- `firestore.rules`: access policy for existing school collections and academy collections.
- `storage.rules`: access policy for course media and private submissions.

## Before production
1. Use Firebase Console → Authentication → Users to preserve existing accounts.
2. In Authentication → Settings → Authorized domains, add the deployed website domain.
3. Enable Cloud Storage and review billing/plan requirements.
4. Test rules in Rules Playground or a staging project first. Existing MySchoolNG user updates may need app adjustments because only safe profile fields are writable.
5. Set the `admin: true` custom claim for the academy owner from a trusted server/Admin SDK. Never let a browser set its own admin claim.
6. Build a trusted admin-only approval process. The browser must never write `academyMembers.status = approved` or change a payment request's status.
7. Store only payment reference/status in Firestore; verify transfers against the PalmPay account manually before an admin approves a request. A receipt alone is not proof of payment.
8. Store lesson files in Storage under `courses/`; do not expose private course files through public static hosting.
9. Configure Firebase web app SDK using the existing project's public web configuration. Do not commit service-account keys or other private credentials.

## Important limitations
These rules do not themselves create a functioning UI, upload workflow, administrator dashboard, or payment verification integration. They are the security layer to deploy after app behavior is implemented and tested. The conversation's WhatsApp flow remains manual verification, not automatic bank verification.
