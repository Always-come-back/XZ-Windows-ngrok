# XZ-Windows-ngrok

This project was created by **İsmet Emir** and uses GitHub Actions to deploy a Windows Server 2022 instance and set up Ngrok for secure remote access. Ngrok is a tunneling service that allows applications running on your local network to be accessible over the internet. Using this setup, you can access the created server remotely for up to 6 hours as long as the CMD window remains open.

---

## Features

- **Windows Server 2022**: Automatically deploys a server using GitHub Actions.
- **Ngrok Integration**: Enables remote access to the server through Ngrok tunnels.
- **Secure Configuration**: Utilizes GitHub Secrets to store sensitive information like the Ngrok token.

---

## How It Works

1. **Trigger GitHub Actions**: The workflow deploys a Windows Server 2022 instance.
2. **Secure Ngrok Configuration**: Requires an Ngrok authentication token, securely stored as a GitHub Secret.
3. **Obtain Ngrok Tunnel URL**: The workflow outputs a Ngrok TCP address for remote desktop access.

---

## Prerequisites

- A [GitHub](https://github.com/) account.
- An [Ngrok](https://ngrok.com/) account with an authentication token.

---

## Setup Instructions

### Step 1: Fork the Repository

1. Clone or fork this repository to your GitHub account.

### Step 2: Add Ngrok Authentication Token as a GitHub Secret

1. Go to the **Settings** tab of your forked repository.
2. Under the **Security** section, click on **Secrets and variables** > **Actions**.
3. Click on the **New repository secret** button.
4. Create a secret named `NGROK_AUTH_TOKEN` and paste your Ngrok authentication token as the value.
5. Save the secret.

### Step 3: Run the Workflow

1. Navigate to the **Actions** tab in your forked repository.
2. Select the workflow file and trigger it manually.
3. The workflow will automatically retrieve the `NGROK_AUTH_TOKEN` secret and configure Ngrok.

### Step 4: Access the Server

1. Once the workflow completes, you will receive a Ngrok TCP URL in the workflow logs.
2. Use this URL to connect to the server via Remote Desktop Protocol (RDP).

---

## Notes

- The server remains active for **6 hours** unless the CMD window is closed.
- Always store sensitive information, such as Ngrok tokens, in GitHub Secrets for enhanced security.
- Check the [Ngrok documentation](https://ngrok.com/docs) for further details on tunnel configurations.

---

## Credits

Developed by **İsmet Emir**.

---

## License

This project is licensed under the [MIT License](LICENSE).

For further questions or assistance, feel free to open an issue in the repository. Happy coding!
