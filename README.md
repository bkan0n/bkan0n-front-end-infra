# Set up crowdsec on server

1. Add crowdsec repos 

    `curl -s https://install.crowdsec.net | sudo sh`

2. Install IPTables bouncer 

    `sudo apt install crowdsec-firewall-bouncer-iptables`

3. Enroll bouncer: 

    `sudo cscli console enroll -e context TOKENHERE`

# Start compose with Doppler CLI
Assuming Doppler CLI has been set up for this repo/directory:
- `doppler run -- docker compose up -d`





# restic backups via backrest
- https://backup.bkan0n.com

### Set up
> [!IMPORTANT]
> MAKE SURE `config.json` IS BACKED UP IN PASSWORD MANAGER FOR ALL RESTIC REPO CHANGES

1. If total loss occurs, initialize backrest.
    1. Grab `config.json` from password manager secure note.
    2. Place in backrest config directory.
2. Reindex snapshots

### To restore specific snapshots
1. Copy `Snapshot ID` from backrest
2. Click `Run Command` in backrest
3. `restore SNAPSHOT_ID --target /path/to/restore`
4. Visit `/path/to/restore` and move files to original location as needed.