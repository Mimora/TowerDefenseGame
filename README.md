# 🏰 Tower Defense Game

---

## 🧩 Game Overview
A Unity-based Tower Defense game where players strategically place towers to stop enemies from reaching the leak point.  
The game progresses in rounds, with the number of enemies increasing each round.

---

## 🏗️ Implemented Features

### A. Tower Types
- **Arrow Tower** – Fires fast homing projectiles, effective against both ground and flying enemies.
- **Cannon Tower** – Fires arcing projectiles, strong against groups of ground enemies, ineffective against flying enemies.
- **Hot Plate** – Constantly damages nearby ground enemies over time.
- **Barricade** – Does not attack, used to shape enemy paths.

### B. Enemy Types
- **Ground Enemy** – Follows paths generated via Unity NavMesh.
- **Flying Enemy** – Appears every 4th round, flies directly to the goal, ignores barricades and Hot Plate.

### C. Game Systems
- **Round Progression**:
  - Each round spawns **+3 more enemies** than the previous round.
  - Flying enemies appear every 4th round.
- **Gold System** – Earn gold each round to build more towers.
- **Tower Selling** – Click towers to sell them for a partial gold refund.
- **Game Over** – Displays the `Game Lost Panel` when all lives are depleted.
- **Play Button Lock Panel** – Prevents starting a round if no valid path exists.
- **Lives Display UI** – Shows remaining lives at the bottom-right corner of the screen.

---

## 💡 Notable Improvements
1. **Dynamic Enemy Scaling** – Each round adds **+3 enemies** for increased difficulty.
2. **Lives Display Panel** – Added to the UI, mirroring the Current Gold panel, updated every frame to reflect remaining lives.
3. **Bug Fix** – Resolved an issue where enemies reaching the leak point were not properly removed from the `enemyHolder`, preventing round progression.

---

## 🗂️ Project Structure
```text
Assets/
├── Prefabs/
│   ├── Towers: Arrow Tower, Cannon Tower, Hot Plate, Barricade
│   ├── Enemies: Ground Enemy, Flying Enemy
│
├── Scripts/
│   ├── Enemy.cs
│   ├── GroundEnemy.cs
│   ├── FlyingEnemy.cs
│   ├── Player.cs
│   ├── Tower.cs
│   ├── Targeter.cs
│   ├── TargetingTower.cs
│   ├── Projectile.cs
│   ├── FiringTower.cs
│   ├── SeekingProjectile.cs
│   ├── ArcingProjectile.cs
│
├── Scenes/
│   └── Main.unity
│
├── UI/
│   ├── Build Button Panel
│   ├── Play Button
│   ├── Play Button Lock Panel
│   ├── Tower Selling Panel
│   ├── Game Lost Panel
│   ├── Current Gold Panel
│   ├── Live Panel (⚠️ New: show remaining lives)
│
├── Materials/ (optional)
```
---

## 📦 How to Run
1. Open in **Unity 2022.3** or later.
2. Load the `Main.unity` scene.
3. Click **Play** to start.
4. Move the camera with **Arrow Keys** or **Right-click + Drag**.

---

## 🛠️ Tools & Technologies
- **Unity 2022.3**
- **C#**
- **TextMeshPro**
- **Unity NavMesh**

---

## 🖼️ Previews
<img width="671" height="569" alt="截屏2025-04-26 00 44 56-24" src="https://github.com/user-attachments/assets/2caf6ada-8388-4230-9264-d65900d5716f" />
<img width="671" height="569" alt="截屏2025-04-26 00 46 03-26" src="https://github.com/user-attachments/assets/c1e1fcec-6858-4059-b150-a44521fbd70a" />
<img width="671" height="569" alt="截屏2025-04-26 00 47 02-30" src="https://github.com/user-attachments/assets/93545d91-a9d2-43e4-be53-5ae8b75fef7e" />
<img width="671" height="569" alt="截屏2025-04-26 00 48 25-28" src="https://github.com/user-attachments/assets/b7ee64a9-5486-487d-af0c-47bf19574eee" />



