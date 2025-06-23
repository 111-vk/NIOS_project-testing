## this is for testing purposes only, do not use this repository for any other purpose.
# NIOS Web Documentation Site

> **Note:** This is a combined repository for the [nios-students GitHub organization](https://github.com/nios-students), allowing you to run the documentation and resources locally for development, testing, and contribution.

This project is a documentation website for the NIOS Students community, built using [VitePress](https://vitepress.dev/). It provides guides, resources, and community links for NIOS students and contributors.

---

## Table of Contents
- [Project Overview](#project-overview)
- [Features](#features)
- [Getting Started](#getting-started)
- [Development Workflow](#development-workflow)
- [Scripts](#scripts)
- [Custom Theme & Logic](#custom-theme--logic)
- [Directory Structure](#directory-structure)
- [Contributing](#contributing)
- [Community](#community)
- [License](#license)

---

## Project Overview
This repository contains the source code and configuration for the NIOS Students documentation site. The site is built with VitePress, a modern static site generator powered by Vite and Vue 3. It is designed to be fast, customizable, and easy to maintain.

## Features
- **VitePress-powered**: Fast, modern static site generator.
- **Custom Theme**: Includes custom popups, redirects, and styling for a unique user experience.
- **Community Links**: Easy access to the NIOS Students community and resources.
- **Markdown Extensions**: Support for MathJax, Mermaid diagrams, and Python code blocks.
- **CI/CD Integration**: Automated build scripts for deployment and continuous integration.

## Getting Started

### Prerequisites
- [Node.js](https://nodejs.org/) (v18 or higher recommended)
- [npm](https://www.npmjs.com/) (comes with Node.js)

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/111-vk/NIOS_project-testing.git
   cd NIOS_project-testing
   ```
2. Install dependencies:
   ```bash
   npm install
   ```

### Running the Development Server
Start the local development server with hot reload:
```bash
npm run docs:dev
```
The site will be available at `http://localhost:5173` (or as indicated in the terminal).

### Building for Production
Generate the static site for deployment:
```bash
npm run docs:build
```
The output will be in the `docs/.vitepress/dist` directory.

### Previewing the Production Build
Serve the built site locally to verify production output:
```bash
npm run docs:preview
```

## Scripts
| Script           | Description                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| `docs:dev`       | Start the VitePress development server.                                                     |
| `docs:build`     | Build the static site for production.                                                       |
| `docs:preview`   | Preview the production build locally.                                                       |
| `docs:cibuild`   | Run a remote build script (for CI/CD, uses helper script from GitHub).                      |
| `docs:quickrun`  | Run the remote build script, then start the dev server (for quick local testing).            |

## Custom Theme & Logic
- Located in `docs/.vitepress/theme/index.ts`.
- Implements custom popups for first-time visitors.
- Redirects users from deprecated `/wiki` routes to the `/docs/links/` page with an alert.
- Uses VitePress and Vue 3 composition API for theme customization.
- Integrates MathJax, Mermaid, and Python code block plugins for enhanced documentation.

## Directory Structure
```
nios-web/
├── docs/
│   ├── .vitepress/
│   │   ├── theme/
│   │   │   └── index.ts         # Custom theme logic (popups, redirects, etc.)
│   │   └── ...                  # VitePress config files
│   ├── public/                  # Static assets (icons, favicons, etc.)
│   └── ...                      # Documentation markdown files
├── package.json                 # Project scripts and dependencies
├── readme.md                    # Project documentation (this file)
└── ...
```

## Contributing
Contributions are welcome! To contribute:
1. Fork the repository.
2. Create a new branch for your feature or fix.
3. Make your changes and commit them with clear messages.
4. Push to your fork and open a pull request.

For major changes, please open an issue first to discuss what you would like to change.



## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
