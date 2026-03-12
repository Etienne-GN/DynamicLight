# Dynamic Light v1.8.0: Verification Test Plan

Follow these steps to confirm all features are working correctly.

## 🧪 1. Held Item Lighting (Main-hand)
- [ ] **Torch**: Hold a standard torch in your main hand. Does it emit light?
- [ ] **Lantern**: Hold a lantern. Does it emit light? (Report if it fails)
- [ ] **Lava Bucket**: Hold a lava bucket. Does it emit light? (Report if it fails)
- [ ] **Moving**: Walk while holding a light source. Does the light follow you smoothly?

## 🧪 2. Off-hand Support & Torching
- [ ] **Off-hand Torch**: Place a torch in your off-hand. Does it emit light?
- [ ] **Off-hand Swap**: Hold a torch in your main hand (off-hand empty) and long-click (interact) while NOT looking at a block. Does the torch move to your off-hand?
- [ ] **Placement Priority**: Look at a block within 4 blocks and long-click with a torch. Does it place the torch instead of swapping to off-hand?

## 🧪 3. Entity & World Illumination
- [ ] **Glow Squids**: Find a Glow Squid. Does it illuminate its surroundings?
- [ ] **Blazes**: Spawn a Blaze. Does it emit light?
- [ ] **Magma Cubes**: Spawn a Magma Cube. Does it emit light?
- [ ] **Dropped Items**: Throw a torch on the ground. Does the dropped item entity emit light?
- [ ] **Burning Entities**: Set a mob on fire (e.g., a Zombie in daylight). Does it emit light while burning?

## 🧪 4. Environmental Effects
- [ ] **Underwater**: Hold a Sea Lantern underwater. Does it function?
- [ ] **HeartBeat (Flickering)**: Stand still with a torch. Does the light level fluctuate slightly for a "flicker" effect?
- [ ] **Raycasting**: Walk past a thin wall (1 block thick). Does the light bleed through to the other side? (Check for refinement).

## 🧪 5. Performance & Tiers
- [ ] **Memory Scaling**: On a server/device with lower RAM, does the lighting updates per second (UPS) decrease automatically?
- [ ] **Lag Test**: Hold a torch and run quickly. Does the light keep up or lag behind significantly?
