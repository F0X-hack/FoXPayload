<div align="center">
<img width="720" height="540" alt="ezgif-88076be499b62061" src="https://github.com/user-attachments/assets/bb754fd9-a29f-4f73-b273-d7e65920a07c" />

# FoXPayload

**Elegant CLI interface for [PayloadsAllTheThings](https://github.com/swisskyrepo/PayloadsAllTheThings)**

<img width="761" height="956" alt="image" src="https://github.com/user-attachments/assets/63ad6b04-d4ca-47c0-8e29-b70018991dec" />

*Browse, search and read PayloadsAllTheThings documentation directly from your terminal.*

</div>

---

## About

**FoXPayload** is a command-line tool that clones and indexes the [PayloadsAllTheThings](https://github.com/swisskyrepo/PayloadsAllTheThings) repository, letting you navigate its entire offensive security documentation without leaving your terminal. It features an interactive shell with syntax highlighting, full-text search and rich Markdown rendering.

---

## Features

- **Interactive mode** — Dedicated shell with command and category autocompletion (via `readline`)
- **Auto-fetch** — Clone or update the PayloadsAllTheThings repository in a single call
- **Local index** — Builds a JSON index for fast browsing and searching
- **Full-text search** — Find any technique across all categories instantly
- **Markdown rendering** — Formatted display with syntax highlighting for code blocks, headings, lists and tables
- **Statistics** — Overview of available categories and Intruder payload files
- **Polished UI** — Animated spinner, progress bar, Unicode borders, consistent color palette

---

## Requirements

- Python **3.8+**
- `git` installed and available in `PATH`
- Write access to `/usr/share/payloadsallthethings` (or edit the paths in the script)

---

## Installation

```sh
git clone https://github.com/F0X-hack/FoXPayload.git
cd FoXPayload
chmod +x setup.sh
./setup.sh
FoXPayload
```

---

## Usage

### Interactive mode (default)

```sh
FoXPayload
```

Launches an interactive shell with `<Tab>` autocompletion.

### Available commands

| Command | Description |
|---|---|
| `fetch` | Download or update the documentation |
| `list` | List all available categories |
| `search <term>` | Search across the entire documentation |
| `view <category>` | Display the content of a category |
| `stats` | Show global statistics |
| `clear` | Clear the screen |
| `help` | Show help |
| `exit` / `quit` | Quit |

### Non-interactive mode

```sh
# Download / update the documentation
FoXPayload fetch

# List categories
FoXPayload list

# Search for a term
FoXPayload search sqli

# View a category
FoXPayload view "SQL Injection"

# Show statistics
FoXPayload stats

# Force index rebuild
FoXPayload fetch --force
```

---

## Project structure

```
FoXPayload/
├── FoXPayload          # Main script
└── README.md

# Generated at runtime (not in the repository):
/usr/share/payloadsallthethings/
├── .payloads_repo/        # Cloned PayloadsAllTheThings repository
└── payloads_docs/
    ├── index.json         # Category index
    └── <Category>/
        ├── README.md
        └── Intruder/      # Wordlists for Burp Suite
```

---

## Credits

All documentation comes from the open-source project **[PayloadsAllTheThings](https://github.com/swisskyrepo/PayloadsAllTheThings)** maintained by [@swisskyrepo](https://github.com/swisskyrepo) and its contributors.

FoXPayload is only a local interface for that content — no payload is created or modified by this tool.

---

## Legal disclaimer

> This tool is intended for **educational purposes and authorized testing environments only.**  
> Using offensive security techniques against systems without explicit permission is illegal.  
> The author takes no responsibility for unethical or unlawful use.

---

<div align="center">

</div>
