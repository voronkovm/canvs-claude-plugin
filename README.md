# Canvs Plugin for Claude Code

A [Claude Code plugin](https://docs.anthropic.com/en/docs/claude-code/plugins) for creating and manipulating collaborative whiteboards with [Canvs.io](https://canvs.io).

## What's included

- **Canvs skill** — teaches Claude how to effectively use Canvs tools (Mermaid-first strategy, iterative workflow, element properties)
- **MCP server config** — automatically connects the Canvs.io MCP server (no manual setup needed)

## What you can do

Ask Claude to create:

- **Diagrams** — flowcharts, sequence diagrams, class diagrams, mind maps
- **Wireframes** — UI layouts, app screens, website mockups
- **Illustrations** — shapes, icons, visual explanations
- **Org charts** — team structures, hierarchies
- **Process flows** — workflows, decision trees, pipelines

## Installation

```bash
claude plugin install canvs
```

Or manually:

```bash
git clone --recursive https://github.com/voronkovm/canvs-claude-plugin.git
claude plugin install ./canvs-claude-plugin
```

## Usage

Claude will automatically use Canvs when you ask to draw or visualize something:

```
> Draw a flowchart showing the CI/CD pipeline
> Create a wireframe for a dashboard page
> Visualize the microservices architecture
```

Or invoke the skill directly:

```
> /canvs:canvs sequence diagram of API request flow
```

## Structure

```
canvs-claude-plugin/
├── .claude-plugin/
│   └── plugin.json          # Plugin manifest
├── .mcp.json                # Canvs MCP server configuration
├── skills/
│   └── canvs-skill/         # Skill submodule (github.com/voronkovm/canvs-skill)
│       └── .claude/skills/canvs/SKILL.md
├── LICENSE
└── README.md
```

## License

MIT
