<div align="center">

# 🏆 PC Tracker

### Tracks the performances of AUST's team across various Programming Contests.

**[🚀 Live Demo →](https://aust-pc-tracker.vercel.app)**

<br/>

[![License: AGPL v3](https://img.shields.io/badge/License-AGPL_v3-blue.svg)](LICENSE)
[![React](https://img.shields.io/badge/React-18-61DAFB?logo=react&logoColor=white)](https://react.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5-3178C6?logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Vite](https://img.shields.io/badge/Vite-4-646CFF?logo=vite&logoColor=white)](https://vitejs.dev/)
[![Docker](https://img.shields.io/badge/Docker-ready-2496ED?logo=docker&logoColor=white)](https://www.docker.com/)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

[![wakatime](https://wakatime.com/badge/github/piru72/PC_TRACKER.svg)](https://wakatime.com/badge/github/piru72/PC_TRACKER)

</div>

---

## 📸 Screenshots

### Summary of the contests

![Summary of the contests](project_screenshot/image.png)

### Contest details for downloading

![Contest details for downloading](project_screenshot/image-1.png)

### List of contestants

![List of contestants](project_screenshot/image-2.png)

### Contestant details

![Contestant details](project_screenshot/image-3.png)

---

## ✨ Features

- **Contest summary** — at-a-glance view of the contests AUST teams have participated in.
- **Downloadable contest details** — export contest standings as image/data for sharing.
- **Contestant list** — browse every team and contestant.
- **Contestant details** — drill into an individual team's or contestant's performance.
- **Scraper toolkit** — Python scrapers (`Scrapper/`) that pull standings from platforms such as [Toph](https://toph.co/) into structured JSON.

---

## 🚀 Tech Stack

| Layer        | Technology                                                                 |
| ------------ | -------------------------------------------------------------------------- |
| Language     | TypeScript 5                                                               |
| Framework    | React 18                                                                   |
| Build tool   | Vite 4 (`@vitejs/plugin-react-swc`)                                         |
| UI           | Chakra UI, Emotion, Framer Motion                                          |
| Routing      | React Router DOM                                                           |
| Data         | PapaParse / SheetJS (`xlsx`) — CSV-driven, fetched from `VITE_REACT_APP_CSV_URL` |
| Export       | `html-to-image`, `html2canvas`, `file-saver`, `downloadjs`                 |
| Markdown     | `react-markdown` + `remark-gfm`                                            |
| Scrapers     | Python (`pandas`) under `Scrapper/`                                        |
| Container    | Docker (multi-stage build → Nginx)                                         |
| Hosting      | Vercel                                                                     |

---

## 📦 Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (LTS recommended) and npm
- Optionally, [Docker](https://www.docker.com/) for the containerized workflow

### 1. Clone the repository

```bash
git clone https://github.com/parvez-ahammed/pc-tracker.git
cd pc-tracker
```

### 2. Configure environment variables

Copy `example.env` to `.env` and point it at your contest data CSV:

```bash
cp example.env .env
```

```env
VITE_REACT_APP_CSV_URL=<url-to-your-contest-data-csv>
```

### 3. Run locally with npm

```bash
npm install
npm run dev      # start the Vite dev server
```

Other available scripts (from `package.json`):

| Script            | Description                          |
| ----------------- | ------------------------------------ |
| `npm run dev`     | Start the Vite dev server            |
| `npm run build`   | Type-check (`tsc`) and build for production |
| `npm run preview` | Preview the production build locally |
| `npm run lint`    | Run ESLint                           |

### 4. Run with Docker

```bash
docker compose up -d
```

The app is then served at [http://localhost:8080](http://localhost:8080) (mapped from the container's Nginx on port 80).

---

## 🤝 Contributing

Contributions are welcome! Please read **[CONTRIBUTING.md](CONTRIBUTING.md)** for guidelines on adding features and new contests. Also see our **[Code of Conduct](CODE_OF_CONDUCT.md)** and **[Security Policy](SECURITY.md)**.

---

## 🙏 Acknowledgements

Thanks to the AUST programming teams for their hard work and dedication, and to [Vercel](https://vercel.com/) for hosting the project.

---

## 📄 License

This project is licensed under the **GNU Affero General Public License v3.0**. See the [LICENSE](LICENSE) file for details.

© 2026 Parvez Ahammed
