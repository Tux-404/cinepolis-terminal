# 🎬 Cinépolis Terminal — Cinema Management System

> A terminal-based cinema management system built in Python, featuring ASCII art UI, role-based access, seat management, and dynamic billboard control.

---

## 📌 About the Project

This was my **final project for my second year of vocational school in Cybersecurity** at Colegio Vocacional Monseñor Sanabria. It simulates a real cinema box office environment running entirely in the terminal.

The system handles two user roles — **administrators** and **customers** — with a fully interactive ASCII art interface for each movie on the billboard.

Originally prototyped in **PsInt** (a pseudocode learning tool) and ported to **Python**, with significant improvements added for the final submission.

---

## ✨ Features

- 🔐 **Role-based authentication** — Separate admin and customer access
- 🎭 **Dynamic billboard** — 7 movies with individual ASCII art, fully replaceable
- ✏️ **Admin panel with 4 functions:**
  - Modify movies (swap from a replacement list with matching art)
  - Add upcoming movies to a future schedule list
  - Remove movies from the active billboard
  - Enable/disable seats per cinema room
- 💺 **Seat management** — 7 rooms with 20 seats each, adjustable by admin
- 💰 **Ticket pricing** — Standard price + tax calculation built in
- 🔜 **Coming soon list** — Admins can queue upcoming releases
- 🛡️ **Error handling** — `try/except` block on main loop
- 🖥️ **Full ASCII art UI** — Custom Braille-style art for every movie

---

## 🛠️ Built With

- **Python 3**
- Standard library only — no external dependencies

---

## 🚀 How to Run

```bash
# Clone the repository
git clone https://github.com/Ed-404/cinepolis-terminal.git

# Navigate to the project folder
cd cinepolis-terminal

# Run the program
python taquillera.py
```

> ⚠️ Run with `python3` if needed. Terminal must support **UTF-8** encoding for the ASCII art to display correctly. On Windows, run: `chcp 65001` before launching.

---

## 🎮 How to Use

### Main Menu

| Option | Description |
|--------|-------------|
| `1` | Admin login |
| `2` | Customer login |
| `3` | New user registration |
| `4` | View full movie billboard |
| `5` | Exit |

**Admin credentials:**
- User: `Sysadmin`
- Password: `Cine1`

### Admin Panel

| Option | Description |
|--------|-------------|
| `1` | Modify a movie (swap with replacement list) |
| `2` | Add movies to upcoming schedule |
| `3` | Remove a movie from the billboard |
| `4` | Enable or disable seats per room |

---

## 🏗️ Project Structure

```
cinepolis-terminal/
│
├── taquillera.py       # Main program
└── README.md
```

### Key Variables

| Variable | Description |
|----------|-------------|
| `CARTELERA` | Active movie list (7 films) |
| `CARTELERA2` | Replacement movies available for swap |
| `CARTELERA3_PROX` | Upcoming movies queue |
| `Sala1–Sala7` | Seat count per room (default: 20 each) |
| `CompraE / CompraT` | Ticket prices (standard / with tax) |
| `Imagen0–Imagen6` | ASCII art assigned to each movie slot |

---

## 📚 What I Learned

- Designing and implementing role-based access control logic from scratch
- Managing parallel data structures (movie list + image list in sync)
- Terminal UI design using ASCII/Braille art
- Input validation and error handling with `try/except`
- Porting pseudocode logic (PsInt) into Python
- Working with lists: `append()`, `pop()`, index-based modification

---

## 🔮 Planned Improvements

- [ ] Refactor movie + image management into a dictionary or class
- [ ] Add a proper database backend (SQLite) for persistent data
- [ ] Implement hashed password authentication
- [ ] Build a GUI version with Tkinter or PyQt
- [ ] Add seat selection per movie showing
- [ ] Complete the customer login flow (currently incomplete)
- [ ] Fix admin auth bug: comparing against global `Passwd` instead of user input `password`

---

## 👤 Author

**Ed-404**
- GitHub: [@Ed-404](https://github.com/Ed-404)

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

*Final project — 2nd year Cybersecurity, Colegio Vocacional Monseñor Sanabria 🇨🇷*
*Part of my journey toward becoming a SOC Analyst and Red Teamer* 🔐
