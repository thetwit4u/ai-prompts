# AI-Driven Development Workflow
## Overview
This folder includes prompts that should be copy/pasted into your project's ai-docs/commands folder. You can then use them by tagging them in the chat (e.g. @plan_feature.md) and providing the necessary context.
Feel free to customize them to your needs! These are a starting point for a powerful, structured AI-assisted development process.

## The Workflow
This set of commands is designed to be used in a logical sequence to take a project from an idea to fully documented code.
 * @create_brief.md: Start here. Establish the high-level vision, target audience, and core purpose of the project.
 * @project_plan.md: Use the brief and raw requirements to create a strategic project plan. This breaks the project into epics, phases, and dependencies.
 * @plan_feature.md: For each feature identified in the project plan, generate a detailed technical implementation plan.
 * @code_review.md: After implementing a feature, use its plan to have the AI perform a thorough code review.
 * @write_docs.md: Once a feature is complete and reviewed, generate comprehensive documentation.

## Command Examples

1. Create Brief
Used for establishing the bigger picture context of what this project is about. This is the first step.
@create_brief.md 

We are building an application to help dungeon masters plan their D&D campaigns and it's going to be called Dragonroll. It will include a variety of different tools, such as a random map generator, NPC generator, and loot generator. We will use AI to allow the dungeon master to input certain prompts or use the tools directly.

2. Create Project Plan
Used to create a high-level strategic project plan. It breaks down the project from the brief into epics, phases, and dependencies, setting the stage for detailed feature planning.
@project_plan.md
@PRODUCT_BRIEF.md

Here are the raw requirements for Dragonroll:
The application must allow a Dungeon Master (DM) to create and manage multiple campaigns. Within a campaign, the DM needs several AI-powered generator tools:
- An NPC generator for creating non-player characters with names, backstories, and images.
- A random map generator for creating dungeons or world maps based on prompts.
- A loot generator to create treasure tables and magic items.
- A session manager to write notes, track initiative, and manage player stats during a game.
Users must be able to register and log in to save their work.

3. Plan Feature
Used to create a detailed technical plan for a single new feature identified in the Project Plan. Focuses on the technical requirements, not product-level context.
@plan_feature.md 

Based on F-02 from the project plan, we want to add the NPC generator page. To implement this, we will use the OpenAI API to generate the NPC's name and description. We'll also generate a portrait for the NPC using the DALL-E 3 model. The page should have a single button "Generate NPC" and display the resulting name, description, and image.

4. Code Review
Used to review the successful completion of a plan in a separate chat.
@code_review.md
@0001_PLAN.md

5. Documentation Writing
Used to create comprehensive documentation for the plan, review, and implementation.
@write_docs.md
@0001_PLAN.md
@0001_REVIEW.md

