# Tower Defense

---

## 🧩 Game Overview
This is a Unity-based Tower Defense game implemented。 Players must place different types of towers to prevent enemies from reaching the leak point. The game progresses in rounds with increasing enemies.

---

## 🏗️ Implemented Features

A. Tower Types
- **Arrow Tower** – Fires fast homing projectiles, effective against both ground and flying enemies.
- **Cannon Tower** – Fires arcing projectiles, effective against grouped ground enemies, ineffective against flying enemies.
- **Hot Plate** – Constantly damages nearby ground enemies over time.
- **Barricade** – No attack. Used to shape enemy path.

B. Enemy Types
- **Ground Enemy** – Follows a path generated via NavMesh.
- **Flying Enemy** – Appears every 4th round, flies directly to the goal, can ignore barricades and Hot Plate.

C. Game Systems
- **Round Progression**:
  - Each round spawns more enemies (+3 per round).
  - Flying enemies appear every 4th round.
- **Gold System**: Players earn gold per round to build more towers.
- **Tower Selling**: Players can click towers to sell them and receive a partial refund.
- **Game Over**: When all player lives are depleted, the `Game Lost Panel` is displayed.
- **Play Button Lock Panel**: Prevents starting a round if no path is available.
- **Lives Display UI**: Shows current remaining lives at the bottom-right corner of the screen.

---

## 💡 Notable Improvements
A. Dynamic enemy difficulty: +3 enemies per round.
B. Added a `Lives Display Panel` mirroring the gold panel, updated every frame to reflect `remainingLives`.

---

## 🗂️ Project Structure
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
│   ├── Live Panel (⚠️New: show remaining lives)
│
├── Materials/ (optional)


---

## 📦 How to Run
1. Open in Unity 2022.3 or above.
2. Open `Main.unity` scene.
3. Click **Play** to test.
4. Use arrow keys or right-click drag to move the camera.

---


