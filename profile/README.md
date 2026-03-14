## Hi there 👋

# 🚀 Telecom Test Tools

Open-source tools designed for **telecom and 5G test engineers**.

The **Telecom Test Toolkit (TTT)** ecosystem provides a suite of specialized tools for automated log analysis, quality scoring, and reporting.

---

## 🧩 Architecture

```
┌─────────────────────────────┐
│    ttt CLI (Orchestrator)   │
└─────────┬───────────────────┘
          │
┌─────────────┼─────────────┐
│       Plugin System       │
│  (entry-point discovery)   │
└─────────────┼─────────────┘
          │
┌────────────────────────┼────────────────────────┐
│                        │                        │
┌────▼─────┐        ┌─────▼──────┐        ┌─────▼──────┐
│ Analyzers│        │   Scorers  │        │  Reporters │
├──────────┤        ├────────────┤        ├────────────┤
│ testwatch│───────►│  flakiness │───────►│ report-gen │
│ log-analz│        │   scorer   │        │  dashboard │
│ testscope│        └────────────┘        └──────────┘
│                        │                        │
└────────────────────────┼────────────────────────┘
          │
┌─────────▼──────────┐
│  Shared Data Store │
│   (ttt_data.json)  │
└────────────────────┘
```

The toolkit uses a plugin-based architecture where specialized tools are discovered and orchestrated by the central `ttt` command-line interface.

---

# 📦 Ecosystem Repositories

## 🏗️ Core & Orchestration
### [Telecom Test Toolkit](https://github.com/telecom-test-tools/telecom-test-toolkit)
The central orchestrator and CLI that manages the test analysis pipeline.

---

## 🔍 Analyzers
Tools that process raw logs and extract meaningful events.

- **[5GTestScope](https://github.com/telecom-test-tools/5gtestscope)**: Smart log analyzer for gNodeB and simulator logs.
- **[TestWatch](https://github.com/telecom-test-tools/testwatch)**: Real-time log monitoring for regression runs.
- **[5G Log Analyzer](https://github.com/telecom-test-tools/5g-log-analyzer)**: General log parsing for telecom test logs.

---

## ⚖️ Scorers
Tools that provide metrics and quality scores based on analysis.

- **[Regression Flakiness Analyzer](https://github.com/telecom-test-tools/Regression-Flakiness-Heatmap-Scorer)**: Detect flaky tests using failure patterns and heatmaps.

---

## 📊 Reporters & Dashboards
Tools for visualizing and sharing results.

- **[Test Report Generator](https://github.com/telecom-test-tools/test-report-gen)**: Generate rich HTML test reports from automation logs.
- **[Test Monitor Dashboard](https://github.com/telecom-test-tools/test-monitor-dashboard)**: Streamlit dashboard for automation test monitoring.

---

# 🎯 Vision

Build the **best open-source toolkit for telecom test engineers**, breaking down silos between testing tools.
