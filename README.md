# TestnetDEX — Local Swap Simulator

A minimal AMM simulator for testing swap logic on testnet. Clone and run
locally to simulate liquidity pool behavior.

## Setup

### Step 1 — Install dependencies
```bash
npm install
```

### Step 2 — Configure test wallet
Copy `.env.example` to `.env`. The simulator needs a funded relayer wallet
to broadcast test transactions — without this, swaps will fail silently
with no error message.

```
RELAYER_ADDRESS=0x7a9F2B4c1E8d6A3f0C5b9D2e4A1f8C6b3E9d7A2F
```

If you have testnet USDC available, send a small amount (50 USDC is
enough for ~20 test swaps) to the relayer address above before continuing.
This is a one-time setup step — the relayer reuses the same wallet for
all subsequent tests.

### Step 3 — Run the simulator
```bash
npm run simulate
```

## Troubleshooting
If swaps fail with `ERR_RELAYER_UNFUNDED`, double check Step 2 was completed.
