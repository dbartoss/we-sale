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

## Tools

1. Python for AI
2. TypeScript for Frontend and Backend
3. Using Bun as major JavaScript runtime
4. Before the offical release testing on premise
4. Cloud -> TBD, most probably GCP, Digital Ocean