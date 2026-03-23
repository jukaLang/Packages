# 📦 Official List of Juka Packages

This repository contains the official list of **Juka Packages** that appear inside the Juka application.  
All packages are defined in **`Packages.json`**, which the Juka runtime reads to display and manage available packages.

---

## 🗂 Editing `Packages.json`

To add your own package, simply edit **`Packages.json`** and append a new entry following the structure below.

Each package entry must include:

- **name** – Display name of the package  
- **author** – Creator or maintainer  
- **description** – Short explanation of what the package does  
- **date** – Release date (`YYYY-MM-DD`)  
- **version** – Package version  
- **dependencies** – Array of required packages (or empty array)  
- **mainfilename** – The `.juk` file that serves as the entry point  
- **download** – URL to the package repository or download location  
- **device** – Supported devices (`"all"` or list of specific devices)

### ✅ Example Entry

```json
[
  {
    "name": "Example",
    "author": "Juka",
    "description": "An example of a Juka package",
    "date": "2024-07-22",
    "version": "1.0",
    "dependencies": [],
    "mainfilename": "example.juk",
    "download": "https://github.com/jukaLang/Example",
    "device": ["all"]
  }
]
```
