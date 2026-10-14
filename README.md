# GOAT Cricket Universe — gameplay upgrade

A browser-based 3D cricket prototype focused on more physical ball flight and active fielding. It preserves the existing GOAT stadium concept and project folder.

## Run the game

The page loads Three.js from jsDelivr, so an internet connection is required.

1. Install Node.js on a computer.
2. Open a terminal inside `goat-cricket-universe`.
3. Run `npm install`.
4. Run `npm run dev`.
5. Open the local address printed by Vite.

For a production build, run `npm run build`; Vite writes the built site to `dist/`.

## Controls

- **BOWL NEXT** — begin a delivery.
- **PLAY SHOT** — time the bat swing as the ball approaches the batter.
- Choose **DRIVE**, **LOFT**, or **DEFEND** and a direction before playing.
- **RUN** — call a run while the ball is in play; a fielder can gather and throw at the wicket, with a run-out chance.
- **CAMERA VIEW** — cycle through broadcast, batter, fielding and bowler views.
- Keyboard: **Space** bowls / plays a shot depending on the current phase; **R** calls a run; **C** cycles camera.

## Gameplay systems in this update

- Time-stepped ball motion with gravity, speed-dependent aerodynamic drag, approximate spin/Magnus deviation, pitch bounce, restitution and ground friction.
- Timing and line affect contact quality and launch speed/angle; drive, loft and defend produce different trajectories.
- Active fielders pursue the ball, back up the chase, gather ground balls and can attempt to throw at the wicket.
- Lofted shots can be caught by a fielder who reaches the descending ball; boundaries distinguish a bounce-over-rope four from a clean six.
- Run calls, score/over tracking, wicket limits, T20 innings limit, and a basic run-out outcome.
- Touch-friendly controls and keyboard shortcuts.

## Honest limitations

This is still a gameplay prototype, not a finished photorealistic or true 4K AAA cricket game. Players are procedural models rather than detailed rigged likenesses; running, throwing and catching use simplified procedural animation and collision checks. It does not yet include a full official cricket rules engine, professional motion-captured animations, a complete 11-player fielding AI, realistic umpire decisions, ball-by-ball commentary audio, or licensed movie assets. The six reference photos are not embedded as 3D player models in this build.

“4K” depends on the display, browser and device GPU; this project renders responsively and caps device pixel ratio for performance rather than forcing 4K on mobile. The stadium is procedural and needs professionally authored textures, models, lighting and animation assets for photorealism. Gameplay and performance have not been verified on every Android device.
