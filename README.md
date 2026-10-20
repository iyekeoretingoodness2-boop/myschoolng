# MySchoolNG

A mobile-friendly school portal prototype for students and teachers.

## Current prototype features
- Responsive landing page
- Student and teacher registration/login preview
- Role-specific dashboard views
- Local-browser demo storage for assignments, lesson notes, and subjects
- Class-based filtering for demo content

## Important limitations
This first version is a **frontend prototype**, not a production school system. Authentication and data are stored in the current browser using localStorage. This is not secure authentication, and data does not sync between devices or users. Do not use real passwords or sensitive student information.

## Next steps for production
1. Connect Firebase Authentication.
2. Set up Cloud Firestore collections for users, classes, subjects, assignments, and lesson notes.
3. Add Firestore security rules so users can access only the data allowed by their role and class.
4. Test registration, login, access control, and mobile layouts.
5. Publish through GitHub Pages (frontend only); Firebase supplies the shared backend.

## Development
The current preview is a static HTML page, so no build step is required. Open `index.html` in a browser or host it as a static site.
