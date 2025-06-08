# PearlThoughts-code-

EmailService

#  Resilient Email Sending Service

This project implements a robust and fault-tolerant email sending service using JavaScript. It supports retry logic, fallback email providers, rate limiting, idempotency, status tracking, and includes unit tests.

---

## Features

-  **Retry Mechanism** – Automatically retries email sending with exponential backoff if a provider fails.
-  **Fallback Providers** – Switches to another provider if the first one fails.
-  **Idempotency** – Prevents duplicate emails using unique `emailId`.
-  **Rate Limiting** – Controls how often emails are sent to avoid spamming.
-  **Status Tracking** – Tracks the status of each email (`sent`, `queued`, `failed`).
-  **Unit Tests** – Uses Jest to test key functionality.

---

## Project Structure Explained

### `EmailService.js`
Main service logic: handles sending, retry, fallback, idempotency, and tracking.

### `MockProviderA.js` & `MockProviderB.js`
Fake providers used to simulate email sending with random failures/successes.

### `StatusTracker.js`
Stores and retrieves the status of each email by `emailId`.

### `__tests__/EmailService.test.js`
Test file for verifying that the service sends emails, blocks duplicates, and tracks status properly.

### `package.json`
Contains project metadata, dependencies, and scripts. Run `npm install` to install and `npm test` to run tests.


Technologies Used:

JavaScript (ES6)

Node.js

Jest (for unit testing)
