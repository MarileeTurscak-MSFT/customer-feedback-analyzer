# Customer Feedback Analyzer

> AI-powered skills for analyzing customer feedback — weekly summaries and cumulative trend reports

![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

## Overview

Customer Feedback Analyzer provides two AI skills that turn raw customer feedback into structured, actionable reports.

- **Weekly Feedback Analyzer** processes meeting transcripts and notes from the past week.
- **Cumulative Feedback Report** synthesizes all historical feedback into trends, ranked features, bugs, and sentiment.
- **Social Sentiment Scanner** searches Reddit, Stack Overflow, and X for public customer sentiment about any product.
- All skills generate **markdown reports** and **visual HTML dashboards**.
- Works with **GitHub Copilot, Claude, ChatGPT, or any LLM agent**.

## Features

- 📅 Weekly feedback summaries with takeaways, feature requests, bugs, quotes
- 📊 Cumulative trend analysis across all feedback history
- 🌐 Social sentiment scanning across Reddit, Stack Overflow, and X
- 📈 Interactive HTML dashboards with charts and visualizations
- 🔌 Portable — works with any LLM and any transcript source
- 🛡️ Privacy-first — runs locally, no data sent to third parties
- 📝 Reusable templates for structured feedback capture

## Quick Start

1. Clone the repo.
2. Copy `skills/` to your project's `.github/prompts/` folder.
3. Configure the settings block at the top of each skill.
4. Point the skill at your feedback folder.
5. Run with your preferred AI agent.

## Supported Transcript Sources

These skills are designed to work with multiple input modes:

- **Local files**: Exported transcripts from Teams, Zoom, Google Meet, or any meeting tool
- **Pasted text**: Copy/paste transcripts directly into chat
- **Feedback repo**: Markdown files in a folder following the included template
- **MCP integration**: Connect your own meeting transcript MCP server
- **CRM exports**: Notes exported from Salesforce, HubSpot, or other CRM tools

## Repo Structure

```text
customer-feedback-analyzer/
├─ README.md                  # Project overview, setup, and usage guidance
├─ LICENSE                    # MIT license
├─ CONTRIBUTING.md            # Contribution rules and data handling expectations
├─ dashboards/                # Self-contained HTML dashboard files and related assets
├─ examples/                  # Example reports, dashboards, and sample outputs
│  └─ sample-feedback/        # Fictional sample feedback data and generated artifacts
├─ skills/                    # Reusable AI skill prompts for weekly and cumulative analysis
└─ templates/                 # Reusable markdown templates for collecting customer feedback
```

## How It Works

### 1. Weekly Feedback Analyzer

1. Discovers meetings from the target time window
2. Extracts insights from transcripts and notes
3. Generates a weekly markdown summary
4. Creates per-meeting notes for traceability

### 2. Cumulative Feedback Report

1. Reads all feedback files in the configured folder
2. Deduplicates repeated requests, bugs, and themes
3. Ranks findings by frequency and impact
4. Generates a comprehensive markdown report and dashboard

### 3. Social Sentiment Scanner

1. Takes a product name and optional aliases as input
2. Searches Reddit, Stack Overflow, and X for recent mentions
3. Classifies each post by sentiment, category, and engagement
4. Generates a report with themes, feature requests, bugs, quotes, and action items

## HTML Dashboards

- Self-contained single-file HTML — no external dependencies
- Open in any browser, works offline
- Pre-loaded with sample data from a fictional **AI Cost Analyzer** product
- Replace the JSON data block at the top with your own data

## Sample Data

- Includes example feedback files and reports for a fictional product
- All company names are fictional (`Contoso Financial`, `Northwind Traders`, and similar examples)
- Use as a reference for formatting your own feedback

## Configuration

Add a configuration block like this at the top of each skill:

```yaml
# Configuration — customize these for your project
product_name: "Your Product Name"
feedback_folder: "customer-feedback/"
transcript_source: "local"  # local | paste | mcp | repo
team_members: ["Name1", "Name2"]
output_folder: "customer-feedback/"
branch_prefix: "feedback/"
```

## Privacy & Security Guidance

- ⚠️ These skills process customer feedback which may contain sensitive information
- Do NOT upload confidential customer data to unapproved AI models
- Remove customer names, emails, and account IDs before sharing reports externally
- Validate AI-generated summaries before acting on them or sharing with stakeholders
- The HTML dashboards render all data as escaped text (not `innerHTML`) for XSS safety
- When sharing dashboards, ensure they don't contain sensitive customer information

## Screenshots

See `examples/` for sample reports and dashboards.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

MIT License. See [LICENSE](LICENSE).
