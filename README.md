# GemsHub Marketplace — Full E2E MVP (Centralized)

This branch provides a starter scaffold for the GemsHub marketplace implementing a centralized, physical-gem marketplace with the following features:
- Seller registration with a one-time registration fee (₹3000)
- Seller KYC document upload and admin review workflow
- Create gem entries and listings
- Buyer checkout via Stripe (Stripe Connect), PayPal, GooglePay, UPI and Bank transfer placeholders
- Platform holds buyer funds in escrow until delivery is confirmed
- Marketplace commissions: 3% seller commission on sales, 4% buyer purchase commission (added on top of listing price)
- Shipping & tracking endpoints

ENVs required (see .env.example)

How to run (local dev):
1. Copy .env.example to .env and fill in values.
2. Create Postgres DB and run the SQL in sql/schema.sql
3. npm install
4. npm run dev

Notes:
- Stripe Connect flows are scaffolded; you must provide STRIPE_SECRET_KEY and set up Connect accounts for sellers (stripe_account_id stored on users table).
- PayPal/GooglePay/UPI/Bank transfer integrations are left as placeholders for future implementation.
