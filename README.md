# Monero Merchant Umbrel Community App Store

Community App Store URL for testing the Monero Merchant Umbrel integration bounty:

```text
https://github.com/ryriigh/monero-merchant-umbrel-store
```

In umbrelOS, open **App Store -> Community App Stores -> Add Store** and paste the URL above. The app appears as **Monero Merchant** with app id `ryriigh-monero-merchant`.

This store mirrors the bounty PR package in [`Monero-Merchant/monero-merchant#33`](https://github.com/Monero-Merchant/monero-merchant/pull/33). The store-specific app id is prefixed with `ryriigh-` because Umbrel Community App Stores require app ids to start with the store id.

## Validation

```sh
APP_DATA_DIR="$(pwd)/.umbrel-test-data" \
APP_PASSWORD="change-me-in-production" \
APP_SEED="$(openssl rand -hex 32)" \
docker compose -f ryriigh-monero-merchant/docker-compose.yml config
```
