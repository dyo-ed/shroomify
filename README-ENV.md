# Environment Setup for Shroomify

This document explains how to set up the environment variables for the Shroomify project.

## Frontend Environment Variables

Create a `.env.local` file in the root directory with the following variables:

```bash


# Backend API Configuration
NEXT_PUBLIC_API_URL=http://localhost:5000
NEXT_PUBLIC_NGROK_URL=https://reliably-one-kiwi.ngrok-free.app
```

## Backend Environment Variables

The backend configuration is in `backend/config.env`. Update the following values:

```bash
# ngrok Configuration
NGROK_DOMAIN=reliably-one-kiwi.ngrok-free.app
NGROK_AUTHTOKEN=your_ngrok_authtoken_here

# Security Configuration
SECRET_KEY=your_secret_key_here
```

## Getting Your Values



### ngrok
1. Sign up at https://ngrok.com
2. Get your authtoken from the dashboard
3. Update the NGROK_AUTHTOKEN in backend/config.env

### Secret Key
Generate a random secret key for Flask sessions:
```bash
python -c "import secrets; print(secrets.token_hex(32))"
```

## File Structure
- `.env.local` - Frontend environment variables (create this file)
- `backend/config.env` - Backend environment variables (already exists)
- `env.example` - Example frontend environment file
