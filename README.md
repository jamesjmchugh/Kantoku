# Kantoku 監督

**The first-generation human-less computer operator.**

Kantoku turns any old Android phone into an autonomous computer operator. Point it at your screen, and it becomes your computer's eyes, keyboard, and mouse — controlling your machine exactly like a human would.

## How It Works

```
┌─────────────┐         ┌─────────────┐
│   Phone     │ ──────> │  Computer   │
│  (Kantoku)  │  HID    │             │
│             │ ◀────── │             │
│  📷 Camera  │  sees   │   Screen    │
└─────────────┘         └─────────────┘
```

1. **See** — The phone's camera watches your computer screen
2. **Think** — Claude Vision AI analyzes what's on screen and decides what to do
3. **Act** — The phone sends keyboard/mouse commands over Bluetooth HID

No software installation on the target computer. No network connection required on the target. Just a phone pointed at a screen.

## Why Kantoku?

### 🔒 Airgapped Computers
Need to automate a machine that can't touch the internet? Kantoku operates entirely through physical I/O — camera in, Bluetooth HID out. The target computer needs zero modifications.

### 🚫 Can't Install Agents
Some computers are locked down, managed by IT, or running legacy systems where you can't install modern automation tools. Kantoku doesn't care — it works with any computer that has a screen and accepts a Bluetooth keyboard.

### ♻️ Use That Old Phone
That Android phone collecting dust in a drawer? It's now an autonomous operator. Give it a purpose.

## Requirements

- Android phone (Android 12+) with Bluetooth HID support
- Target computer with Bluetooth (or USB Bluetooth adapter)
- Phone holder/stand to point at screen
- Anthropic API key (for Claude Vision)

## Setup

1. Install Kantoku on your Android phone
2. Pair the phone with your target computer via Bluetooth
3. Enter your Anthropic API key
4. Position the phone to see the full screen
5. Describe your task and let it work

## Supported Actions

| Command | Description |
|---------|-------------|
| `KEY:enter` | Press a key |
| `KEY:cmd+space` | Key combinations |
| `TYPE:hello` | Type text |
| `CLICK:720,450` | Click at coordinates |
| `MOVE:100,-50` | Move mouse relatively |
| `WAIT` | Wait for something to load |
| `DONE` | Task complete |

## Example Tasks

- "Open Numbers and create a new spreadsheet"
- "Find the WiFi password in System Preferences"
- "Open Safari and search for today's weather"
- "Create a new folder on the desktop called Projects"

## Limitations

- Screen coordinate mapping from camera perspective isn't perfect yet
- Works best with stable phone positioning
- API calls cost money (currently using Claude Sonnet)
- 60-second intervals between actions to conserve API credits

## The Name

**Kantoku** (監督) is Japanese for "director" or "supervisor" — the one who watches and guides the action.

## Future Ideas

- [ ] On-device vision model (no API needed)
- [ ] Better coordinate calibration
- [ ] USB HID mode (no Bluetooth required)
- [ ] Multi-monitor support
- [ ] Action recording and playback

## License

MIT

---

*Built for the machines that can't be touched, by the phones that were forgotten.*
