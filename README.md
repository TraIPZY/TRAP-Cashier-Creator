

## 🧾 TRAP Cashier Creator — FiveM ESX Script
<img width="1536" height="1024" alt="ChatGPT Image 30 déc  2025, 16 h 05 min 54 s" src="https://github.com/user-attachments/assets/f31a2965-1d9b-400c-b672-9a85bffd740c" />

**TRAP Cashier Creator** is a FiveM script made for **ESX roleplay servers** that want a clean, immersive, and fully functional cashier system for all job-based businesses.

Admins can place cash registers directly in-game, link them to specific jobs, and employees can bill nearby players through a simple, intuitive interface.

🔗 YouTube Preview: **[https://www.youtube.com/watch?v=GAzd1ECR-jI](https://www.youtube.com/watch?v=GAzd1ECR-jI)**

🛒 Get it on Tebex: **[https://trap-scripts.tebex.io/package/7197624](https://trap-scripts.tebex.io/package/7197624)**

---

## ✨ Features

### 🔑 Admin Features

* **/addcashier** — Place cashiers directly in game
* Set a custom cashier name
* Link the cashier to a specific ESX job
* Persistent and database-based

---

### 🧑‍💼 Employee Usage

* Interaction via **ox_target**
* Clean billing menu using **ox_lib**
* Enter billing amount
* Select the client from a dropdown list
* **Choose payment method: Cash or Bank**
* Real-time, RP-friendly workflow

---

### 👤 Client Side

* Payment request notification
* Accept or decline payment
* Payment deducted from Cash or Bank
* UI confirmation for both parties

---

### 💰 Money Handling

* Money sent directly to the **job society account**
* Fully compatible with **esx_addonaccount**
* Cash and Bank payment support
* No fake items or external dependencies

---

### 🛠️ Admin Management — `/cashierlist`

* View all existing cashiers
* Teleport to a cashier
* Delete any cashier
* Simple and effective admin control

---

## 📦 Commands

| Command        | Description                         |
| -------------- | ----------------------------------- |
| `/addcashier`  | Create and place a new cashier      |
| `/cashierlist` | View, teleport, and delete cashiers |

---

## ⚙️ Dependencies

* **es_extended**
* **ox_lib**
* **ox_target**
* **oxmysql**
* **esx_addonaccount**

---

## 🗄️ SQL Structure

```sql
CREATE TABLE IF NOT EXISTS trap_cashiers (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(50),
    job VARCHAR(50),
    coords LONGTEXT,
    heading FLOAT,
    prop VARCHAR(100)
);
```

---

## 🚀 Installation

1. Add the script folder to your `resources`.
2. Import the SQL table into your database.
3. Update your server config to start dependencies *before* this script.
4. Start the resource.

Example:

```
ensure oxmysql
ensure es_extended
ensure ox_lib
ensure ox_target
ensure TRAP_CashierCreator
```

---

## 🎯 Key Notes

* Player proximity detection is handled **server-side**, ensuring compatibility with OneSync and other production environments.
* Designed for **official servers** with optimized performance.
* Fully persistent: cashiers remain after restart, reconnect, or resource reload.

---

## 📌 Credits

Script by **TRAPZY**
**© TRAP Development**
Discord: [https://discord.gg/rjjU2y93X7](https://discord.gg/rjjU2y93X7)


