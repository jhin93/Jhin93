# Jinkyung Kim

**Full-Stack / Frontend Developer** · React, TypeScript, Next.js · Python/FastAPI, Node.js · AWS

Relocating to Stockholm in December 2026 · Right to work in Sweden (EU-citizen family member, no sponsorship needed)

[LinkedIn](https://www.linkedin.com/in/jinkyung-kim-64a28b1b2/) · scene1993@gmail.com

## 🚀 About Me

Full-stack developer, frontend-strong: 4+ years' experience (3+ in React/Next.js and TypeScript) with Python/FastAPI and Node.js back-ends and the AWS, Terraform and GitHub Actions pipelines that ship them. Most recently built a two-sided catering marketplace solo for a Sydney client, from requirements to a deployed pre-launch build and handover; earlier shipped an NFT copyright platform (4,000+ NFTs on Polygon) in a cross-functional product team at CLO Virtual Fashion.

> Client and company code lives in private repositories, so the links below point to live products and public on-chain records.

## 🧑🏻‍💻 Work Experiences

### 1. Full-Stack Developer (Contract)
#### Cloud Riverdale · Sydney (Sep 2025 – Sep 2026)

**GoCatering** — two-sided catering marketplace · [gocatering.com.au](https://gocatering.com.au) · Jun – Sep 2026  
`Next.js 16` `TypeScript` `FastAPI` `PostgreSQL` `Docker` `AWS` `GitHub Actions` `Playwright`

<img width="1614" height="957" alt="gocatering" src="https://github.com/user-attachments/assets/6596138c-d000-4101-b061-91fe00808d8d" />

- Sole engineer from requirements to a deployed Milestone 1 build and client handover: 121 REST endpoints covering caterer onboarding, listings, search and booking.
- Bookings modelled as an explicit state machine (request → accept / decline / counter-offer → change → tiered-refund cancellation) with calendar holds against double booking; every transition validated server-side.
- Business rules enforced in the back-end, not the UI: food-safety and insurance documents required before a caterer is listed; admin console for KYC-style review, approve/pause, 30-day trials and per-caterer fee overrides.
- Seven weekly client demos with written demo guides; triaged the client's 45-item UAT sheet and closed 36 of 45 within ten days; releases verified with Playwright runs and API smoke checks.
- Right-sized hosting for a pre-launch product: one EC2 host with Docker Compose (Caddy, Next.js, FastAPI) at ~US$15/month instead of the planned Kubernetes; GitHub Actions deploys each push to main, then runs a health check.

**EternalRecord** — document-integrity service on Polygon · [sfx-d.com](https://www.sfx-d.com/) · Feb – Jun 2026  
`Next.js` `FastAPI` `Solidity` `Hardhat` `Terraform` `AWS ECS Fargate`

<img width="1601" height="946" alt="sfx-d" src="https://github.com/user-attachments/assets/6ce511c1-b2a7-46b5-8905-c0f01024d2f0" />

- Built the Next.js front-end, FastAPI back-end (AES-256-GCM encryption) and Solidity contracts with Hardhat tests; issuers record documents with email-OTP login only, verifiers need no account.
- Provisioned AWS with Terraform (VPC, ALB, ECS Fargate Spot, ECR, RDS, Route 53) and path-filtered GitHub Actions CI with OIDC push to ECR; wrote the Go-vs-Python and EKS-vs-Fargate decision records (ADRs).

**sfx-a** — financial-accounts platform (a user's accounts in one view) · Sep 2025 – Feb 2026  
`Next.js` `Node.js` `Xero API` `AWS`

<img width="1610" height="958" alt="sfx-a" src="https://github.com/user-attachments/assets/2f305cb1-0ed1-4d32-8de6-7c11b9467496" />

- Worked on the inherited Next.js front-end and Node.js back-end; kept the stack rather than rewrite it (time, cost).
- Integrated Xero accounting data through the Xero API, so any Xero user can see their books inside sfx-a.
- Repaired, then rebuilt, the CI/CD pipeline; wrote an AWS cost-optimisation proposal for the EC2/RDS estate (−17.5% annual, each change rated by risk and downtime).

### 2. Smart Contract & dApp Developer
#### CLO Virtual Fashion · Seoul (Jun 2022 – Jan 2025)

Maker of CLO and Marvelous Designer (3D garment simulation). I worked on CONNECT, CLO's 3D asset marketplace.

<img width="1725" alt="connect-closet" src="https://github.com/user-attachments/assets/7660a7eb-7a75-467c-b83b-055571ea8120" />

- Built the CONNECT marketplace front-end (Next.js/TypeScript) in a cross-functional team, working daily with product planning and design; implemented the back-office 'Order' feature; Lighthouse errors −25%, performance and accessibility scores above 80.
- Customised and deployed ERC-721 contracts on Polygon mainnet giving 3D artworks permanent copyright records; a consume-once transfer moves each NFT once to its owner, then locks it.
- 4,000+ NFTs issued, every mint and transfer verifiable on PolygonScan (see Digital Stamp below); Thirdweb/TypeScript integration layer (automated minting, MetaMask/WalletConnect, IPFS metadata); production monitoring with Datadog.

### 3. UI Developer
#### Feelway · Seoul (Sep 2020 – Apr 2021)

<a href="https://www.feelway.com/">
    <img width="1725" alt="feelway" src="https://github.com/user-attachments/assets/560e30a0-efe0-40b8-8fdf-5365e2366c81" />
</a>  

At Feelway, I contributed to the development and enhancement of a luxury brand trading platform, focusing on front-end development and UI/UX improvements. 

#### 🖥️ Front-End Development: 
My core responsibilities included designing and developing functional pages and event landing pages using HTML, CSS, and JavaScript. I collaborated closely with the design team to ensure pixel-perfect UI implementation and responsive design across various devices while maintaining the web environment and user interfaces to deliver a seamless user experience. Key achievements include developing over 20 event landing pages, boosting user engagement by 15% during promotional campaigns, and enhancing mobile responsiveness, which resulted in a 10% reduction in user drop-off rates on mobile devices.

## 🌟 Projects

### Digital Stamp — blockchain copyright records for CONNECT users (CLO Virtual Fashion)

<img width="1726" alt="CONNECT Digital Stamp" src="https://github.com/user-attachments/assets/59a76a65-a8ad-41f1-ae32-8ef1c156e72e" />

*Screenshot from when the feature was live. CLO has since retired the NFT feature from CONNECT; the contract and its 4,000+ records remain on Polygon mainnet (links below).*

Digital Stamp issued a customer's 3D artwork information as an NFT and transferred it to the customer's wallet. The modified ERC-721 contract allows each token exactly one transfer: once it reaches the customer's wallet the remaining transfer count drops to 0, so the token stays bound to that wallet as a record of ownership and creation time, even if the artwork is later copied.

### On-chain verification details
- Modified ERC-721 Contract: 0xeb579c015d87d2e648066d27321d16d3ae1c2176
- Company Deployment Wallet: 0xa55BF4e73eCE4444a8196875C72796C2Db51Dd9C
- PolygonScan: https://polygonscan.com/address/0xeb579c015d87d2e648066d27321d16d3ae1c2176
- All 4,000+ minting, transfer, and ownership proof transactions will always be available for verification on Polygon mainnet, enabling permanent verification outside a centralized service.
- This transparent, on-chain approach ensures that even if 3D artworks are stolen or copied, the immutable blockchain record proves original ownership and creation timestamp 
- Monitored on-chain transactions and contract performance in the production environment with Datadog

## 🛠️ Skills & Technologies

- **Frontend:** React, Next.js (App Router), TypeScript, JavaScript (ES6+), Tailwind CSS, HTML/CSS, Lighthouse tuning
- **Backend:** Python (FastAPI, SQLAlchemy, Alembic), Node.js, REST APIs, OpenAPI, PostgreSQL, JWT/OAuth 2.0
- **Cloud & DevOps:** AWS (EC2, ECS Fargate, ECR, RDS, ALB, Route 53, Secrets Manager, CloudWatch, SES), Terraform, Docker Compose, GitHub Actions (OIDC), Caddy, Vercel, Neon, Datadog
- **Testing & quality:** Playwright (end-to-end), Hardhat contract tests, API smoke tests, ESLint
- **Blockchain:** Solidity (ERC-721), Hardhat, web3.py, Thirdweb SDK, Polygon PoS, IPFS, MetaMask/WalletConnect
- **Ways of working:** Git/GitHub, Jira, weekly client demos, decision records (ADRs), AI-assisted development (Claude Code)

## 🎓 Education

- **University of Technology Sydney** — Master of Information Technology, Enterprise Software Development · Feb 2025 – Oct 2026
- **Hanyang University** — B.A. Cultural Anthropology; B.F.A. Communication Design · 2013 – 2019

## 🌐 Languages

English — professional working proficiency · Korean — native
