# 🛡️ Internet Positif Block Page (Svelte)

![Svelte](https://img.shields.io/badge/svelte-%23f1413d.svg?style=for-the-badge&logo=svelte&logoColor=white) ![Vite](https://img.shields.io/badge/vite-%23646CFF.svg?style=for-the-badge&logo=vite&logoColor=white)

A modern, responsive recreation of the Indonesian "Internet Positif" / Komdigi block page, built with **Svelte** and **Vite**.

## ✨ Features

- **📱 Responsive Design**:
  - **Mobile**: Stacked card layout for easy reading on small screens.
  - **Desktop**: Split-screen layout with a dedicated branding sidebar and content area.
- **🌙 Dark Mode Support**: Automatically detects system color scheme preferences (Light/Dark mode) and adjusts colors accordingly (Deep Dark/AMOLED Black for dark mode).
- **⚡ Dynamic Content**:
  - Automatically detects and displays the blocked domain name.
  - Displays current date and time (Indonesian locale).
  - Auto-updating copyright year.
- **🎨 Visuals**:
  - Professional UI with `lucide-svelte` icons.
  - Official branding colors (Red/White) adapted for modern aesthetics.
  - Custom "T+" shield logo.
- **⚖️ Legal Information**: Includes detailed references to UU ITE and Permenkominfo regulations.

## 🛠️ Tech Stack

- [Svelte](https://svelte.dev/) - Cybernetically enhanced web apps.
- [Vite](https://vitejs.dev/) - Next Generation Frontend Tooling.
- [Lucide Svelte](https://lucide.dev/guide/packages/lucide-svelte) - Beautiful & consistent icons.
- **CSS Variables** for flexible theming.

## 🚀 Setup & Run

1.  **📦 Install dependencies:**
    ```bash
    npm install
    ```

2.  **💻 Run development server:**
    ```bash
    npm run dev
    ```

3.  **🏗️ Build for production:**
    ```bash
    npm run build
    ```

## 📂 Project Structure

- `src/App.svelte`: Main application logic, layout, and styles.
- `public/`: Static assets (favicon, etc.).

## 📜 License

This project is for **educational and simulation purposes**.