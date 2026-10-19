# 🌾 Bhu-Drishti: Land-Use & Land Records Intelligence Platform

> A full-stack platform for exploring land-use data, research, geospatial insights, and policy decision support in India.

Bhu-Drishti brings land statistics, public datasets, research publications, geospatial visualizations, anomaly detection, and natural-language exploration together in one dashboard.

## Key Features

- **Interactive map explorer** — explore state-level land-use information and historical trends.
- **Evidence-oriented AI assistant** — ask questions in English, Hindi, or Hinglish and inspect the reasoning behind responses.
- **Anomaly detection** — highlight unusual changes in land-use indicators for further investigation.
- **Historical trends** — compare periods, examine land conversion, and review growth indicators.
- **Policy analysis** — organize evidence for evaluating land-related policies.
- **Dataset explorer** — browse dataset metadata and preview available records.
- **Research library** — discover studies and generate concise summaries and citations.
- **Report export** — prepare reports for review and sharing.
- **Data-ingestion tools** — support CSV/JSON ingestion with validation and audit information.

> **Data note:** Treat model-generated summaries and anomaly flags as decision-support signals, not authoritative conclusions. Verify findings against the linked source datasets and official publications before using them in research or policy decisions. Document dataset provenance, update dates, and limitations wherever applicable.

## Technology Stack

- **Frontend:** React, TypeScript, Vite, Tailwind CSS, Recharts, Lucide React
- **Backend:** Node.js, Express, TypeScript
- **Data:** PostgreSQL, PostGIS, Prisma ORM (with an in-memory fallback where configured)
- **Deployment:** Docker Compose; frontend/backend can be deployed separately
- **AI:** Google Gemini API

## Prerequisites

- Node.js 18 or newer
- npm
- Docker Desktop / Docker Engine (optional, for container-based setup)
- Valid API credentials if enabling the AI-powered features

## Getting Started

### Option 1: Local development

Clone this repository:

```bash
git clone https://github.com/Ishant-Mishra/sih-project.git
cd sih-project
npm install
```

Configure the environment variables required by your setup. **Do not commit API keys, database passwords, or other secrets.** If the project provides an environment template, copy it to a local `.env` file and fill in the values.

Start development:

```bash
npm run dev
```

If your package scripts support running services separately, use:

```bash
npm run dev:server
npm run dev:client
```

Build for production:

```bash
npm run build
```

### Option 2: Docker Compose

```bash
git clone https://github.com/Ishant-Mishra/sih-project.git
cd sih-project
docker compose up --build
```

Review the Compose file and local environment configuration for the actual service ports and credentials. Change default development credentials before using any deployment outside your local machine.

## Database Setup

When PostgreSQL is configured, set `DATABASE_URL` in your local environment, then run the project’s supported database scripts:

```bash
npm run db:generate
npm run db:push
npm run db:seed
```

Run only the scripts that are present in `package.json` and review schema/seed behavior before using a non-development database.

## Deployment Notes

The frontend and backend may be deployed separately, depending on the project configuration. Configure the API base URL and server-side secrets in the relevant hosting dashboards. Never expose a server API key through a `VITE_*` variable, since Vite variables are bundled for client-side use.

## Data Quality & Responsible Use

- Record the source, publication date, geographic coverage, and time period of each dataset.
- Distinguish verified source values from estimates, synthetic/demo data, and AI-generated explanations.
- Display methodology and uncertainty for statistical alerts.
- Validate findings against original government or research sources before citing them in reports.
- Do not use the platform’s outputs as a substitute for legal, land-title, or official administrative verification.

## Contributing

1. Create a feature branch.
2. Keep changes focused and explain the reason for each change.
3. Test the affected functionality.
4. Open a pull request with a summary, screenshots where relevant, and testing notes.

## License

No license is specified here yet. Until a license is added, do not assume that the repository grants permission to reuse or redistribute its code.

---

**Repository:** [Ishant-Mishra/sih-project](https://github.com/Ishant-Mishra/sih-project)
