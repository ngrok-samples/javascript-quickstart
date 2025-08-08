# ngrok JavaScript SDK Quickstart

A minimal Node.js app demonstrating the ngrok JavaScript SDK.

## What you'll need

- An [ngrok account](https://dashboard.ngrok.com/signup).
- Your [ngrok auth token](https://dashboard.ngrok.com/get-started/your-authtoken).
- [Node.js installed](https://nodejs.org/en/download/) on your machine.

## Setup

1. Install dependencies:
   ```bash
   npm install
   ```

2. Create a `.env` file from the example:
   ```bash
   cp .env.example .env
   ```

3. Add your ngrok auth token to the `.env` file:
   ```txt
   NGROK_AUTHTOKEN=your_actual_authtoken_here
   ```

4. (Optional) Reserve a domain in the [ngrok dashboard](https://dashboard.ngrok.com/domains) and update the `domain` field in `example.js`.

## Running the app

1. Start the Node.js service:
   ```bash
   npm start
   ```

2. In another terminal, start the ngrok agent endpoint:
   ```bash
   npm run ngrok
   ```

The ngrok agent endpoint will output a URL that forwards traffic to your local app. If you configured OAuth, visitors will need to log in with Google to access it.

## Files

- `service.js` - Basic Node.js HTTP server
- `example.js` - ngrok agent endpoint configuration with OAuth
- `.env.example` - Environment variable template
