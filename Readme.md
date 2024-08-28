# Demo services
- SSH Service 1: Bound on port 10122
- SSH Service 2: Bound on port 10222
- Traefik main entrypoint: Bound on port 10022 --> Change this in docker-compose.yml within traefik config

# Try it
`docker compose up --build -d`  
`ssh -p 10022 sshuser@127.0.0.1` # Try to connect from whatever IP  
`ssh -p 10022 sshuser@192.168.1.90`# Try to connect from whitelisted Client IP  

username: sshuser
password: password

# Change services to something 
1. Replace real targets instead of fake ssh services within traefik/ssh.yml
2. Replace ClientIP for the split within traefik/ssh.yml

