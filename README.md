E-Commerce Chatbot: Project Summary
Introduction
A new conversational chatbot feature was developed for a white-label e-commerce platform through a collaborative hackfest. The chatbot, built in TypeScript using the Node.js Bot Framework SDK, offers features like order tracking, product browsing with natural language filtering, shopping cart management, FAQ search, and blog post search. It supports localization (e.g., English, Slovak) and is accessible via Facebook Messenger and an embedded website chat using Direct Line.

Development Process
1. Backend API Preparation
The e-commerce platform was originally a Django MVC web application without API services. REST APIs were developed to integrate the chatbot.

2. Bot Integration with APIs
The bot consumes e-commerce services (e.g., product search, cart management, FAQs) and displays content through rich cards and adaptive cards.

3. Authentication
Messenger: Implemented using OAuth and Messenger's account linking feature.
Direct Line: Token passed via parameters when embedding the chat window.
4. Proactive Messaging
The bot sends proactive messages (e.g., "full cart, no order" notifications) on Messenger, enabling up-selling opportunities.

5. Command Recognizers
The bot supports custom command recognition via action buttons and regular expressions, limiting user freedom to enhance experience.

6. Localization
Supports Slovak and English, with future plans for expansion to other languages.

7. Product Filtering with Natural Language
Instead of using LUIS (limited language support), Elastic Search and regex-based rules were implemented for advanced filtering.

8. Monitoring
Application Insights tracks usage and logs errors to refine performance.

Challenges and Learnings
Platform Limitations:

Messenger restricts adaptive card functionality and quick reply redirects.
HTTPS was mandatory for development, requiring tools like ngrok.
Localization Issues:

LUIS lacks Slovak support; translations via Bing Translate were imprecise.
Elastic Search provided a viable alternative for NLP.
Bot Publication:

Facebook's approval process requires meticulous setup and compliance.
Future Plans
Add shopping and payment functionality (pending regulatory clarification).
Extend NLP capabilities if LUIS supports additional languages.
Migrate session storage to Azure's Redis Cache post-Bot Framework updates.
Impact
The chatbot was successfully implemented and onboarded its first customer. It serves as a unique feature, distinguishing the e-commerce solution in a competitive market while providing automated support and new customer engagement channels.
This is only for educational achievements not for punlic outreach or use.
