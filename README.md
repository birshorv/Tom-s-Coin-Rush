# Tom's Coin Rush — game design

## Premise and identity
Tom is an original ginger cat driving a red arcade car. Drive along an endless three-lane road, collect coins, avoid traffic and cones, and improve the car between runs. Original vector graphics are drawn in Canvas and CSS; no outside character artwork or assets are used. The visual direction is a contemporary dusk road scene with charcoal surfaces, amber rewards, teal surroundings, and a compact editorial HUD.

## Landing page and stages
The first screen introduces Tom and presents two routes. Classic Circuit is open from the first launch, with the brighter original road style. Neon Highway unlocks once the player reaches 500 m in a run, then can be selected from the same landing page. It uses the redesigned dusk road, faster speed and denser traffic. The locked card shows remaining distance. Existing best scores unlock the stage automatically. The garage remains accessible from the landing page.

## Core loop
Start race → steer toward coin trails → avoid incoming cars/cones → gather 100 boost charge → trigger a four-second protective turbo → survive as long as possible → bank collected coins → buy permanent upgrades → retry. Runs grow faster over distance. A collision removes one heart and grants brief invulnerability; the race ends at zero hearts.

## Controls
Touch: tap or drag to a lane, tap BOOST. Mouse: click/drag to a lane. Keyboard: left/right or A/D to change lanes, Space for boost, Escape to pause. Pause and resume also work via visible buttons. The game preserves user progress in browser localStorage when run independently and uses YouTube Playables cloud save when embedded.

## Garage economy
Coin magnet: 80/160/240 coins for larger pickup range. Strong bumper: 110/220 coins for an extra starting heart per level. Turbo boost: 100/200/300 coins for faster charge. All currencies are earned through play; no purchase flow. Saved data is a compact profile of bank, best distance, and upgrade levels.

## Playables integration
The HTML loads YouTube SDK before game code, reports first frame and game ready, hooks pause/resume and audio state, submits best distance as score, and uses cloud save. Bundle uses relative paths and no network services besides the SDK. Before a YouTube release: device and layout QA, balance playtesting, test suite, thumbnails, metadata, and private portal certification.

## Next content pass
Add distinct traffic types, set-piece environments, missions, deeper road events, animation polish and original sound. Verify engine and input behavior inside the YouTube test suite. Current score is personal best distance, not a multiplayer leaderboard.
