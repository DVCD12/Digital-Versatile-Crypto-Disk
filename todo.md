# DiscWallet TODO

- [x] Y2K Optical Deck design system (dark chassis, amber LED, Chakra Petch + JetBrains Mono)
- [x] Read Disc via window.showDirectoryPicker (Chrome/Edge)
- [x] Recursive directory fingerprint: sorted path:filesize + volume label, cap 400 entries / depth 3
- [x] SHA-256 fingerprint → ed25519 seed → tweetnacl keypair → base58 Solana address
- [x] Eject detection: poll directory handle every 4s, lock back to idle screen when unreadable
- [x] Idle screen with animated iridescent CD (spins faster while reading) and Read Disc button
- [x] Wallet screen: address + copy button, live SOL balance, disc label, fingerprint hex, Eject button
- [x] Live SOL balance via getBalance JSON-RPC (direct to api.mainnet-beta.solana.com, server relay fallback for 403)
- [x] Simulate Disc button with rotating fake disc catalog
- [x] Fallback: <input webkitdirectory> one-shot read for Firefox/Safari
- [x] Drive-bay aesthetic: faceplate, screws, vents, activity LED, VFD readout panels
- [x] Vitest tests: derivation determinism + relay procedure
- [x] Final visual verification and checkpoint

## Multi-chain hardware-wallet upgrade

- [x] Derive Ethereum address from disc fingerprint (secp256k1 + keccak256, EIP-55 checksum)
- [x] Derive Bitcoin address from disc fingerprint (secp256k1, P2WPKH bech32)
- [x] Derive additional EVM-compatible chains (Polygon, Base) sharing the ETH address
- [x] Server relay procedures for ETH/BTC/EVM balance fetching (public RPCs/APIs)
- [x] Chain-selector UI in the deck (hardware-wallet style chain list with per-chain LED/balances)
- [x] Per-chain address + copy + live balance readout
- [x] Vitest tests for multi-chain derivation determinism and relays
- [x] Visual verification and checkpoint

## Disc-insertion animation

- [x] Drive-slot visual (horizontal slot with bezel/LED) in the disc tray area
- [x] Reading state: disc slides/inserts into the slot instead of only spinning in place
- [x] Loaded state: disc remains docked in slot; eject slides it back out
- [x] Verify animation in browser (simulate flow) and mobile layout
- [x] Checkpoint and deliver

## Bug fixes

- [x] Fix insertion animation: disc appears to pass behind the bezel instead of into the slot — clip the disc exactly at the slot mouth line
- [x] Rework insertion geometry: disc must stay in front of the bezel and only disappear through the slot mouth itself (clip boundary = slot line, disc rendered above bezel)

## Send / Receive per chain

- [x] Vintage DVD-deck styled SEND / RECEIVE transport buttons in the chain readout
- [x] Receive panel: address + QR code per chain
- [x] Send panel: recipient + amount form with deck styling
- [x] Solana send: build/sign transfer client-side with disc-derived key, broadcast via relay
- [x] EVM send (ETH/Polygon/Base): sign EIP-1559 tx client-side, broadcast via relay
- [x] Bitcoin send: graceful receive-only (SEND disabled with "RECEIVE-ONLY" note)
- [x] Server relay endpoints for broadcasting transactions per chain
- [x] Tests for send building/signing helpers
- [x] Verify flows in browser and checkpoint

## Rebrand

- [x] Rename "DiscWallet" to "DVCD" everywhere in the site UI (header, title, meta, footer copy, toasts, alt text)
