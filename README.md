## Overview

This is an agentic autoresearch and deployment harness for the Numerai tournament (Unity) that combines:

- Orchestrating agents with instructions in `program.md` (agent-neutral - Claude, Codex, etc.)
- Autoresearch inspired by Karpathy in `autoresearch-src/prepare.py`, `autoresearch-src/train.py`, and `program.md` for feature analysis, experimentation loop, and logging results. 
- Feature analysis with dynamic per-era feature selection
- Bayesian optimization with Optuna and MLflow-backed experiment tracking
- Walk-forward training and time-series cross-validation
- Agent tool use for the weekly loop: a JSON CLI of pipeline tools driven by agent skills, plus an MCP client for Numerai's official MCP server to handle submissions
- Structured weekly submissions with generated HTML summary reports
