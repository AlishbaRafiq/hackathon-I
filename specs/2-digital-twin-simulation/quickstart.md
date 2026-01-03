# Quickstart Guide: Digital Twin Simulation Module

**Date**: 2026-01-02

## Adding Module 2 to Docusaurus Project

### Prerequisites
- Access to the existing Docusaurus project in `book_frontend/` directory
- Node.js and npm for local development
- Git for version control

### Module Structure Creation

1. **Create module directory in docs/**:
   ```bash
   mkdir -p book_frontend/docs/module2-digital-twin
   ```

2. **Create initial content files**:
   ```bash
   touch book_frontend/docs/module2-digital-twin/index.md
   touch book_frontend/docs/module2-digital-twin/physics-simulation.md
   touch book_frontend/docs/module2-digital-twin/sensor-simulation.md
   touch book_frontend/docs/module2-digital-twin/unity-interaction.md
   ```

### Configuring Navigation

1. **Update `sidebars.js`** to include Module 2:
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
         label: 'Module 2: The Digital Twin (Gazebo & Unity)',
         items: [
           'module2-digital-twin/index',
           'module2-digital-twin/physics-simulation',
           'module2-digital-twin/sensor-simulation',
           'module2-digital-twin/unity-interaction',
         ],
       },
       {
         type: 'category',
         label: 'Module 3: Python Agents with ROS 2',
         items: [
           'module2-python-ros/index',
           'module2-python-ros/rclpy-nodes',
           'module2-python-ros/ai-integration',
         ],
       },
       {
         type: 'category',
         label: 'Module 4: Humanoid Modeling with URDF',
         items: [
           'module3-urdf-humanoids/index',
           'module3-urdf-humanoids/links-joints-frames',
           'module3-urdf-humanoids/sensors-simulation',
         ],
       },
     ],
   };
   ```

2. **Verify the existing structure** to ensure Module 2 is properly integrated with the existing modules.

### Writing Content

1. **Markdown syntax for documentation**:
   - Use standard markdown for text
   - Add code blocks with syntax highlighting: ` ```xml ` for XML, ` ```bash ` for bash commands
   - Use admonitions for important notes: ` :::note`, ` :::tip`, ` :::caution`

2. **Example content structure**:
   ```markdown
   ---
   sidebar_position: 1
   title: Module 2 - The Digital Twin (Gazebo & Unity)
   description: Understanding digital twins using Gazebo and Unity for humanoid robot simulation
   keywords: [gazebo, unity, simulation, digital twin, robotics]
   authors: [AI and Robotics Education Team]
   last_updated: 2026-01-02
   tags: [simulation, digital-twin, gazebo, unity]
   ---

   # Module 2: The Digital Twin (Gazebo & Unity)

   This module covers digital twin technology using Gazebo and Unity for humanoid robot simulation...

   ## Learning Objectives

   By the end of this module, you will be able to:
   - Explain digital twin concepts in robotics
   - Create physics simulations with Gazebo
   - Configure sensors in simulation environments
   - Understand Unity's role in high-fidelity visualization
   ```

### Content Organization

1. **Chapter 1: Physics Simulation with Gazebo**
   - Focus on gravity, collisions, and dynamics
   - Include examples of simulating humanoid movement
   - Cover Gazebo world files and model integration

2. **Chapter 2: Sensors in Simulation**
   - Cover LiDAR, depth cameras, and IMUs
   - Explain sensor data flow into ROS 2
   - Include practical examples and configurations

3. **Chapter 3: High-Fidelity Interaction with Unity**
   - Focus on visual realism and human-robot interaction
   - Explain when to use Unity alongside Gazebo
   - Cover Unity-ROS integration approaches

## Local Development

### Starting the Development Server
- Navigate to the `book_frontend` directory
- Run `npm run start` to start the development server
- Navigate to http://localhost:3000 to view your site
- Changes to content will be reflected automatically