# Warehouse Run - 2 Player Prototype

A mobile-first, top-down warehouse kart racer prototype.

## What is implemented
- 5 selectable racers plus a permanently locked sixth slot.
- 2-player peer-to-peer rooms using PeerJS/WebRTC.
- Solo test mode.
- 3-lap warehouse/yard circuit with a timed roller shutter.
- Moving forklift hazards, racking and yard obstacles.
- Pineapple weapon system:
  - 1 pineapple: straight shot.
  - 2 pineapples: one homing shot.
  - 3 pineapples: orbit the racer and fire one-by-one straight.
- Pipeline Punch-style pink can boost, stackable to 3 for longer boost duration.
- Character voice lines through browser text-to-speech (Coco remains silent).
- Mobile landscape touch controls plus keyboard controls.

## Run locally
Serve this folder over HTTP. For example:

```bash
python3 -m http.server 8080
```

Then open http://localhost:8080.

For multiplayer between phones, deploy the folder to any HTTPS static host (Vercel works well). One player chooses **Create room**, the other chooses **Join room** and enters the 5-character code.

## Desktop controls
- Arrow keys / WASD: drive
- Space: fire pineapple
- Shift: use stored boost

## Prototype notes
The multiplayer model is host-authoritative. The host simulates both racers and broadcasts race state to player 2 over WebRTC. It is intentionally lightweight for a first playable build.
