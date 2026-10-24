# PayBounty AI

> Autonomous open-source bounty evaluation and instant payouts powered by AI and the PayPal Developer Platform.

PayBounty AI bridges the gap between open-source maintainers and global contributors. Reviewing community pull requests manually takes time, and issuing small payments across borders often involves tedious admin work or complex setup.

PayBounty AI automates code reviews using LLMs and dispatches real-time micro-bounties directly to a developer’s PayPal account the moment their code meets quality and security standards.

---

## Key Features

* **Automated Code Auditing**: Analyzes submitted PR diffs for quality, potential security risks, and overall project impact.
* **Dynamic Bounty Valuation**: Calculates fair payout rates based on code complexity, lines changed, and issue priority.
* **Instant Fiat Payouts**: Connects directly to the **PayPal Payouts API** (Sandbox environment) to send funds straight to the contributor’s email address upon code acceptance.
* **Real-time Agent Console**: Provides transparent logs of the AI's reasoning, test outputs, and JSON payloads for full auditability.

---

## Tech Stack & Sponsor Tools

* **Frontend**: HTML5, Tailwind CSS, JavaScript (ES6)
* **Payment Processing**: PayPal Developer Platform (Sandbox API / Payouts Engine)
* **AI Engine**: LLM-based code evaluation prompt architecture
* **API Testing & Workflows**: Postman (for payload validation)
* **Hosting**: Netlify / GitHub Pages

---

## Getting Started & Local Setup

Because PayBounty AI is built as a lightweight, zero-dependency client application, running it locally requires no build steps or heavy node module installations.

1. **Clone the Repository**
```bash
git clone https://github.com/YOUR_USERNAME/paypalaihackathon.git
cd paypalaihackathon

```


2. **Open the Application**
* Double-click `index.html` to open it directly in any modern browser (Chrome, Firefox, Safari, Edge).
* *Alternatively*, serve it locally via Python:
```bash
python -m http.server 8000

```


Then open `http://localhost:8000` in your browser.



---

## PayPal Sandbox Testing Setup

To test live API triggers inside the app:

1. Open the application and navigate to the **API Credentials Config** tab in the top dashboard.
2. Enter your PayPal Developer **Client ID** and **Client Secret** (from your [PayPal Developer Dashboard](https://developer.paypal.com/)).
3. Toggle the target environment to **Sandbox**.
4. Select any test Pull Request from the Bounty Board and click **Trigger Autonomous AI Audit & PayPal Payout**.

---

## How It Works

```
[ Contributor Submits PR ] 
           │
           ▼
[ AI Code Review Engine ] ──(Fails Security/Quality)──► [ Rejection & Feedback ]
           │
     (Score >= 8/10)
           │
           ▼
[ Dynamic Bounty Calculation ]
           │
           ▼
[ PayPal Payouts API Call ] ──► [ Instant Fiat Delivered to Developer Email ]

```

---

## License

Distributed under the MIT License. See `LICENSE` for more information.
