🌊 WaveManager – Dynamic 3D Spawn System for Unity

A flexible and performance-friendly wave-based object spawner designed for 3D environments in Unity.
Perfect for enemy waves, item drops, and procedural spawning systems.

✨ Overview

WaveManager allows you to spawn multiple object types in controlled waves inside a ring-shaped area, using physics-based raycasts to perfectly align objects with uneven terrains.

It supports dynamic difficulty scaling, custom spawn profiles, and layer-based spawn filtering — giving you full control over spawning behavior directly from the Unity Editor.

🎮 Features
🌀 Ring-Based Spawn Area

Defines an inner and outer radius to create a circular spawn zone.

Ensures precise placement with raycasts, adjusting object positions to match terrain slopes.

🧩 Multi-Profile Spawning

Add multiple SpawnProfiles, each with:

Custom prefab

Base spawn rate

Object cap (maxActiveCount)

Optional particle or visual effects

⚙️ Dynamic Difficulty System

Uses an AnimationCurve to scale difficulty non-linearly.

Increases spawn frequency and object count as difficulty rises.

Difficulty	Spawn Interval	Objects per Wave
0	Slow	Few
5	Medium	Moderate
10	Very Fast	Many
🚫 Layer-Based Filtering

Define which layers should not spawn objects using a LayerMask.

Example: prevent spawning on the "Ground" layer while allowing it on "Buildings" or "Terrain".

🧠 Object Tracking

Keeps a dictionary of all active objects for each profile.

Automatically removes entries when objects are disabled or destroyed.

🧭 Scene Gizmos

Inner and outer spawn rings are visualized in the Scene view for easy editing.

⚡ Example Use Case

Enemies: Spawn more enemies faster as difficulty rises.

Pickups: Scatter health packs or resources around a zone.

Environmental FX: Spawn falling rocks, meteors, or dynamic scenery.

📜 Inspector Breakdown
🔹 Ring Settings
Field	Description
centerPoint	The transform used as the spawn area’s center
innerRadius	Minimum spawn distance
outerRadius	Maximum spawn distance
ignoreLayers	Layers that block spawning
🔹 Difficulty Settings
Field	Description
difficulty	Global difficulty value (0–10)
difficultyCurve	Controls how spawn frequency scales with difficulty
🔹 SpawnProfile
Field	Description
prefab	Object to spawn
baseSpawnInterval	Default time between waves
baseSpawnCountPerWave	Default spawn amount per wave
maxActiveCount	Maximum active objects
spawnEffect	Optional particle or visual effect
💡 Tips

Use AnimationCurve to fine-tune difficulty growth.

Combine with an AI Manager or Object Pooling System for optimal performance.

Visualize your spawn zone using OnDrawGizmosSelected().

🔧 Requirements

Unity 2021.3 or newer

Works with both URP and HDRP

Physics-based scenes recommended

🧾 License

This project is open-source.
You are free to use, modify, and distribute it in both personal and commercial projects.
