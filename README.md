# HTML to Design Spec

Convert HTML prototypes into design specifications and reconstruction-ready product intelligence for AI coding agents.

## Overview

This skill converts interactive web prototypes or HTML design drafts from tools like Lovable, v0, Bolt, or similar into design specifications and reconstruction-ready product intelligence. It explores prototypes, deduplicates UI states, captures evidence, and writes outputs that preserve both interaction flow and visual style for reconstruction.

## Features

- **Comprehensive Analysis**: Explore HTML prototypes and capture UI states
- **Structured Outputs**: Generate pages.json, flows.json, graph.json, style.json
- **Visual Documentation**: Capture screenshots for different viewports
- **Design Specifications**: Create detailed specs and reconstruction prompts
- **Workflow Automation**: Scripts to create analysis directory structure

## Output Structure

Each analysis run creates a directory with:
- `pages.json` - Page/state inventory
- `flows.json` - User flows and interaction transitions
- `graph.json` - UI state graph with nodes and edges
- `style.json` - Design tokens and component styling
- `screenshots/` - Visual evidence for different states and viewports
- `prompts/` - AI reconstruction prompts
- `specs/` - Detailed design specifications

## Usage

The skill is designed for use with AI coding agents. The main workflow is documented in `SKILL.md`.

### Quick Start

1. Use the `scripts/create_run_dir.py` script to create an analysis directory:
   ```bash
   python scripts/create_run_dir.py /path/to/project --name "my-prototype" --target "http://localhost:3000"
   ```

2. Follow the workflow in `SKILL.md` to analyze the prototype

3. Generate structured outputs for reconstruction

## References

- `SKILL.md` - Complete skill documentation and workflow
- `references/output-schemas.md` - JSON schema definitions for output files
- `agents/openai.yaml` - Agent interface configuration

## License

This skill is ported from the original [skills repository](https://github.com/opoojkk/skills).