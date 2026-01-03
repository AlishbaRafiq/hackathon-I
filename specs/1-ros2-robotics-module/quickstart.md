# Quickstart Guide: ROS 2 Educational Module

**Date**: 2026-01-02

## Setting Up the Docusaurus Project

### Prerequisites
- Node.js (LTS version recommended)
- npm or yarn package manager
- Git for version control

### Installation Steps

1. **Install Docusaurus globally**:
   ```bash
   npm install -g @docusaurus/init
   ```

2. **Create a new Docusaurus project**:
   ```bash
   npx create-docusaurus@latest docusaurus-project classic
   cd docusaurus-project
   ```

3. **Start the development server**:
   ```bash
   npm run start
   ```

4. **Project structure**:
   After installation, your project will have the following structure:
   ```
   docusaurus-project/
   ├── blog/          # Blog posts (optional)
   ├── docs/          # Documentation files
   ├── src/
   │   ├── components/ # React components
   │   ├── pages/     # Static pages
   │   └── css/       # Custom CSS
   ├── static/        # Static assets
   ├── docusaurus.config.js  # Site configuration
   ├── sidebars.js    # Sidebar navigation
   └── package.json   # Dependencies
   ```

## Adding ROS 2 Educational Content

### Creating the Module Structure

1. **Create module directories in docs/**:
   ```bash
   mkdir -p docs/module1-ros2-basics
   mkdir -p docs/module2-python-ros
   mkdir -p docs/module3-urdf-humanoids
   ```

2. **Create initial content files**:
   ```bash
   touch docs/module1-ros2-basics/index.md
   touch docs/module1-ros2-basics/concepts.md
   touch docs/module1-ros2-basics/middleware.md
   touch docs/module2-python-ros/index.md
   touch docs/module2-python-ros/rclpy-nodes.md
   touch docs/module2-python-ros/ai-integration.md
   touch docs/module3-urdf-humanoids/index.md
   touch docs/module3-urdf-humanoids/links-joints-frames.md
   touch docs/module3-urdf-humanoids/sensors-simulation.md
   ```

### Configuring Navigation

1. **Update `sidebars.js`** to include your modules:
   ```javascript
   module.exports = {
     tutorialSidebar: [
       'intro',
       {
         type: 'category',
         label: 'Module 1: ROS 2 Fundamentals for Physical AI',
         items: [
           'module1-ros2-basics/index',
           'module1-ros2-basics/concepts',
           'module1-ros2-basics/middleware',
         ],
       },
       {
         type: 'category',
         label: 'Module 2: Python Agents with ROS 2',
         items: [
           'module2-python-ros/index',
           'module2-python-ros/rclpy-nodes',
           'module2-python-ros/ai-integration',
         ],
       },
       {
         type: 'category',
         label: 'Module 3: Humanoid Modeling with URDF',
         items: [
           'module3-urdf-humanoids/index',
           'module3-urdf-humanoids/links-joints-frames',
           'module3-urdf-humanoids/sensors-simulation',
         ],
       },
     ],
   };
   ```

2. **Update `docusaurus.config.js`** with site metadata:
   ```javascript
   const config = {
     title: 'ROS 2 for AI and Robotics Students',
     tagline: 'Learn ROS 2 as the robotic nervous system for humanoid robots',
     url: 'https://your-username.github.io',
     baseUrl: '/ros2-robotics-module/',
     onBrokenLinks: 'throw',
     onBrokenMarkdownLinks: 'warn',
     favicon: 'img/favicon.ico',
     organizationName: 'your-username',
     projectName: 'ros2-robotics-module',
     deploymentBranch: 'gh-pages',
     trailingSlash: false,
     // ... rest of configuration
   };
   ```

### Writing Content

1. **Markdown syntax for documentation**:
   - Use standard markdown for text
   - Add code blocks with syntax highlighting: ` ```python ` for Python code
   - Use admonitions for important notes: ` :::note`, ` :::tip`, ` :::caution`

2. **Example content structure**:
   ```markdown
   ---
   sidebar_position: 1
   ---

   # Module 1: ROS 2 Fundamentals for Physical AI

   This module introduces the core concepts of ROS 2 as middleware for humanoid robots.

   ## Learning Objectives

   By the end of this module, you will be able to:
   - Explain the role of ROS 2 in embodied intelligence
   - Identify the four main communication patterns in ROS 2
   - Describe how ROS 2 serves as middleware for humanoid robots

   ## What is ROS 2?

   ROS 2 (Robot Operating System 2) is not an operating system but rather a middleware framework...
   ```

## Building and Deployment

### Local Development
- Run `npm run start` to start the development server
- Navigate to http://localhost:3000 to view your site
- Changes to content will be reflected automatically

### Building for Production
- Run `npm run build` to create a static build
- The build output will be in the `build/` directory

### Deploying to GitHub Pages
- Run `npm run deploy` to deploy to GitHub Pages
- This command will push the built site to the `gh-pages` branch