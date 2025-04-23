Roadmap Phases

Phase 1: Project Setup and Design (Weeks 1–3, May 1–May 21, 2025)

Objective

Establish the project foundation, including technical setup, UI/UX design, and Firebase configuration, using Create React App and Sass.

Milestones





Project environment setup with Create React App.



UI/UX mockups completed with Sass-based style guide.



Firebase project initialized.

Tasks





Project Initialization (Week 1, 3 days):





Set up Git repository (GitHub).



Initialize React project with Create React App: npx create-react-app wedding-invitations.



Install dependencies: React Router, Sass (node-sass or sass), Firebase SDK.



Configure CSS Modules in CRA (default support with .module.scss files).



Assign team roles and set up communication tools (e.g., Slack, Trello).



Assigned: Project Manager, Frontend Developer.



Dependencies: None.



Firebase Setup (Week 1, 2 days):





Create Firebase project.



Enable Authentication (email/password, Google), Firestore, Storage, Functions, Hosting.



Configure Firebase SDK in React app (src/firebase.js).



Set up initial Firestore Security Rules and Storage Rules.



Assigned: Backend Developer.



Dependencies: None.



UI/UX Design (Weeks 1–2, 10 days):





Design responsive layouts in Figma for:





Homepage (template showcase).



Template details page.



Customization editor.



Cart and checkout.



User dashboard (saved designs, orders).



Admin dashboard (template/order management).



Create style guide using Sass (define variables for colors, typography, spacing in src/styles/_variables.scss).



Develop reusable CSS Modules (e.g., Button.module.scss, Card.module.scss).



Validate designs with stakeholders.



Assigned: UI/UX Designer, Frontend Developer (for Sass setup).



Dependencies: None.



Initial Deployment (Week 3, 2 days):





Deploy empty React app to Firebase Hosting using Firebase CLI.



Verify Firebase Authentication and Firestore connectivity.



Set up CI/CD with GitHub Actions for automated builds.



Assigned: Frontend Developer, Backend Developer.



Dependencies: Tasks 1, 2.

Deliverables





Git repository with CRA project structure.



Configured Firebase project (Authentication, Firestore, Storage, Functions, Hosting).



Figma mockups and Sass-based style guide (variables, reusable CSS Modules).



Initial deployment to Firebase Hosting.

Risks





Risk: CRA setup slower than Vite, impacting initial development speed.





Mitigation: Use CRA’s default optimizations; allocate extra day for setup.



Risk: Sass/CSS Modules increase styling complexity.





Mitigation: Define clear Sass structure; reuse styles with mixins and variables.



Phase 2: Core Features Development (Weeks 4–9, May 22–July 2, 2025)

Objective

Implement core user features: authentication, template browsing, customization editor, and checkout, using CSS Modules for styling.

Milestones





User authentication implemented.



Template browsing and filtering functional.



Customization editor operational.



Cart and payment integration completed.

Tasks





User Authentication (Week 4, 4 days):





Implement login/signup with Firebase Authentication (email/password, Google).



Create user profile page (React component) with CSS Modules (Profile.module.scss) for styling.



Secure routes with React Router (e.g., /dashboard requires login).



Write unit tests for authentication flows using Jest.



Assigned: Frontend Developer, Backend Developer.



Dependencies: Phase 1 (Firebase setup).



Template Browsing (Weeks 5–6, 8 days):





Create TemplateCard component with styling in TemplateCard.module.scss.



Fetch templates from Firestore (templates collection).



Implement search (by name) and filter (by category, price) using Firestore queries.



Build template details page with preview and "Customize" button, styled with TemplateDetails.module.scss.



Optimize image loading with lazy loading (use loading="lazy" for <img> tags).



Assigned: Frontend Developer, Backend Developer.



Dependencies: Phase 1 (Firestore setup).



Customization Editor (Weeks 6–8, 10 days):





Use react-konva for canvas-based editor, styled with Editor.module.scss.



Allow editing of text (content, font), colors, and user-uploaded images.



Save customizations to Firestore (customizations collection) and images to Storage.



Implement real-time preview of changes in the canvas.



Write tests for editor functionality using Jest.



Assigned: Frontend Developer.



Dependencies: Task 2 (template data).



Cart and Checkout (Weeks 8–9, 8 days):





Build Cart component with styling in Cart.module.scss.



Integrate Stripe or Razorpay for payments (use SDKs for React).



Create order in Firestore (orders collection) after payment.



Send confirmation email via SendGrid or Firebase Functions.



Test payment flows in sandbox mode.



Assigned: Frontend Developer, Backend Developer.



Dependencies: Task 3 (customizations).

Deliverables





Authentication system with login/signup and styled profile page.



Template browsing with search and filter functionality, styled with CSS Modules.



Customization editor with save and preview features.



Cart and checkout with payment integration, styled with Sass.



Unit tests for core components.

Risks





Risk: CSS Modules lead to verbose styling code.





Mitigation: Use Sass mixins and partials to reduce duplication.



Risk: CRA’s Webpack build times slow down development.





Mitigation: Optimize Webpack config; use react-scripts defaults initially.



Phase 3: Advanced Features Development (Weeks 10–12, July 3–July 23, 2025)

Objective

Add digital/physical invite delivery, RSVP functionality, and admin dashboard, styled with CSS Modules and Sass.

Milestones





Digital and physical invite delivery implemented.



RSVP system functional.



Admin dashboard completed.

Tasks





Digital and Physical Invites (Weeks 10–11, 8 days):





Generate PDFs for digital invites using pdfkit (Node.js Firebase Function) or jsPDF (client-side).



Store PDFs in Firebase Storage and provide download links.



Integrate with print service API (e.g., Printful) for physical orders.



Allow sharing via WhatsApp/email using APIs.



Style download/share UI with InviteDelivery.module.scss.



Test PDF generation and sharing flows.



Assigned: Backend Developer, Frontend Developer.



Dependencies: Phase 2 (customizations, orders).



RSVP and Guest Features (Week 11, 4 days):





Create RSVP form (React component) styled with RSVP.module.scss.



Store responses in Firestore (rsvp subcollection under orders).



Display event details (date, venue) on e-invite page, styled with EInvite.module.scss.



Test RSVP submission and data retrieval.



Assigned: Frontend Developer, Backend Developer.



Dependencies: Task 1 (e-invites).



Admin Dashboard (Week 12, 5 days):





Build admin interface (React components) styled with AdminDashboard.module.scss to:





Upload/edit/delete templates (templates collection).



View/update order statuses (orders collection).



Manage users (users collection).



Add analytics (e.g., total sales, popular templates) using Firestore queries.



Secure dashboard with admin-only access (Firebase Authentication roles).



Write tests for admin features.



Assigned: Frontend Developer, Backend Developer.



Dependencies: Phase 2 (core features).

Deliverables





PDF generation and sharing for digital invites, styled with CSS Modules.



Physical order integration with print service.



RSVP system for e-invites, styled with Sass.



Admin dashboard with template, order, and user management.



Tests for advanced features.

Risks





Risk: Styling inconsistencies across components.





Mitigation: Enforce style guide; use Sass variables for consistency.



Risk: Print service API integration delays.





Mitigation: Research API docs early; have fallback (manual printing process).



Phase 4: Testing, Optimization, and Deployment (Weeks 13–16, July 24–August 31, 2025)

Objective

Ensure the application is bug-free, optimized, and production-ready, using CRA’s Webpack for builds.

Milestones





Application fully tested.



Performance optimized.



Production deployment completed.

Tasks





Testing (Weeks 13–14, 10 days):





Write unit tests for React components (Jest, React Testing Library).



Test Firebase Functions and APIs (Mocha or Jest).



Perform integration tests for authentication, payments, and PDF generation.



Conduct manual testing for UI/UX across devices (mobile, tablet, desktop).



Test security (e.g., unauthorized access, payment flows).



Assigned: QA Engineer, Frontend Developer, Backend Developer.



Dependencies: Phase 3 (all features).



Optimization (Week 15, 5 days):





Optimize image loading with lazy loading and compression.



Minimize bundle size (code splitting with CRA’s React.lazy, Webpack optimizations).



Set up caching with Cloudflare CDN for static assets.



Monitor Firebase usage and optimize Firestore queries.



Assigned: Frontend Developer, Backend Developer.



Dependencies: Task 1 (testing).



Deployment and Documentation (Week 16, 5 days):





Deploy React app to Firebase Hosting.



Deploy Firebase Functions and Node.js APIs (if any) to Firebase or Heroku.



Verify production environment (authentication, payments, PDFs).



Write documentation for:





Codebase (README, API endpoints).



Maintenance (Firebase monitoring, backups).



User guides (for admins and customers).



Train stakeholders on admin dashboard usage.



Assigned: Project Manager, Frontend Developer, Backend Developer.



Dependencies: Task 2 (optimization).

Deliverables





Fully tested application (unit, integration, manual tests).



Optimized performance (fast load times, minimal bundle size).



Production-ready deployment on Firebase.



Comprehensive documentation and training materials.

Risks





Risk: CRA’s larger bundle size impacts performance.





Mitigation: Use code splitting, lazy loading, and Webpack optimizations.



Risk: Firebase costs exceed budget.





Mitigation: Set Budget Alerts; optimize queries and Storage usage.