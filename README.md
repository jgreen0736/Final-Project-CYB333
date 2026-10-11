# Final-Project-CYB333

## Email and Slack alerts

Run both alert paths offline with mocked SMTP and Slack transports:

```bash
python3 alert_demo.py --mock
```

The mock run validates each alert's payload and reports simulated success without contacting either service. To send real alerts, create a local `.env` file with SMTP and Slack webhook settings, replace all example values with your own credentials, and run `python3 alert_demo.py --send`. Real mode sends actual email and Slack alerts. Never commit `.env`, passwords, or webhook URLs; they are excluded by `.gitignore`.