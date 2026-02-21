# ⚔️ Sudoku Duel

[![App Store](https://img.shields.io/badge/Download_on_the-App_Store-black?style=for-the-badge&logo=apple)]([BURAYA_APP_STORE_LINKIN_GELECEK])
[![Platform](https://img.shields.io/badge/Platform-iOS-lightgrey?style=for-the-badge)](#)

**Sudoku, but competitive.**  Sudoku Duel turns the classic logic puzzle into a fast, real-time multiplayer challenge. Face off against friends, solve the same Sudoku grid simultaneously, and win by thinking faster and making fewer mistakes.

> **Note: This repository serves as a showcase and architecture overview. The source code is not public.*

---

## 📱 Screenshots

<div align="center">
  <img src="[BURAYA_EKRAN_GORUNTUSU_LINKI_1]" width="250" alt="Home Screen">
  <img src="[BURAYA_EKRAN_GORUNTUSU_LINKI_2]" width="250" alt="Multiplayer Gameplay">
  <img src="[BURAYA_EKRAN_GORUNTUSU_LINKI_3]" width="250" alt="Victory Screen">
</div>

---

## Tech Stack

This project was built using a modern web-to-native architecture to ensure high performance and seamless real-time syncing:

* **Frontend:** React, TypeScript, Vite
* **Styling:** Tailwind CSS
* **Backend & Real-Time Sync:** Supabase (PostgreSQL, Realtime WebSockets)
* **Native Compilation (iOS):** Capacitor JS

---

## Key Features

* **Real-Time Battles:** Play head-to-head Sudoku matches with people you know using unique room codes.
* **Skill-Based Engine:** Both players receive identical, procedurally generated puzzles. No luck, just pure logic and speed.
* **Live Opponent Tracking:** See your opponent's progress in real-time as you play.
* **Privacy First:** No user accounts, emails, or personal data collected. Simply create a room and share the code.
* **Offline Solo Mode:** Practice your skills in a distraction-free single-player environment.

---

## ⚙️ How Multiplayer Works (Architecture Brief)

The core multiplayer experience relies on **Supabase Realtime**. 
1. **Room Creation:** Player 1 generates a session. The app creates a unique room entry in the Supabase database along with a seeded Sudoku puzzle.
2. **Connection:** Player 2 enters the 4-digit room code, fetching the exact same puzzle state.
3. **Synchronization:** Every valid move is pushed to the database and broadcasted instantly via WebSockets to the opponent's screen, ensuring a true head-to-head competitive feel.

---

## 👨‍💻 Developer

**Kaan Efe Taş**

*Computer Engineering Student @ İstanbul Bilgi University*
* [LinkedIn](https://www.linkedin.com/in/kaan-efe-tas/)
* [GitHub](https://github.com/kaant7)
