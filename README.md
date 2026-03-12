# True Dynamic Light
Real-time lighting effects for held items, entities, and projectiles.

## 🗺 Roadmap

### 🟢 Verified
* **Multi-Tier Performance**: Automatically adjusts quality based on server memory (Low, Mid, High, SuperHigh) (v1.8.0).
* **Held Item Lighting (Torch Only)**: Players holding torches emit light (v1.8.0).
* **Off-hand Support (Torch Only)**: Lighting works for torches in the off-hand (v1.8.0).
* **Torching to Off-hand (Torch Only)**: Long-clicking (item use) with a torch moves it to the empty off-hand (v1.8.0).
* **Entity Illumination**: Blazes, Magma Cubes, and Glow Squids naturally emit light (v1.8.0).
* **Dropped Item Lighting (Torch Only)**: Light-emitting items on the ground still function as light sources (v1.8.0).
* **HeartBeat System**: Torches and fire-based sources have a realistic flickering effect (v1.8.0).
* **Underwater Support**: Sea lanterns and other water-loggable items work submerged (v1.8.0).
* **Dynamic Fire Lighting**: Entities on fire emit light while burning (v1.8.0).

### 🔵 To Test
* **Raycasting Accuracy**: Lighting occasionally clips through thin walls or corners (Needs Refinement).
* **Lantern & Lava Bucket Support**: Verify if other light sources from `ItemIlumination` list are functioning as intended.

### ⚪ To-Do
1. **Projectile Lighting**: Glowing projectiles (like Flaming Arrows or Fireballs) should emit light while in flight.
2. **Colored Lighting**: (Experimental) Use different light block intensities or particles to simulate colored light for Soul Torches or Redstone.
3. **Custom Item Tags**: Allow other mods to register light-emitting items via tags (e.g., `dynamic_light:15`).
4. **Armor Illumination**: Wearing specific armor (like a "Glow Helmet") should provide light.
5. **Dimming Effect**: Gradually decrease light intensity as a source (like a torch) "burns out" if a durability system is implemented.
6. **Performance Toggle**: Add an in-game command to manually switch between performance tiers.
7. **Block-to-Light Mapping**: Expand the `ItemIlumination` list to include all 1.21+ light-emitting blocks (e.g., Trial Spawners, Vaults).
8. **Broaden Held Item Support**: Ensure all items in `ItemIlumination` (Lanterns, Soul Torches, etc.) work for main-hand and off-hand.
9. **Broaden Torching to Off-hand**: Support all light-emitting items for the "move to off-hand" feature.

## 🛠 Build Instructions
To create the `.mcaddon` file for testing:
1. From the project root, run: `./package_addon.sh DynamicLight`

## 📜 Changelog

### [1.8.0] - Active Development
#### Added
- Multi-Tier Performance: Automatically adjusts quality based on server memory.
- Held Item Lighting (Main-hand and Off-hand).
- Torching to Off-hand: Long-clicking with light item moves it to empty off-hand.
- Entity Illumination (Blazes, Magma Cubes, Glow Squids).
- Dropped Item Lighting.
- HeartBeat System: realistic flickering effect for fire sources.
- Underwater Support.
- Dynamic Fire Lighting for burning entities.
#### Changed
- Raycasting Accuracy needs refinement (Current known issue).

## ⚖️ Commit & Versioning Rules
1. **Stable UUIDs:** Once a mod version is stable, **DO NOT** change the `uuid` in `manifest.json`.
2. **Increment Version:** To update the mod, only increment the `version` array in `manifest.json`. This allows users to import it as an update without deleting the old version.
3. **Update README:** After every significant change, update the Roadmap in the `README.md` (move items from To-Do to Verified).

## Custom Addon Integration
To implement dynamic lighting in third-party addons:
- Add a `dynamic_light:light_level` tag to the item.
- Replace `light_level` with the desired light intensity (0 - 15).
