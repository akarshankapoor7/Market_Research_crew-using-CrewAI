# MarketResearchCrew Crew

This project implements a sophisticated multi-agent AI system using CrewAI to automate end-to-end market research and business analysis. It orchestrates five specialized agents—ranging from Market Research and Competitive Intelligence to Product Strategy—that collaborate sequentially to transform raw product ideas into comprehensive investment-ready memos. Leveraging advanced tools for web searching and scraping, the crew delivers data-backed insights on market sizing, customer personas, and technical feasibility. The final output is a professional Markdown report detailing pricing strategies, revenue models, and a definitive go/no-go recommendation for AI product concepts.

## Installation

Ensure you have Python >=3.10 <3.14 installed on your system. This project uses [UV](https://docs.astral.sh/uv/) for dependency management and package handling, offering a seamless setup and execution experience.

First, if you haven't already, install uv:

```bash
pip install uv
```

Next, navigate to your project directory and install the dependencies:

(Optional) Lock the dependencies and install them by using the CLI command:
```bash
crewai install
```
### Customizing

**Add your `OPENAI_API_KEY/GROQ_API_KEY` into the `.env` file**

- Modify `src/market_research_crew/config/agents.yaml` to define your agents
- Modify `src/market_research_crew/config/tasks.yaml` to define your tasks
- Modify `src/market_research_crew/crew.py` to add your own logic, tools and specific args
- Modify `src/market_research_crew/main.py` to add custom inputs for your agents and tasks

## Running the Project

To kickstart your crew of AI agents and begin task execution, run this from the root folder of your project:

```bash
$ crewai run
```

This command initializes the market_research_crew Crew, assembling the agents and assigning them tasks as defined in your configuration.

This example, unmodified, will run the create a `report.md` file with the output of a research on LLMs in the root folder.

# Understanding Your Crew

The MarketResearchCrew is a sophisticated multi-agent system where five specialized AI entities collaborate to transform a product idea into a validated business strategy:

Market Research Specialist: Performs the initial deep dive into market sizing (TAM/SAM/SOM), growth drivers, and regulatory landscapes.

Competitive Intelligence Analyst: Conducts a 360-degree audit of the competition, mapping out their strengths, pricing models, and market positioning to find strategic gaps.

Customer Insights Researcher: Builds detailed user personas and journey maps by analyzing real-world pain points and customer behaviors.

Product Strategy Advisor: Synthesizes research into a concrete product roadmap, prioritizing MVP features and assessing technical feasibility.

Business Analyst: Acts as the final synthesizer, providing a professional investment-grade report with pricing models, risk matrices, and a final Go/No-Go recommendation.

These agents operate sequentially as defined in crew.py, passing context from one task to the next to ensure the final report is grounded in cohesive, data-driven insights. Your agent configurations are managed in config/agents.yaml, while the specific research objectives and expected outputs are detailed in config/tasks.yaml.

# Additional Tools Used

The MarketResearchCrew leverages a suite of specialized tools to ensure agents have access to real-time, high-fidelity data from the web:

SerperDevTool: A powerful Google Search API used by the agents to conduct broad market research, track industry trends, and identify competitors across the live web.

ScrapeWebsiteTool: Enables agents to extract structured information directly from specific URLs, such as competitor landing pages or industry news articles.

SeleniumScrapingTool: Provides advanced browser-based scraping capabilities, allowing agents to navigate and extract data from complex, JavaScript-heavy websites that standard scrapers might miss.

Configuration
These tools are initialized within crew.py and bundled into a toolkit that is assigned to the specialized agents. This setup ensures that your Market Research Specialist and Competitive Intelligence Analyst have the "eyes" needed to find the most current data-backed insights.

## Support

For support, questions, or feedback regarding the MarketResearchCrew Crew or crewAI.
- Visit our [documentation](https://docs.crewai.com)
- Reach out to us through our [GitHub repository](https://github.com/joaomdmoura/crewai)
- [Join our Discord](https://discord.com/invite/X4JWnZnxPb)
- [Chat with our docs](https://chatg.pt/DWjSBZn)

Let's create wonders together with the power and simplicity of crewAI.
