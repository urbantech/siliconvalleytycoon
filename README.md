---
# **Silicon Valley TyCoon**
---

Silicon Valley TyCoon is an educational and entertaining clicker tycoon game that simulates the journey of a Silicon Valley entrepreneur. This project combines game mechanics built in Roblox Studio with a robust backend for managing game data and analytics, adhering to Test-Driven Development (TDD) and Behavior-Driven Development (BDD) practices.

## **Table of Contents**

1. [Project Overview](#project-overview)
2. [Technologies Used](#technologies-used)
3. [Features](#features)
4. [Installation](#installation)
5. [Usage](#usage)
6. [File Structure](#file-structure)
7. [API Documentation](#api-documentation)
8. [Testing](#testing)
9. [License](#license)

---

## **Project Overview**

**Silicon Valley TyCoon** gamifies the startup journey, allowing players to progress through stages such as bootstrapping in a garage, scaling their startup, and becoming a unicorn. The game encourages creativity by enabling community developers to create add-ons and extensions.

- **Core Game Mechanics**: Built in Lua on Roblox Studio.
- **Tycoon API**: Node.js API for managing player data, upgrades, and products.
- **Analytics API**: Python-based API for tracking player behavior and generating reports.

---

## **Technologies Used**

### **Frontend/Game**
- **Roblox Studio**: Game development platform.
- **Lua**: Scripting language for in-game mechanics.

### **Backend**
- **Node.js**: Server-side JavaScript runtime.
- **Express.js**: Framework for building the Tycoon API.
- **MongoDB**: Database for storing player and game data.

### **Analytics**
- **Python**: Backend for Analytics API.
- **Flask**: Lightweight web framework.
- **Pandas**: Data analysis library for metrics and reports.

### **Testing**
- **Jest**: Unit and integration testing for Node.js.
- **unittest**: Testing framework for Python.
- **Roblox TestService**: In-game testing for Lua scripts.

### **Deployment**
- **Digital Ocean**: Hosting for APIs.

---

## **Features**

### **Core Features**
- **Clicker Mechanic**: Players earn funding by clicking.
- **Startup Progression**: Players upgrade their office, hire employees, and launch products.
- **Dynamic Upgrades**: Customizable boosts for income and efficiency.
- **Community Add-ons**: API support for developer extensions.

### **Analytics Features**
- **Player Metrics**: Track clicks, upgrades, and game progression.
- **Reports**: Generate summaries of player behavior.

### **Developer Tools**
- **Tycoon API**: Create upgrades, products, and events.
- **In-Game Integration**: Real-time communication with APIs.

---

## **Installation**

### **Prerequisites**
- [Node.js](https://nodejs.org/) (v14+)
- [Python](https://www.python.org/) (v3.8+)
- [MongoDB](https://www.mongodb.com/)
- [Roblox Studio](https://www.roblox.com/create)

### **Step 1: Clone the Repository**
```bash
git clone https://github.com/yourusername/silicon_valley_tycoon.git
cd silicon_valley_tycoon
```

### **Step 2: Install Dependencies**
#### Backend (Node.js)
```bash
cd backend/tycoon_api
npm install
cd ../analytics_api
pip install -r requirements.txt
```

#### Roblox
- Open `silicon_valley_tycoon/roblox` in Roblox Studio.
- Import the scripts and assets.

### **Step 3: Set Up the Database**
```bash
mongo
use silicon_valley_tycoon
db.createCollection("players")
db.createCollection("upgrades")
db.createCollection("products")
```

### **Step 4: Start the Servers**
#### Tycoon API
```bash
cd backend/tycoon_api
node index.js
```

#### Analytics API
```bash
cd backend/analytics_api
python app.py
```

---

## **Usage**

### **Run the Game**
1. Open the Roblox project in Roblox Studio.
2. Play the game locally to test mechanics.

### **API Endpoints**
- Tycoon API: `http://localhost:3000`
- Analytics API: `http://localhost:5000`

---

## **File Structure**

```
silicon_valley_tycoon
├── backend
│   ├── tycoon_api
│   │   ├── controllers
│   │   ├── models
│   │   ├── routes
│   │   ├── test
│   │   └── index.js
│   ├── analytics_api
│   │   ├── controllers
│   │   ├── models
│   │   ├── routes
│   │   ├── test
│   │   └── app.py
│   └── db
├── roblox
│   ├── scripts
│   │   ├── ClickerScript.lua
│   │   └── ClickerTest.lua
│   └── assets
└── README.md
```

---

## **API Documentation**

### **Tycoon API**
#### **Player Endpoints**
- `GET /players`: Retrieve all players.
- `POST /players`: Create a new player.

#### **Upgrade Endpoints**
- `GET /upgrades`: Retrieve all upgrades.
- `POST /upgrades`: Create a new upgrade.

### **Analytics API**
#### **Metrics Endpoints**
- `POST /metrics`: Log player metrics.
- `GET /metrics/report`: Generate a summary report.

---

## **Testing**

### **Node.js Tests**
Run tests for the Tycoon API:
```bash
cd backend/tycoon_api
npx jest
```

### **Python Tests**
Run tests for the Analytics API:
```bash
cd backend/analytics_api
python -m unittest discover
```

### **Roblox Tests**
Use **TestService** in Roblox Studio to validate Lua scripts.

---

## **License**

This project is licensed under the [MIT License](LICENSE).

---
