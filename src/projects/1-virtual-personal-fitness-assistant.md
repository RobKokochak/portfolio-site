---
title: "AI Personal Fitness Assistant"
summary: "A React Native app utilizing ChatGPT to provide a conversational interface to set, update and schedule fitness and nutrition goals."
image: /images/fitness-assistant-screenshots.png
imageAlt: "Screenshot of Virtual Personal Fitness Assistant"
tech:
  - "React Native"
  - "Typescript"
  - "Express"
siteUrl: "#"
repoUrl: "#"
---

## **Problem Statement**

Create a text-based chat AI interface for fitness and nutrition planning in React Native. 

It should be capable of maintaining user metrics and goals, scheduling meals and workouts, creating personalized workouts and nutrition plans, and providing tailored advice based on the needs of the user.

## **Technologies Used**

- **Frontend**: React Native, Typescript
- **Backend**: Express, Sequelize, MySQL
- **APIs**: OpenAI API 

## **Challenges Faced**
- **Prompt Engineering**

While anyone can send requests to an LLM and receive generalized answers, how do you make sure the response is strictly within scope? And more broadly, how do you integrate this powerful language recognition tool into the functionality and data of an application? 

Through development, we became very familiar with the intricacies of tailoring prompts, this being the main factor for ensuring the LLM understands the context of a user request and returns the desired response and format. 

Some of the biggest challenges included making sure the LLM did not fulfill user requests out of the scope of health & fitness (the LLM is programmed to please the user at all costs, so this was a challenge), along with guiding the LLM to make the correct decision on tricky edge cases such as categorization of events or metrics, which were key to our data-routing structure.

- **Data Routing**

 Once we had the prompt and the return-format in place, the question became what to do with the GPT response - how to turn that into the execution of a use case. 
 
 While OpenAI's function-calling feature had just been released, one of our requirements was that API calls must remain small and performant, and this feature required too much context to be passed to GPT. We chose to create a custom keyword-based structure, where GPT would return only the most important categorizing keywords of the user's request based on very specific instructions. These keywords then serve as the keys to a routing hierarchy, with the return value being a specific function for that combination of keywords, e.g. set/get/update metrics, events, goals, etc. 

## **Lessons Learned**

- **Managing Complexity: Efficiency in Data Routing and Promise Dependency**

In using GPT for both parameterizing user input and returning a conversational response, a single request could trigger multiple API calls, passing data through many different parts of the application code and database. Focusing on the principles of REST and keeping promise dependencies to a minimum was key to both keeping the API context small and the app performant.

- **Planning and Building a Full-Stack Application**

This project encompassed the full development lifecycle of planning, documenting, building, integrating, and testing. We learned about when and where certain technologies need to be put in place to enable others in the stack, the integration of frontend/backend/database, the importance of code maintainability, redundancy, UX, testing, and stakeholder interaction. 

