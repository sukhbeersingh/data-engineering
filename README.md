# Data Engineering Guide

Welcome to the Data Engineering Guide! This comprehensive resource covers essential concepts, tools, and best practices in the field of data engineering.

## What You'll Learn

This guide covers:

- **Data Pipeline Architecture**: Design patterns and best practices for building robust data pipelines
- **Data Storage Solutions**: Understanding different storage systems and when to use them
- **Data Processing Frameworks**: Overview of popular processing tools and frameworks
- **Data Quality & Governance**: Ensuring data reliability and compliance
- **Cloud Platforms**: Working with cloud-based data engineering services
- **Best Practices**: Industry standards and proven methodologies

## Getting Started

Navigate through the chapters using the table of contents to explore different aspects of data engineering. Each section includes practical examples and real-world scenarios.

## Development Setup

This documentation site is built using [HonKit](https://github.com/honkit/honkit) (a GitBook community fork) and is automatically deployed to GitHub Pages.

### Prerequisites

- Node.js (version 16 or higher)
- npm

### Local Development

1. Clone the repository:
   ```bash
   git clone https://github.com/sukhbeersingh/data-engineering.git
   cd data-engineering
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Start the development server:
   ```bash
   npm run dev
   ```

4. Open your browser and navigate to `http://localhost:4000`

### Available Scripts

- `npm run build` - Build the static site for production
- `npm run dev` - Start the development server with live reload
- `npm run docs:build` - Build the GitBook
- `npm run docs:serve` - Serve the GitBook locally

### Building for Production

To build the site for production:

```bash
npm run build
```

The generated static files will be in the `_book` directory.

## Deployment

This site is automatically deployed to GitHub Pages using GitHub Actions when changes are pushed to the `main` branch. The workflow:

1. Installs Node.js and dependencies
2. Builds the GitBook
3. Deploys the generated site to GitHub Pages

## Contributing

This guide is a living document. Contributions and feedback are welcome to help improve the content and keep it up-to-date with the latest industry trends.

### Adding New Content

1. Create new markdown files in the `chapters/` directory
2. Update the `SUMMARY.md` file to include your new content in the table of contents
3. Test locally using `npm run dev`
4. Submit a pull request

### Project Structure

```
├── .github/workflows/    # GitHub Actions workflows
├── chapters/            # Documentation chapters
├── _book/              # Generated static site (ignored in git)
├── book.json           # GitBook configuration
├── SUMMARY.md          # Table of contents
├── README.md           # This file
└── package.json        # Node.js dependencies and scripts
```

## License

This project is licensed under the ISC License.