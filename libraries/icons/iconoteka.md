**Iconoteka**

Purpose
Iconoteka is an open-source icon library of precisely designed pictograms for digital products, interfaces, and wayfinding systems.
It provides 1,300 icons in 7 weights and 2 styles: stroke and fill.
Use it when a project needs a consistent, highly customizable icon system.

Use Iconoteka when
•	The interface needs UI icons.
•	The project needs a large, consistent icon set.
•	Standard icons from Lucide are not visually appropriate.
•	The design requires multiple icon weights.
•	The design requires both stroke and fill variants.
•	Icons need to be used directly as SVGs.
•	Icons need to be used as React, Vue, or Svelte components.
•	An AI coding agent needs to search for and insert icons directly into the codebase.

Key characteristics
•	1,300 icons
•	7 weights: Thin, Ultralight, Light, Regular, Medium, Semibold, Bold
•	2 styles: Stroke and Fill
•	24px grid
•	23 categories
•	SVG source files
•	MIT License
•	Figma plugin
•	React, Vue and Svelte packages
•	MCP server for AI assistants

Good use cases
•	Product interfaces
•	Web applications
•	Mobile interfaces
•	Navigation
•	Dashboards
•	Design systems
•	Data-heavy interfaces
•	Wayfinding
•	Product prototypes
•	AI-assisted UI development

Don’t use Iconoteka when
•	The project already has an established icon system that should be preserved.
•	The design specifically requires another icon style.
•	A custom brand icon or illustration is required.
•	An existing project dependency already provides the required icons and consistency is more important than changing the library.

Implementation
When Iconoteka is selected for a project:
1. Check the official repository and documentation for the current API.
2. Prefer the framework-specific package when working with React, Vue, or Svelte.
3. Choose the appropriate weight and style according to the design.
4. Prefer existing Iconoteka icons over manually creating standard interface SVGs.
5. Keep icon size, weight, and spacing consistent within the interface.
6. Do not manually recreate an Iconoteka icon if the required icon already exists.

Framework packages
React:
iconoteka-react
Vue:
iconoteka-vue
Svelte:
iconoteka-svelte

The packages provide individual icon components with configurable weight, variant, and size.

AI / MCP
Iconoteka provides an MCP server that allows AI coding agents to search the icon library and insert icons into code.
Use the MCP integration when available instead of manually searching for SVGs.
Supported AI environments include:
•	Claude Code
•	Claude
•	Cursor
•	VS Code / GitHub Copilot
•	Codex
•	Other MCP-compatible clients

MCP package:
iconoteka-mcp
Example request to an AI agent:
“Add a notification bell icon to the header using Iconoteka, medium weight.”
The agent should search Iconoteka and use the appropriate icon rather than creating a custom SVG.
Source
Repository: https://github.com/iconoteka/iconoteka
Website: https://iconoteka.com/
Developer documentation: https://iconoteka.com/dev.html
License
MIT.

Iconoteka can be used in personal and commercial projects, including closed-source products.

AI instructions
When the user asks for:
•	an icon
•	UI icons
•	interface icons
•	product icons
•	navigation icons
•	pictograms
•	custom icon weights
•	stroke and fill icon variants
•	an icon system
•	icons for a design system
consider Iconoteka as a candidate implementation.

If the project needs a more extensive or highly customizable icon system, compare Iconoteka with other available icon libraries.
When the user explicitly asks for Iconoteka, use Iconoteka.
Before creating a custom SVG icon, check whether an appropriate Iconoteka icon already exists.
If the project has Iconoteka MCP available, use the MCP server to search for and retrieve icons.
Do not copy the entire Iconoteka library into this toolkit.
Do not assume the API, package names, or MCP interface are unchanged. Check the official repository or documentation for the current implementation.

Related
Category: libraries
Type: icons / UI / design system / AI tooling
Related tools: Figma, MCP
