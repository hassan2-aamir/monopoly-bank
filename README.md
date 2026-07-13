# 🏦 Monopoly Bank

A single-device banker console for Monopoly. One person (the banker) runs it on their machine or phone — everyone else just watches the screen. No accounts, no network sync, no sockets.

---

## Setup

```bash
cd monopoly-bank
npm install
node server.js
```

When the server starts, it prints your local address:

```
╔══════════════════════════════════════════════╗
║        MONOPOLY BANK — SERVER RUNNING        ║
╠══════════════════════════════════════════════╣
║  Local:    http://localhost:3000              ║
║  Network:  http://192.168.X.X:3000           ║
╚══════════════════════════════════════════════╝
```

Open that address in a browser. Everything runs on that one device — the game state lives in the browser's local storage, so refreshing the page won't lose your progress (use **Reset Game** to clear it).

---

## How it works

### 1. Add participants

On launch you get a setup screen. Type each player's name and click **Add** (or press Enter) — they appear as chips below. Click the ✕ on a chip to remove someone before starting.

### 2. Start the game

Click **Start Game ▶** once everyone's added. Each player starts with **$1,500**.

### 3. Run the bank from the player cards

Every player card (and the Free Parking card) has three buttons:

| Button | Action                                                                                                                                          |
| ------ | ----------------------------------------------------------------------------------------------------------------------------------------------- |
| **+**  | Add money — click, type the amount, press **Enter**.                                                                                            |
| **−**  | Subtract money — click, type the amount, press **Enter**.                                                                                       |
| **→**  | Transfer — click, then click the second player's card (or Free Parking), then type the amount on the arrow connecting them and press **Enter**. |

No extra clicks into text boxes — the amount field is focused automatically the moment you click. Press **Escape**, or click anywhere outside, to cancel an action in progress.

Free Parking also gets a **🏆** button (shown whenever it holds money) to instantly give the entire pot to whichever player card you click next.

---

## Starting Balance

Each player starts with **$1,500**. To change it, edit `STARTING_BALANCE` near the top of the `<script>` in `public/index.html`.

## Deploymed link

https://hassan2-aamir.github.io/monopoly-bank/
