# Serverless Version Control (Single-File HTML)

This is a complete, local version control system that runs entirely within the web browser via a single HTML file.

The system is designed for teams or individuals who need version control functionality (inspired by Git) but work on **shared network drives** or in restricted environments where installing software is not possible.

It requires **no installation**, no server, and no database setup. It operates exclusively using the `FileSystem Access API` available in modern browsers.

## Key Features

* **No Installation Required:** It consists of a single `.html` file. Download it, place it in your project folder, and open it.
* **Linear History:** A simplified logic without branches or merges. It functions as a linear timeline, allowing you to restore the entire project or specific files to any previous state.
* **Visual Diff:** Includes a built-in difference viewer. Before taking a snapshot, you can compare modified files to see exactly which lines were added (green) or removed (red).
* **Collision Protection:** The system automatically detects if a colleague has saved a new snapshot to the shared drive while you were working. It prevents you from overwriting their history.
* **File Viewer:** View the content of historical text files directly in the browser without needing to restore them first.
* **Storage Efficiency:** Uses SHA-256 hashing to store files. Identical files are only stored once, saving disk space.
* **Garbage Collection:** Includes a "Prune Storage" function to permanently delete old file versions that are no longer referenced by any snapshot history.

## How to Get Started

1.  Download the `index.html` file.
2.  Place the file in the root of the folder you wish to version control.
3.  Double-click the file to open it in a compatible browser as Chrome or Vivaldi.
4.  Click the **Select Project Folder** button and grant read/write permission to the directory.
5.  You are now ready to track changes and take snapshots.

## AI Generation Notice

**This project code was 99% AI-generated.**

The code was developed through an iterative dialogue with **Google Gemini**. 

* **Language:** HTML5, CSS3, Vanilla JavaScript.
* **Dependencies:** None (No external libraries or CDNs).
* **Data Storage:** Uses the browser's `IndexedDB` for local settings and the local file system (`.version_repo` folder) for data persistence.

## Important Usage Notes

The system creates a hidden folder named `.version_repo` inside your project directory. This folder contains all historical data and metadata.

* **Do not delete** the `.version_repo` folder, or you will lose your version history.
* **Backup:** Since this tool manipulates files directly on your disk, it is recommended to keep a separate backup of critical data before initial use.

---

*License: MIT (Free to use and modify).*
