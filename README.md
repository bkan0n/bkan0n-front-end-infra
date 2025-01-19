# Set up crowdsec on server

1. Add crowdsec repos `curl -s https://install.crowdsec.net | sudo sh`
2. Install IPTables bouncer `sudo apt install crowdsec-firewall-bouncer-iptables`
3. Enroll bouncer: `sudo cscli console enroll -e context TOKENHERE`

# Start compose with Doppler CLI
Assuming Doppler CLI has been set up for this repo/directory:
- `doppler run -- docker compose up -d`