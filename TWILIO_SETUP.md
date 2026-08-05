# Twilio SMS Alert Setup Guide

## Step 1: Get Your Twilio Credentials

1. Sign up for a free Twilio account at https://www.twilio.com/console
2. After signing up, you'll see your **Account SID** and **Auth Token** on the dashboard
3. Copy these values (keep Auth Token secure!)

## Step 2: Get a Twilio Phone Number

1. In the Twilio Console, go to **Phone Numbers > Manage Numbers > Active Numbers**
2. If you don't have one, click **Get Your First Twilio Phone Number**
3. Follow the prompts to claim a phone number (e.g., +1234567890)
4. Copy this phone number

## Step 3: Configure .env File

Edit the `.env` file in the project root and fill in these values:

```
TWILIO_ACCOUNT_SID=your_account_sid_here
TWILIO_AUTH_TOKEN=your_auth_token_here
TWILIO_PHONE_NUMBER=+1234567890
RECIPIENT_PHONE_NUMBER=+91XXXXXXXXXX
ENABLE_SMS_ALERTS=true
```

### Where to find these:

- **TWILIO_ACCOUNT_SID**: Twilio Console Dashboard (looks like: AC...)
- **TWILIO_AUTH_TOKEN**: Twilio Console Dashboard (next to Account SID)
- **TWILIO_PHONE_NUMBER**: From Twilio > Phone Numbers > Active Numbers
- **RECIPIENT_PHONE_NUMBER**: Your phone number (with country code, e.g., +91 for India, +1 for USA)
- **ENABLE_SMS_ALERTS**: Set to `true` to enable, `false` to disable

## Step 4: Install Python Package

Run this in your terminal:

```bash
pip install twilio python-dotenv
```

Or if using venv:

```bash
.\.venv\Scripts\pip install twilio python-dotenv
```

## Step 5: Test the Setup

1. Start the server: `.\.venv\Scripts\python.exe app.py`
2. Open the browser and go to http://127.0.0.1:5000
3. Go to Webcam tab and click **Start Webcam**
4. Make a sad/fear/angry face for 10+ seconds
5. Check your phone — you should receive an SMS alert!

## Alert Message Format

When an emotion is detected, you'll receive:
```
🚨 Emotion Alert: Person detected with Sad emotion at 2026-02-24 18:45:30
```

## SMS Cooldown

- SMS alerts are sent **once every 60 seconds** per emotion type (to avoid spam)
- Terminal prints happen every second once threshold is reached
- You can adjust the cooldown in `app.py` by changing the `60.0` value

## Troubleshooting

- If SMS doesn't arrive: Check `.env` credentials are correct
- If you see "Twilio initialization failed": Make sure `python-dotenv` is installed
- Trial accounts may have restrictions on recipient phone numbers
- Make sure your phone number includes the country code (e.g., +91, +1)
- If terminal says "SMS request accepted" but no SMS arrives, check Twilio Console > Monitor > Logs > Messaging for delivery status and error codes
- `error_code=30008` means carrier/network rejected delivery (common with international routes like US Twilio number to India)
- For India (+91), trial/US long-code routes are often blocked unless account/number setup supports India regulations; typically requires a paid account and India-compliant sender setup
- In Twilio Console, verify:
	- Destination number is verified (trial accounts)
	- Geo permissions for SMS to India are enabled
	- Sender type supports the destination country
- Rotate credentials immediately if `.env` was shared/screenshotted publicly (especially Auth Token)
