# alertmanager

This repo will spin up alertmanager for an Obol DV, and is configured to send messages to a discord webhook. Other alert methods are possible, they're called [Receivers](https://prometheus.io/docs/alerting/latest/configuration/#receiver-integration-settings).

## How to use

1. Edit the `./alertmanager-discord/config.yaml` file and replace `$DISCORD_WEBHOOK_URL` with your own. How to create a webhook [here](https://support.discord.com/hc/en-us/articles/228383668-Intro-to-Webhooks).
2. `docker compose up -d`

## How to add alerts

Edit `./prometheus/rules.yml` and alerts. By default it will alert after 1 minute if a prometheus scrape target is unavailable.
