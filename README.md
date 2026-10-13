# SENSEX Option OI Monitor

Streamlit app that tracks the SENSEX option chain (Upstox API, BSE_INDEX|SENSEX, weekly + monthly expiries) with the same table as the NIFTY 50 / BANKNIFTY versions:
buildup labels, Market View, strike PCR, fast-move rockets, spread, volume, signal and strike ideas.

## Run locally
    pip install -r requirements.txt
    streamlit run app.py

No token? Tick **Demo mode** in the sidebar (synthetic SENSEX data).

## Deploy (GitHub + Streamlit Community Cloud)
1. Push this folder to a GitHub repo (`.gitignore` already excludes secrets).
2. share.streamlit.io -> New app -> pick the repo, main file `app.py`.
3. App settings -> Secrets:
       UPSTOX_ACCESS_TOKEN = "your-access-token"
4. The Upstox access token expires daily (~3:30 AM IST): update the secret and reboot the app.

Never commit a real token to GitHub.
