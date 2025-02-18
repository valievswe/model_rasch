# Rasch model calculator Telegram bot

This guide will help you set up and run the Telegram bot from this repository.

## Prerequisites

Before you start, ensure you have the following installed:

- [Node.js](https://nodejs.org/) (Latest LTS version recommended)
- [npm](https://www.npmjs.com/) (comes with Node.js)

## Installation

1. **Clone the Repository**

   ```sh
   git clone https://github.com/valievswe/model_rasch.git
   cd rasch
   ```

2. **Install Dependencies**

   ```sh
   npm install
   ```

3. **Set Up Telegram Bot Token**

   - Create a bot using [@BotFather](https://t.me/botfather) on Telegram.
   - Obtain the bot token from BotFather.
   - Create a `.env` file in the project root and add the token.
   - Optional: you can connect PostgreSQL db with prisma:
     ```sh
     BOT_TOKEN=your_bot_token_here
     DB_URL = YOUR_DB_URL
     ```

4. **Run the Bot**
   ```sh
   node server.js
   ```

## Usage

- Start the bot in Telegram by sending `/start`.
- Send the xls, xlsx or csv file which contains a matrix of student-question-answer relation. 0 means incorrect, 1 means correct answer
  ![dummy-data](./images/dummy_data.png)
- You'll get result.xls as a response
  ![result](./images/result.png)

## Troubleshooting

- Ensure your bot token is correct.
- Check if all required dependencies are installed (`npm install`).
- Verify that Node.js is properly installed (`node -v`).
