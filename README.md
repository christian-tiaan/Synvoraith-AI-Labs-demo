# Synvoraith AI Labs — Interactive AI & Automation Showcase

**Research. Build. Innovate. Scale.**

Synvoraith AI Labs is an experimental space for exploring practical artificial intelligence and building interactive prototypes. This repository contains the public-facing AI Labs website and **Synvoraith Flow**, a browser-based visual workflow builder that demonstrates how an automation can be designed, connected, simulated, and exported as a workflow blueprint.

> **Prototype notice:** Synvoraith Flow is a demonstration tool. Its Run action simulates node execution in the browser. It does not connect to live business systems, send emails or WhatsApp messages, read or update Google Sheets, or execute exported workflows.

## Live demo

- **Website:** https://christian-tiaan.github.io/Synvoraith-AI-Labs-demo/
- **Workflow builder:** https://christian-tiaan.github.io/Synvoraith-AI-Labs-demo/flow.html
- **GitHub repository:** https://github.com/christian-tiaan/Synvoraith-AI-Labs-demo
- **Synvoraith AI on LinkedIn:** https://www.linkedin.com/company/synvoraith-ai/

If the live demo is unavailable, check that GitHub Pages is enabled for the repository's `main` branch.

## What is included?

### 1. Synvoraith AI Labs website

The landing page introduces the lab, its areas of exploration, development approach, example project directions, and the interactive Flow demo.

Website sections include:

- **About:** the lab's purpose and approach to practical experimentation.
- **Capabilities:** machine learning, computer vision, conversational AI, intelligent automation, data and evaluation, and responsible AI.
- **Process:** Discover → Prepare data → Build models → Test and validate → Deploy and learn.
- **Project directions:** examples of possible AI and automation projects.
- **Live demo:** an embedded view of Synvoraith Flow, with a link to open it separately.
- **Contact:** a link to the Synvoraith AI LinkedIn page.

### 2. Synvoraith Flow — visual workflow builder

Synvoraith Flow is an interactive, browser-based prototype for planning and visualising automation workflows.

**Current features**

- Add workflow nodes from a node palette.
- Move nodes around the canvas using drag interactions.
- Connect nodes by dragging from an output connector to another node.
- Select nodes and edit their names and configuration fields.
- Select and delete connections.
- Delete individual nodes.
- Run a visual simulation and view a step-by-step activity log.
- Identify nodes that are not connected to a starting node.
- Export the workflow as a simplified n8n-style JSON blueprint.
- Download the JSON export and attempt to copy it to the clipboard when browser permissions allow.
- Reset the canvas to the sample workflow.
- Save the current workflow in browser local storage so it can be restored in the same browser.

### Sample node types

| Node | Demonstration purpose |
|---|---|
| Schedule trigger | Starts a sample workflow on a schedule |
| Google Sheets | Represents reading lead rows |
| Filter | Represents filtering invalid or inactive leads |
| Split in batches | Represents releasing records in batches |
| Wait | Represents spacing actions over time |
| Send email | Represents a sample email step |
| Check replies | Represents checking for replies or bounces |
| Update sheet | Represents updating record status |
| Weekly report | Represents preparing a scheduled report |

The default canvas contains a sample outreach workflow with these nodes. Its run log uses illustrative messages and counts to demonstrate the flow; these are not results from real services.

### How to use Synvoraith Flow

1. Open the [Flow builder](https://christian-tiaan.github.io/Synvoraith-AI-Labs-demo/flow.html).
2. Change the workflow name in the top bar.
3. Add nodes from the palette, or edit the sample nodes already on the canvas.
4. Drag nodes to arrange the workflow.
5. Connect the output dot on one node to the target node.
6. Select a node to edit its name and available settings.
7. Select a connection and delete it if needed.
8. Choose **Run workflow** to view the simulated execution log.
9. Choose **Export JSON** to generate and download a simplified n8n-style blueprint.
10. Use **Reset** to restore the sample outreach workflow.

**Important export limitation:** the JSON is a starting blueprint, not a ready-to-run n8n workflow. Node types and parameters are simplified; credentials, service connections, valid platform-specific node settings, and production logic must be configured separately in the target automation platform.

## AI and technology areas explored

The lab's website presents these research and prototype directions:

- **Machine learning:** data-driven prediction, classification, model evaluation, and improvement.
- **Computer vision:** image analysis, object detection, and OCR.
- **Conversational AI:** chatbots, intelligent assistants, FAQs, and natural-language interfaces.
- **Intelligent automation:** workflow design, task automation, and software integrations.
- **Data and evaluation:** data preparation, experiment tracking, test cases, and performance measurement.
- **Responsible AI:** privacy-aware design, human oversight, security considerations, and transparent limitations.

These are areas of exploration and example directions, not a claim that every capability is currently delivered as a production service.

## Example project directions shown on the website

- **OpenCV face recognition prototype:** a computer-vision learning direction. Any real-world use of face data should be designed around consent, privacy, security, and applicable law.
- **WhatsApp workflow automation:** a concept for routing enquiries, answering common questions, and handing conversations to a person when appropriate.
- **AI assistant experiments:** conversational prototypes for finding information and supporting routine tasks.
- **Model evaluation dashboard:** a possible interface for reviewing experiment results, metrics, test cases, and improvements.
- **Synvoraith Flow:** the interactive workflow-planning and simulation prototype included in this repository.

Project directions should be treated as concepts or experiments unless a working implementation is explicitly identified.

## Technology

The current repository is a lightweight front-end project built with:

- HTML5 for page structure.
- CSS3 for layout, styling, responsive behaviour, and theme-aware presentation.
- Vanilla JavaScript for workflow interactions and browser-side simulation.
- Browser local storage for saving the Flow editor state locally.
- SVG for drawing workflow connections.
- Browser Blob and download APIs for exporting the JSON blueprint.

There is no application framework or package installation required for the current static demo.

## Repository structure

```text
Synvoraith-AI-Labs-demo/
├── index.html                 # Main Synvoraith AI Labs landing page
├── flow.html                  # Interactive Synvoraith Flow builder
├── README.md                  # Project overview and documentation
└── assets/
    ├── ai-labs-banner.png     # AI Labs banner artwork
    ├── synvoraith-ai-labs-logo.png
    ├── synvoraith-logo.png
    ├── synvoraith-symbol.png
    └── view                    # Existing repository asset
```

## Run locally

Because this is a static website, you can open `index.html` in a modern browser. For a local web server, run one of the following from the repository folder:

**Python**
```bash
python -m http.server 8000
```

Then visit:

- http://localhost:8000/
- http://localhost:8000/flow.html

## Deployment

The project can be hosted as a static site using GitHub Pages:

1. Open the repository's **Settings → Pages**.
2. Select **Deploy from a branch**.
3. Choose the `main` branch and the root folder (`/ `).
4. Save the settings and wait for the deployment to complete.

The public URL is normally:

`https://christian-tiaan.github.io/Synvoraith-AI-Labs-demo/`

## Current limitations

- The workflow execution is simulated in the browser; it does not perform real-world actions.
- Sample Google Sheets, email, reply-checking, and reporting nodes are illustrative only.
- No live API integrations, authentication, backend, or external service credentials are included.
- Exported JSON is a simplified n8n-style representation and requires adaptation before use in an automation platform.
- Workflow data is stored in the current browser's local storage; it is not synchronised across devices or users.
- The prototype is intended for exploration, demonstration, and workflow planning—not production operations.

## Responsible development

Synvoraith AI Labs aims to explore useful AI while communicating capabilities and limitations clearly. Any future implementation involving personal data, face recognition, customer conversations, or automated outreach should include appropriate consent, privacy safeguards, security controls, human oversight, testing, and compliance with applicable requirements.

## Roadmap ideas

Potential future improvements—not yet promised or implemented—include:

- More node types and configurable workflow templates.
- Improved validation for missing or disconnected workflow steps.
- Importing previously exported workflow blueprints.
- More complete n8n-compatible export mapping.
- Optional backend integrations with secure credential handling.
- Workflow versioning, sharing, and collaboration.
- Expanded testing, accessibility, and mobile canvas interactions.

## About Synvoraith AI Labs

Synvoraith AI Labs explores emerging technologies and develops practical prototypes across AI, machine learning, computer vision, conversational AI, and intelligent automation. The goal is to turn useful ideas into understandable experiments and, where appropriate, reliable solutions.

**Synvoraith AI Labs — Research. Build. Innovate. Scale.**

Connect with us on [LinkedIn](https://www.linkedin.com/company/synvoraith-ai/).
