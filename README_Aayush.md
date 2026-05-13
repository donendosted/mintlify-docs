📝 HydraDB Documentation Contribution Guide
This branch contains updates for the HydraDB documentation. Follow the steps below to set up your local environment and preview the changes before they are merged into main.

🛠 Prerequisites
Ensure you have the following installed on your machine:

Node.js: Use LTS Version 20 (Higher versions like 25+ are currently unsupported).

Package Manager: npm or yarn.

Git: To manage your local branch.

🚀 Local Preview Steps
1. Version Control & Setup
First, ensure you are on the correct branch and have your Node environment synced:

Bash
# Verify you are on the correct branch
git checkout <your-branch-name>

# Switch to Node 20 using NVM
nvm use 20

# Install dependencies
npm install
2. Install Mintlify CLI
If you haven't installed the Mintlify CLI globally for this Node version, run:

Bash
npm install -g mintlify
3. Start the Dev Server
Run the following command from the root of the repository:

Bash
mintlify dev
Once the server starts, open your browser to http://localhost:3000. The preview features hot-reloading, so your changes will update instantly as you save files.

🧼 Quality & Hygiene Checks
Before submitting your Pull Request, please run the hygiene check to ensure there are no broken links or configuration errors:

Bash
npm run hygiene
Note for macOS Users: If you encounter a sha256sum error, ensure you have coreutils installed via Homebrew and your PATH is updated.

🎨 Documentation Standards
Mermaid Diagrams
All diagrams should follow the HydraDB Dark Mode styling.

Primary Nodes: #1e293b (Slate Gray)

Core Innovation/Highlight: #4c1d95 (Hydra Purple)

Text: #f8fafc

Navigation
If you add new pages, ensure they are registered in the navigation array within docs.json. Use the format "folder/file-name" (without the .mdx extension).

📬 Review Process
Push your changes to your fork/branch.

Open a Pull Request against the main branch.

Wait for the Mintlify Bot to generate a deployment preview link in the PR comments for a final web-based check.