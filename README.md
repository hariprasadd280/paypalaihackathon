# PayBounty AI

> An autonomous maintainer agent that audits pull requests, evaluates code quality/security, and dispatches instant PayPal micro-bounties to open-source contributors.

---

## What It Does

Open-source maintainers spend endless hours reviewing PRs, managing micro-tasks, and handling payouts across different platforms. Contributor friction is high, and waiting weeks for manual approvals kills community momentum.

**PayBounty AI** automates this lifecycle:
1. **Monitors GitHub Pull Requests** for open issues and incoming submissions.
2. **Runs automated AI code quality and security checks** on the PR diff (evaluating security risks, test coverage, code style, and task complexity).
3. **Calculates dynamic micro-bounties** based on actual code impact ($5 for minor bug/doc fixes, up to $50+ for complex features).
4. **Triggers instant payouts** directly to the developer's email via PayPal’s Developer Sandbox (`/v1/payments/payouts` API) as soon as high-quality code gets merged.

---

## Tech Stack & APIs Used

- **Frontend:** Vanilla JS / HTML5 / Tailwind CSS
- **Payments Engine:** PayPal Developer Platform (Sandbox Payouts API)
- **AI Engine:** Code auditing & security inspection logic
- **Developer Tools Used:** Postman (for testing payment endpoints), Render (hosting setup)

---

## Key Features

- **Autonomous Payment Dispatch:** No manual approval buttons needed once safety thresholds (score ≥ 8/10) are met.
- **Fiat Payouts for Devs:** Uses PayPal directly so contributors don't need crypto wallets or complex wire setups.
- **Live Terminal & Audit Log:** Clear, transparent audit trails showing exact prompt checks, safety scores, and raw PayPal JSON responses.
- **Rejection Circuit Breakers:** Flags unsafe code patterns (like unhandled edge cases or hardcoded secrets) and rejects payout attempts automatically.

---

## Getting Started / Local Setup

No complex setup or build steps required. The dashboard runs directly in any web browser.

1. **Clone the repo:**
   ```bash
   git clone [https://github.com/YOUR_USERNAME/paypalaihackathon.git](https://github.com/YOUR_USERNAME/paypalaihackathon.git)
   cd paypalaihackathon

Open the application:

Double-click index.html to open it in your browser, OR

Run a basic static server:

Bash
npx serve .
Configure Sandbox Credentials (Optional):

Click API Configuration in the top navigation bar.

Enter your PayPal Sandbox Client ID and Client Secret to test live API calls against the Sandbox environment.

Demo Video & Hosted Link
Live Hosted Demo: [Paste your Netlify or GitHub Pages link here]

Demonstration Video: [Paste your YouTube video link here]

License
This project is licensed under the MIT License - see the LICENSE file for details.
