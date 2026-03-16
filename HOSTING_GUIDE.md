# Hosting Your Solar Dashboard

## Option 1: Quick Local Test
Just open `page.html` directly in your browser - no server needed.

---

## Option 2: Host on Raspberry Pi (Local + Remote Access)

### Step 1: Host Locally on Pi
```
bash
# SSH into your Pi, then:
mkdir ~/solar-dashboard
# Copy page.html to this folder on Pi

cd ~/solar-dashboard
python3 -m http.server 8080
```

### Step 2: Access Locally
- Browser: `http://192.168.1.XXX:8080/page.html`

### Step 3: Access Remotely (Outside Home)

#### Method A: ngrok (Easiest - Free)
```bash
# On Pi, install ngrok:
curl -s https://ngrok-agent.s3.amazonaws.com/ngrok.zip -o ngrok.zip
unzip ngrok.zip
./ngrok http 8080

# You'll get a public URL like: https://abc123.ngrok.io
# Use this URL from anywhere!
```

#### Method B: Cloudflare Tunnel (Best - Free)
```
bash
# Install cloudflared on Pi:
curl -L https://github.com/cloudflare/cloudflared/releases/latest/download/cloudflared-linux-arm64 -o cloudflared
chmod +x cloudflared

# Create free tunnel:
./cloudflared tunnel create solar-dashboard
./cloudflared tunnel url solar-dashboard

# Get your public URL from cloudflare dashboard
```

#### Method C: Tailscale VPN (Most Secure)
```
bash
# Install Tailscale on Pi:
curl -fsSL https://tailscale.com/install.sh | sh

# Login and connect
tailscale up

# Access via: http://tailscale-ip:8080/page.html
```

---

## Your Pi IP Address
Check your Pi's local IP:
```
bash
hostname -I
```

---

## Need Help?
Let me know which method you want to set up and I can provide detailed steps!
