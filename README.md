# Jinkyung Kim

**Full-Stack / Frontend Developer** · React, TypeScript, Next.js · Python/FastAPI, Node.js · AWS

Relocating to Stockholm in December 2026 · **Right to work in Sweden** (EU-citizen family member, no sponsorship needed)

[LinkedIn](https://www.linkedin.com/in/jinkyung-kim-64a28b1b2/) · scene1993@gmail.com

## 🚀 About Me

Full-stack developer, frontend-strong: 3+ years of full-time industry experience, mostly frontend (Next.js/TypeScript since 2022), plus a year of part-time full-stack work alongside a Master's: Python/FastAPI and Node.js back-ends, AWS/Terraform delivery and daily use of AI coding agents (Claude Code). Most recently built a two-sided catering marketplace solo for a Sydney client, from requirements to a deployed pre-launch build and handover; earlier developed the CONNECT marketplace front-end and its NFT copyright feature (4,000+ NFTs on Polygon) at CLO Virtual Fashion.

> Client and company code lives in private repositories, so the links and screenshots below show the deployed builds and public on-chain records.

## 🧑🏻‍💻 Work Experiences

### 1. Full-Stack Developer (part-time contract)
#### Cloud Riverdale · Sydney (Sep 2025 – Sep 2026)

Reported to the CEO throughout; PR code review with a fellow developer for about the first half of the engagement.

**GoCatering** — two-sided catering marketplace · [gocatering.com.au](https://gocatering.com.au) · Jun 2026 – Sep 2026  
`Next.js 16` `React 19` `TypeScript` `FastAPI` `PostgreSQL` `Docker` `AWS` `GitHub Actions` `Playwright`

<img width="1614" height="957" alt="gocatering" src="https://github.com/user-attachments/assets/6596138c-d000-4101-b061-91fe00808d8d" />

- Sole engineer from requirements to a deployed Milestone 1 build and client handover: React 19/Next.js 16 front-end (26 pages, three role-based UIs) on a FastAPI/PostgreSQL back-end with 121 REST endpoints.
- Built the customer search and booking flow (URL-synced filters), a caterer dashboard (7-step onboarding, listing editor with live preview, availability rules) and an admin console (KYC-style review, approve/pause, 30-day trials, per-caterer fee overrides); 16 shared components and a typed API client with automatic token refresh.
- Bookings modelled as an explicit state machine (request → accept / decline / counter-offer → change → tiered-refund cancellation) with calendar holds against double booking; every transition validated server-side.
- Business rules enforced in the back-end, not the UI: no caterer is listed without food-safety and insurance documents, and booking quotes are calculated server-side.
- Seven weekly client demos with written demo guides; triaged the client's 45-item UAT sheet and closed 36 of 45 within ten days; releases verified with Playwright runs and API smoke checks.
- Right-sized hosting for a pre-launch product: one EC2 host with Docker Compose (Caddy, Next.js, FastAPI) at ~US$15/month instead of the planned Kubernetes; GitHub Actions deploys each push to main, then runs a health check.

**EternalRecord** — document-integrity service on Polygon · [sfx-d.com](https://www.sfx-d.com/) · Feb 2026 – Jun 2026  
`Next.js` `FastAPI` `Solidity` `Hardhat` `Terraform` `AWS ECS Fargate`

<img width="1601" height="946" alt="sfx-d" src="https://github.com/user-attachments/assets/6ce511c1-b2a7-46b5-8905-c0f01024d2f0" />

- Built the Next.js front-end, FastAPI back-end (AES-256-GCM encryption) and Solidity contracts with Hardhat tests; issuers record documents with email-OTP login only, verifiers need no account.
- Provisioned AWS with Terraform (VPC, ALB, ECS Fargate Spot, ECR, RDS, Route 53) and path-filtered GitHub Actions CI with OIDC push to ECR; wrote the Go-vs-Python and EKS-vs-Fargate decision records (ADRs).

**sfx-a** — financial-accounts platform (a user's accounts in one view), internship · Sep 2025 – Feb 2026  
`Next.js` `Node.js` `Xero API` `AWS`

<img width="1610" height="958" alt="sfx-a" src="https://github.com/user-attachments/assets/2f305cb1-0ed1-4d32-8de6-7c11b9467496" />

- Six months on the inherited Next.js front-end and Node.js back-end; kept the stack rather than rewrite it (time, cost).
- Integrated Xero accounting data through the Xero API (OAuth 2.0), built against a Xero demo company, so any Xero user can see their books inside sfx-a.
- Repaired, then rebuilt, the CI/CD pipeline (automated build, test and deploy); wrote an AWS cost-optimisation proposal for the EC2/RDS estate (−17.5% annual, each change rated by risk and downtime).

### 2. Front-End Developer & Smart Contract Engineer
#### CLO Virtual Fashion · Seoul (Jun 2022 – Jan 2025)

Maker of CLO and Marvelous Designer (3D garment simulation). I worked on CONNECT, CLO's 3D asset marketplace.

<img width="1725" alt="connect-closet" src="https://github.com/user-attachments/assets/7660a7eb-7a75-467c-b83b-055571ea8120" />

- Built the CONNECT marketplace front-end (Next.js/TypeScript, Tailwind CSS) in a five-person frontend team with PR code review, working daily with product planning and design; Lighthouse errors −25%, performance and accessibility scores above 80.
- Implemented the 'Order' feature in the CONNECT back-office, streamlining order-flow management and tracking.
- Customised and deployed ERC-721 contracts on Polygon mainnet with a consume-once transfer that locks each NFT to its owner; 4,000+ NFTs issued, every mint and transfer verifiable on PolygonScan (see Digital Stamp below), via a Thirdweb/TypeScript minting layer (MetaMask/WalletConnect, IPFS metadata); production monitoring with Datadog.

### 3. UI Developer
#### Feelway · Seoul (Sep 2020 – Apr 2021)

Luxury resale platform.

<a href="https://www.feelway.com/">
    <img width="1725" alt="feelway" src="https://github.com/user-attachments/assets/560e30a0-efe0-40b8-8fdf-5365e2366c81" />
</a>

- Built 20+ responsive campaign landing pages (HTML, CSS, JavaScript/jQuery) with the design team: +15% campaign engagement, −10% mobile drop-off.

## 🌟 Projects

### Digital Stamp — blockchain copyright records for CONNECT users (CLO Virtual Fashion)

<img width="1726" alt="CONNECT Digital Stamp" src="https://github.com/user-attachments/assets/59a76a65-a8ad-41f1-ae32-8ef1c156e72e" />

*Screenshot from when the feature was live. CLO has since retired the NFT feature from CONNECT; the contract and its 4,000+ records remain on Polygon mainnet (links below).*

Digital Stamp issued a customer's 3D artwork information as an NFT and transferred it to the customer's wallet. The modified ERC-721 contract allows each token exactly one transfer: once it reaches the customer's wallet the remaining transfer count drops to 0, so the token stays bound to that wallet as a record of ownership and creation time, even if the artwork is later copied.

### On-chain verification details
- Modified ERC-721 Contract: 0xeb579c015d87d2e648066d27321d16d3ae1c2176
- Company Deployment Wallet: 0xa55BF4e73eCE4444a8196875C72796C2Db51Dd9C
- PolygonScan: https://polygonscan.com/address/0xeb579c015d87d2e648066d27321d16d3ae1c2176
- All 4,000+ minting, transfer, and ownership proof transactions remain verifiable on Polygon mainnet, independent of any centralised service.
- Even if a 3D artwork is copied, the on-chain record shows the original owner and creation timestamp.
- Monitored on-chain transactions and contract performance in production with Datadog.

## 🛠️ Skills & Technologies

- **Frontend:** React, Next.js (App Router), TypeScript, JavaScript (ES6+), Tailwind CSS, HTML/CSS, Lighthouse tuning
- **Backend:** Python (FastAPI, SQLAlchemy, Alembic), Node.js, REST APIs, PostgreSQL, JWT/OAuth 2.0
- **Cloud & DevOps:** AWS (EC2, ECS Fargate, RDS, CloudWatch), Terraform, Docker, GitHub Actions CI/CD, Datadog
- **Testing & quality:** Playwright (end-to-end), Hardhat contract tests, API smoke tests, ESLint
- **Blockchain:** Solidity (ERC-721), Hardhat, Thirdweb SDK, Polygon mainnet, IPFS, MetaMask/WalletConnect
- **Ways of working:** Git/GitHub with PR code review, Jira, Confluence, Slack, AI-assisted development (Claude Code)

## 🎓 Education & Training

- **University of Technology Sydney** — Master of Information Technology, Enterprise Software Development (coursework focus: networking & cybersecurity) · Feb 2025 – Oct 2026
- **Hanyang University** — B.A. Cultural Anthropology; B.F.A. Communication Design · Mar 2013 – Feb 2019
- **KYUNGIL Academy** — Government-funded Blockchain & Software Programme · Oct 2021 – May 2022
- **Code States** — Front-end Engineering Bootcamp · Feb 2020 – Jul 2020

## 🌐 Languages

English — professional working proficiency · Korean — native
