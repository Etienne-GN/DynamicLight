# True Dynamic Light
Real-time lighting effects for held items, entities, and projectiles.

## 🗺 Roadmap

### 🟢 Verified
* **Multi-Tier Performance**: Automatically adjusts quality based on server memory (Low, Mid, High, SuperHigh).
* **Held Item Lighting**: Players holding torches, lanterns, or lava buckets emit light.
* **Off-hand Support**: Lighting now works for items in the off-hand.
* **Torching to Off-hand**: Long-clicking (item use) with a light-emitting item moves it to the empty off-hand.
* **Entity Illumination**: Blazes, Magma Cubes, and Glow Squids naturally emit light.
* **Dropped Item Lighting**: Light-emitting items on the ground still function as light sources.
* **HeartBeat System**: Torches and fire-based sources have a realistic flickering effect.
* **Underwater Support**: Sea lanterns and other water-loggable items work submerged.
* **Dynamic Fire Lighting**: Entities on fire emit light while burning.

### 🔵 To Test
* **Raycasting Accuracy**: Lighting occasionally clips through thin walls or corners (Needs Refinement).

### ⚪ To-Do
1. **Projectile Lighting**: Glowing projectiles (like Flaming Arrows or Fireballs) should emit light while in flight.
2. **Colored Lighting**: (Experimental) Use different light block intensities or particles to simulate colored light for Soul Torches or Redstone.
3. **Custom Item Tags**: Allow other mods to register light-emitting items via tags (e.g., `dynamic_light:15`).
4. **Armor Illumination**: Wearing specific armor (like a "Glow Helmet") should provide light.
5. **Dimming Effect**: Gradually decrease light intensity as a source (like a torch) "burns out" if a durability system is implemented.
6. **Performance Toggle**: Add an in-game command to manually switch between performance tiers.
7. **Block-to-Light Mapping**: Expand the `ItemIlumination` list to include all 1.21+ light-emitting blocks (e.g., Trial Spawners, Vaults).

## 🛠 Build Instructions
To create the `.mcaddon` file for testing:
1. From the project root, run: `./package_addon.sh dynamic_lights`

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
