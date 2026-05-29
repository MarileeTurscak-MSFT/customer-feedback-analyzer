# Customer Feedback Analyzer

> AI-powered skills for analyzing customer feedback — weekly summaries and cumulative trend reports

![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

## Overview

Customer Feedback Analyzer provides AI skills that turn raw customer feedback into structured, actionable reports.

- **Weekly Feedback Analyzer** processes meeting transcripts and notes from the past week.
- **Cumulative Feedback Report** synthesizes all historical feedback into trends, ranked features, bugs, and sentiment.
- **Social Sentiment Scanner** searches Reddit, Stack Overflow, and X for public customer sentiment about any product.
- **Resolution Status Tracker** cross-references customer feedback with your issue tracker to report what's been fixed, what's on the roadmap, and what's still open.
- **Asset Gap Tracker** identifies missing docs, videos, labs, and marketing materials causing customer friction, and tracks their creation status.
- **Customer Usage Tracker** tracks product adoption metrics: total customers, advanced deployers, MAU, WAU, and at-risk accounts.
- **Bug Tracker** tracks all customer-reported bugs with severity, resolution status, patterns, and velocity metrics.
- **Feature Request Tracker** ranks customer feature requests by demand, tracks roadmap status, and identifies untracked asks.
- All skills generate **markdown reports** and **visual HTML dashboards**.
- Works with **GitHub Copilot, Claude, ChatGPT, or any LLM agent**.

## Features

- 📅 Weekly feedback summaries with takeaways, feature requests, bugs, quotes
- 📊 Cumulative trend analysis across all feedback history
- 🌐 Social sentiment scanning across Reddit, Stack Overflow, and X
- ✅ Resolution tracking — what's fixed, roadmapped, backlogged, or missing
- 📂 Asset gap tracking — missing docs, videos, labs, and marketing materials
- 👥 Customer usage tracking — adoption depth, MAU/WAU, at-risk accounts
- 🐛 Bug tracking — severity, resolution velocity, pattern detection
- 💡 Feature request tracking — demand ranking, roadmap status, gap detection
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

### 4. Resolution Status Tracker

1. Cross-references customer feedback with your issue tracker (ADO, GitHub Issues, Jira)
2. Classifies each item as resolved, on roadmap, backlogged, open, or untracked
3. Calculates resolution rate and roadmap coverage metrics
4. Flags customer-reported items with no matching work item

### 5. Asset Gap Tracker

1. Scans feedback for signals of missing or hard-to-find enablement assets
2. Categorizes gaps by type: docs, videos, labs, samples, marketing, FAQs
3. Identifies friction hotspots where multiple gaps cluster
4. Tracks creation status of each asset from missing through resolved

### 6. Customer Usage Tracker

1. Connects to your data source (telemetry API, database, CSV, or manual input)
2. Calculates deployment depth per customer (number of features used)
3. Classifies customers as advanced deployers, MAU, WAU, at-risk, or churned
4. Flags at-risk customers with specific engagement signals

### 7. Bug Tracker

1. Scans feedback for all customer-reported bugs
2. Classifies by severity (critical/high/medium/low) based on customer impact
3. Cross-references with issue tracker for resolution status
4. Identifies bug patterns, resolution velocity, and untracked bugs

### 8. Feature Request Tracker

1. Extracts all feature requests from feedback sources
2. Deduplicates and ranks by customer demand count
3. Cross-references with issue tracker and roadmap
4. Flags requests with no matching work item

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
