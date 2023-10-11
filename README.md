# We Sale

Back in the day we have built a WeSale, voice and text recognition tool for sellers and marketers to evalute the quality of conversation.

When building the product, there were none well supported and "battle-tested" NLP tools and models.
DialogFlow was supporting only the engilish language, so after a few years things have changed.
There is a lot of different tools and models now, so we can use for it to support our clients with enormous accuracy.

## Idea

1. Allow companies to create discussions' scenarios for sellers/marketers etc.
2. Process what does seller says with omitting the input of their client to avoid the issue of recording someone who does not want to be recorded.
3. Since we are processing any input it can be either a text or a voice (that is in the end transformed to text).

This gives us a huge flexibility:
1. We can process any texts and voice
    - MVP will consist of text processing only to simplify
    - Voice processing will be a v2, since transforming Voice to Text is already a technical curve to tackle

2. It can be used in various scenarios (text)
    - emails (cold mailing, targetted mails etc.)
    - posts (blogs, social media etc.)
    - chatbots (to help AI tools to be more precised with communication with a human)
    - chats (were a human is on the "other side")

3. Voice
    - direct sellers
    - phone calls (call centers etc.)

## Product

### V1

1. NLP Models
    - for text processing

2. API
    - for storing company's scenarios in the Database
    - for traning models based on scenarios
    - for monitoring the accuracy of conversations and the benefits from using WeSale
    - for managing company's employees accounts and seeing their individual statistics

### Next steps

3. Frontend (PWA)
    - act as an employee
    - evaluate discussions in live using chatbot (to be extended to voice recognition tool in the future)

4. Frontend (Browser Plugin)
    - act as an employee
    - evaluate emails, posts etc

## Technical Decisions

1. Python for AI
2. TypeScript for Frontend and Backend
3. Using Node.js as major JavaScript runtime
    - Bun comes into consideration due to being v1.0.0 recently, but it still does not support such a features like WebSockets, Performance Observers etc. so it does not make sense to use it now
    - Deno is not that interesting, since it's native frameworks are not so pleasnt and they have rather a small community, Node frameworks sadly have huge performance drawbacks in some cases
4. Using v20 of Node.js
    - instead of LTS because that's a greenfield
5. Using Svetle Kit for frontend
    - as SPA with possiblity to extend that to PWA in the future
6. Before the offical release testing on premise
    - Cloud -> TBD, most probably GCP or Digital Ocean

#### AI

1. Use Python 3.12
    - pandas
    - keras

#### Backend

1. Use TypeScript 5.2
    - Fastify@latest
    - Node v20

#### Frontend

1. Use TypeScript 5.2
    - Svetle Kit@latest
    - Vite@latest
    - Node v20
    - SPA
    - PWA (not as MVP)

#### Package Managers

1. Due to Bun not being battle-tested and without support for WebSockets we have to leave with Node.js package mangers
2. Since we need to live without Bun the choice is PNPM due to its great performance and support


#### Continues Integration

1. Use CircleCI due to its maturity and great support

#### Monorepo package manager

1. Turborepo due to its support to the CircleCI, rising community and great performance

#### Hosting

1. Before the official release it will be hosted on premise
2. Then maybe moved to cloud like GCP or even Digital Ocean due to costs reasons


## Maintenance Decisions

1. To deliver the MVP faster let's make a monorepo
    - in the future it can make sense to separate Python code from the rest
2. All the JS packages should be inside workspaces


## Root Folder Structure

    .
    ├── ci                      # Continues Integration settings
    ├── docs                    # Unrelated project documentation
    ├── modules                 # Source Code
    ├── scripts                 # Scripts for local environment
    └── README.md
