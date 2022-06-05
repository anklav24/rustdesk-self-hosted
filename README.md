# Open Source Alternative to TeamViewer

## Requirements

- git
- docker
- docker-compose
- small vps
- external ip address
- domain name (optional)
- access to your router and firewall

## Setting-up

- Clone repository

  ```bash
  cd ~
  git clone https://github.com/anklav24/rustdesk-self-hosted.git
  cd rustdesk-self-hosted
  ```

- Edit `.env`

  ```bash
  cp .env.example .env
  vim .env
  ```

- Start servers

  ```bash
  docker-compose up -d
  docker-compose logs -f
  ```

- Open ports on your router and forward to server with rustdesk
  - TCP: 21115, 21116, 21117, 21118, 21119
  - UDP: 21116

- Set-up user apps
  - Get the key on the server

  ```bash
  cat data/*.pub
  ```

  - Id server: YOUR_DOMAIN_NAME
  - Key: SQJABZtnQkwpT1SJFkg14iuM2KhuVkeKOi+wCV6HI6A=  (Example)
