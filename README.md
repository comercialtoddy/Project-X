<div align="center">

# Leaker Flow

*Much more than a social network — it's a community for Grand Theft Auto VI players and content creators.*

![Leaker Flow Screenshot](./banner.png)

Leaker Flow is the ultimate open-source community platform for Grand Theft Auto VI enthusiasts. Through our interactive hub, Leaker Flow connects players and content creators, providing tools for collaboration, research, and sharing. It's your digital companion for navigating the world of GTA VI, combining powerful community features with an intuitive interface that understands what you need and helps you connect with others.

Leaker Flow's toolkit includes seamless integration with gaming news sources, community forums, and social media to bring you the latest information. It features robust user profiles, crew management tools, event planning capabilities, and a platform for sharing user-generated content like guides, screenshots, and videos. These features work together harmoniously, allowing you to enhance your gaming experience and engage with the community through a single, unified platform.

[![License](https://img.shields.io/badge/License-Apache--2.0-blue)](./license)
[![Discord Follow](https://dcbadge.limes.pink/api/server/Py6pCBUUPw?style=flat)](https://discord.gg/leakerflow)
[![Twitter Follow](https://img.shields.io/twitter/follow/leakerflow)](https://x.com/leakerflow)
[![GitHub Repo stars](https://img.shields.io/github/stars/leaker-flow/leakerflow)](https://github.com/leaker-flow/leakerflow)
[![Issues](https://img.shields.io/github/issues/leaker-flow/leakerflow)](https://github.com/leaker-flow/leakerflow/labels/bug)

</div>

## Table of Contents

- [Project Architecture](#project-architecture)
  - [Backend API](#backend-api)
  - [Frontend](#frontend)
  - [Agent Docker](#agent-docker)
  - [Supabase Database](#supabase-database)
- [Use Cases](#use-cases)
- [Self-Hosting](#self-hosting)
- [Acknowledgements](#acknowledgements)
- [License](#license)

## Project Architecture

![Architecture Diagram](./docs/images/diagram.png)

Leaker Flow consists of four main components:

### Backend API

A Python/FastAPI service that handles REST endpoints, user interactions, real-time notifications, and content management.

### Frontend

A Next.js/React application providing a responsive UI with a community feed, user profiles, crew pages, event calendars, and content creation tools.

### Agent Docker

An isolated execution environment for community-focused tasks, such as scraping the latest game news, analyzing in-game trends, moderating content, and powering interactive community bots.

### Supabase Database

Handles data persistence with authentication, user management, profiles, posts, comments, crew information, and real-time subscriptions for a live community experience.

## Use Cases

1.  **Get the Latest News & Leaks** - _"Show me the latest verified leaks and news about GTA VI from the last 24 hours. Filter out rumors and include sources from top gaming journals and insider forums."_

2.  **Find Your Crew** - _"I'm looking for a role-playing crew that is active in the evenings (EU time). They should be focused on cooperative missions rather than PvP. Show me the top 3 crews and their recruitment status."_

3.  **Plan a Community Event** - _"Create a community event for a cross-platform car meet. The event should be scheduled for next Saturday at 8:00 PM UTC. Generate an invite link and post it in the main community channel."_

4.  **Discover Content Ideas** - _"I'm a streamer looking for new content ideas for GTA VI. Analyze the most popular community topics this week and suggest three unique video ideas, complete with titles and descriptions."_

5.  **Track In-Game Assets** - _"Notify me when the Ocelot Virtue car is available for purchase or has been spotted in a specific location by other players. Provide the server and location details."_

6.  **Generate a Mission Guide** - _"Create a step-by-step guide for the 'Heist of the Century' mission, including optimal loadouts, crew roles, and strategies submitted by top players in the community."_

7.  **Analyze Player Statistics** - _"Compare my mission completion times and accuracy stats with the community average. Identify my top 3 strongest skills and suggest areas for improvement."_

8.  **Find Custom Lobbies** - _"Search for open custom race lobbies that are happening right now. Filter for non-contact races with at least 10 participants and display the host's username and lobby name."_

## Self-Hosting

Leaker Flow can be self-hosted on your own infrastructure using our setup wizard. For a comprehensive guide to self-hosting, please refer to our [Self-Hosting Guide](./docs/SELF-HOSTING.md).

The setup process includes:

-   Setting up a Supabase project for database and authentication
-   Configuring Redis for caching and session management
-   Setting up Daytona for secure agent execution
-   Integrating with LLM providers (Anthropic, OpenAI, Groq, etc.) for AI-powered features
-   Configuring web search and scraping capabilities

### Quick Start

1.  **Clone the repository**:

    ```bash
    git clone https://github.com/leaker-flow/leakerflow.git
    cd leakerflow
    ```

2.  **Run the setup wizard**:

    ```bash
    python setup.py
    ```

3.  **Start or stop the containers**:

    ```bash
    python start.py
    ```

### Manual Setup

See the [Self-Hosting Guide](./docs/SELF-HOSTING.md) for detailed manual setup instructions.

The wizard will guide you through all necessary steps to get your Leaker Flow instance up and running. For detailed instructions, troubleshooting tips, and advanced configuration options, see the [Self-Hosting Guide](./SELF-HOSTING.md).

## Contributing

We welcome contributions from the community! Please see our [Contributing Guide](./CONTRIBUTING.md) for more details.

## Acknowledgements

### Technologies

Leaker Flow is built on the shoulders of giants. We would like to thank the developers behind these amazing open-source projects and services:

-   [Daytona](https://daytona.io/) - Secure agent execution environment
-   [Supabase](https://supabase.com/) - Database and authentication
-   [Playwright](https://playwright.dev/) - Browser automation
-   [OpenAI](https://openai.com/) - LLM provider
-   [Anthropic](https://www.anthropic.com/) - LLM provider
-   [Tavily](https://tavily.com/) - Search capabilities
-   [Firecrawl](https://firecrawl.dev/) - Web scraping capabilities

## License

Leaker Flow is licensed under the Apache License, Version 2.0. See [LICENSE](./LICENSE) for the full license text.
