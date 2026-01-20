You’re asking exactly the right question, because **Phase 0 looks huge**, but the actual required implementation is very specific. Based on the page you opened, here is the precise list of what you must implement.

---

# 🧩 What You *Actually* Need to Implement in Phase 0

Everything you write goes in the **shared** module under  
`shared/src/main/java/chess`.

The assignment gives you several classes with empty methods that currently throw exceptions. **Your job is to fully implement those classes so the pass‑off tests succeed.**

Below is the exact checklist.

---

# 1. **ChessPosition**
You must implement:
- Fields for **row** (1–8) and **column** (1–8)
- Constructor
- Getters
- `equals()` and `hashCode()`  
- `toString()` (optional but helpful)

This class is simple: it just represents a square like (2, 5).

---

# 2. **ChessMove**
You must implement:
- Fields:
  - start position
  - end position
  - optional promotion piece type
- Constructor
- Getters
- `equals()` and `hashCode()`

This is also straightforward: it’s just a data container.

---

# 3. **ChessPiece**
This is the **core** of Phase 0.

You must implement:
- Fields:
  - team color
  - piece type (KING, QUEEN, etc.)
- Constructor
- Getters
- `equals()` and `hashCode()`
- **pieceMoves(ChessBoard board, ChessPosition position)**  
  This is the big one.

### pieceMoves must:
- Return *all* legal moves for that piece **ignoring check, turn order, and checkmate**
- Respect:
  - board boundaries
  - blocking by friendly pieces
  - capturing enemy pieces
  - each piece’s movement rules:
    - Pawn: forward moves, diagonal captures, first‑move double step, promotion
    - Rook: straight lines until blocked
    - Bishop: diagonals until blocked
    - Queen: rook + bishop
    - Knight: L‑shape jumps
    - King: one square in any direction

This is where 90% of your logic goes.

---

# 4. **ChessBoard**
You must implement:
- Internal board representation (2D array, map, whatever you choose)
- `addPiece(position, piece)`
- `getPiece(position)`
- `resetBoard()`  
  → Must set up the standard chess starting position
- `equals()` and `hashCode()`

The board must correctly store and retrieve pieces so `pieceMoves` can work.

---

# 5. **ChessGame**
The page explicitly says:

> “Although the ChessGame class is presented now, it will not be used until Phase 1.”

So for Phase 0:
- You do **not** implement game logic
- You do **not** implement turn order
- You do **not** implement check/checkmate

Just leave the class as-is.

---

# 🧪 6. Pass‑off Tests
The tests in `src/test/java/passoff/chess` check:
- Each piece’s movement rules
- Board setup
- Correct equals/hashCode behavior

If your movement logic is correct, the tests will pass.

---

# ✔️ Summary: Your Phase 0 To‑Do List

| Class | What to Implement |
|-------|-------------------|
| **ChessPosition** | fields, constructor, getters, equals/hashCode |
| **ChessMove** | fields, constructor, getters, equals/hashCode |
| **ChessPiece** | fields, constructor, getters, equals/hashCode, **pieceMoves** (full movement logic) |
| **ChessBoard** | board storage, add/remove/get, **resetBoard**, equals/hashCode |
| **ChessGame** | nothing for Phase 0 |

---

If you want, I can walk you through **how to structure pieceMoves**, or help you design the board representation so movement logic becomes easier.
