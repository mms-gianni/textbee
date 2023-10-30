# TextBee - Android SMS Gateway

A simple SMS gateway that allows users to send SMS messages from a web interface or
from their application via a REST API. It utilizes android phones as SMS gateways.

- **Technology stack**: React, Next.js, Node.js, NestJs, MongoDB, Android, Java
- **Status**: MVP in development, not ready for production use yet
- **Link**: [https://textbee.vernu.dev](https://textbee.vernu.dev/)

![](https://ik.imagekit.io/vernu/textbee/texbee-landing-light.png?updatedAt=1687076964687)

## Usage

1. Go to [textbee.vernu.dev](https://textbee.vernu.dev) and register or login with your account
2. Install the app on your android phone from [textbee.vernu.dev/android](https://textbee.vernu.dev/android)
3. Open the app and grant the permissions for SMS
4. Go to [textbee.vernu.dev/dashboard](https://textbee.vernu.dev/dashboard) and click register device/ generate API Key
5. Scan the QR code with the app or enter the API key manually
6. You are ready to send SMS messages from the dashboard or from your application via the REST API

**Code Snippet**: Few lines of code showing how to send an SMS message via the REST API

```javascript
const API_KEY = 'YOUR_API_KEY';
const DEVICE_ID = 'YOUR_DEVICE_ID';

await axios.post(`https://api.textbee.vernu.dev/api/v1/gateway/devices/${DEVICE_ID}/sendSMS?apiKey=${API_KEY}`, {
  receivers: [ '+251912345678' ],
  smsBody: 'Hello World!',
})

```

## Contributing

Contributions are welcome!

1. Fork the project.
2. Create a feature or bugfix branch from `main` branch.
3. Make sure your commit messages and PR comment summaries are descriptive.
4. Create a pull request to the `main` branch.