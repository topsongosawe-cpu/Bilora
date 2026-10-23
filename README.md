# Billora starter

Responsive Next.js prototype for an invoicing, receipt and quotation SaaS.

## Included
- Dashboard UI with demo KPIs and recent documents
- Search and document filters
- Create-document modal with basic validation
- Business profile settings screen
- Responsive layout for mobile and desktop

## Not connected yet
This prototype stores new documents only in temporary browser state. Authentication, database persistence, production PDF export, logo/signature upload, WhatsApp delivery, Paystack billing, subscription enforcement and deployment are not implemented yet.

## Run locally
Install a current Node.js LTS version, then run `npm install` and `npm run dev`; open `http://localhost:3000`.

Copy `.env.example` to `.env.local` only after creating a Supabase project. Never expose a Supabase service-role key in browser code. All customer/document tables must use row-level security. Subscription status must come from verified server-side payment events, never uploaded payment screenshots.

## Build plan
1. Create Supabase project and GitHub repository.
2. Implement auth, workspace ownership, and secure database tables.
3. Add complete document editor, line items, taxes, discounts, numbering and due dates.
4. Implement print styles and PDF export.
5. Add logo and drawn/imported signature.
6. Add verified Paystack subscription webhooks.
7. Add official WhatsApp Business Platform integration after account approval.
8. Test and deploy.
