
 Azure AI Agent
 ---------------
 we showcase how to integrate a custom Azure AI Foundry Agent with Microsoft 365 Copilot using a modular and scalable architecture.
Instead of relying solely on Copilot’s out-of-the-box capabilities, We’re using a dedicated AI agent to ensure consistent and reliable answers, showcasing how this setup can be adapted for specific business scenarios later.
To make this possible, we combined:
•	Azure AI Foundry – to host the custom GPT-based agent(Host logic and memory)
•	Azure Function – to securely serve the agent as an API(act as api wrapper) This acts as the bridge between external services like Power Automate and our agent
•	Power Automate – to connect and orchestrate the flow between services(Passes user message to the function and return output)
•	Copilot Studio – to expose the experience to end users via conversational UI(Ui Interface) We used the Conversational Boosting feature to handle unrecognized questions, and redirected those to our Power Automate Flow
We walk through each component
Demo
Benefits:
•  Custom logic, we build programmable agent not declarative agent like co pilot
•  More control
•  Debug-friendly(via Flow + Function logs)
•  Modular and reusable( easily swap in other agents or APIs)
•  Copilot + GPT power combo(using GPT models under the hood)
Future Enhancements:
Thread handling
•  Message formatting/wrapping for user awareness(Powered by Foundry Agent or agent name)
•  Add APIM for central access control(Azure API Management)
Implement Event-Driven Triggers from Copilot or Teams Bot
To conclude
We chose this architecture because it gives us full control.
With Azure AI Foundry, we can build agents with domain-specific logic, plug in custom prompts, reuse them across apps — and not be limited by Copilot’s default behaviour. Instead of locking everything into one place, this setup gives you freedom, flexibility, and control — so you can plug your AI into any channel or upgrade parts anytime.
Any questions /suggestions.
You can freely explore Foundry, but you pay for what you use—compute, storage, and AI inference.
•  Deploying powerful models (e.g., GPT 4, xAI Grok) costs based on tokens processed and compute time.
•  Additional services like search, storage, and telemetry cost separately.
This Azure Function takes the user’s message, talks to the AI agent in Azure Foundry, gets a smart answer, and sends it back — acting like a translator between Copilot and our custom AI.”


