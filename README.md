# 🏏 Hand Cricket (Python Edition)

Welcome to **Hand Cricket** – the digital revival of the legendary school-time game, coded in Python!  
Right now, this repository contains the **Toss phase**, with more exciting innings to come!

---

## 🎮 What’s in the game so far?

Right now, we’ve coded the **Toss**—because every epic match needs a proper start!

### ⚙️ Toss Logic:
- User picks **odd** or **even**
- Both player and computer choose a number between **1 and 6**
- Their sum decides the result
- Whoever wins the toss gets to **choose to bat or bowl first** (or the computer chooses randomly if it wins)

---

## 🧠 How it Works (Code Summary):

```python
from random import *

user_choice = input("odd or even ? ")
user_toss = int(input("Enter a number for the toss : "))

if user_toss < 1 or user_toss > 6:
    print("Invalid input , HANG IN THE FAN ")
else:
    comp_toss = randint(1, 6)
    toss = user_toss + comp_toss
    result = "even" if toss % 2 == 0 else "odd"

    if user_choice == result:
        print("You won the toss")
        choice = input("batting OR bowling ? ")
    else:
        print("Computer won the toss")
        choices = ["batting", "bowling"]
        choice = choice(choices)  # ⚠️ Bug here (see below)

    print(f"You are {choice}")
````
---

## 🚧 Future Plans

* 🏏 Full batting and bowling logic
* 🔢 Scoring system
* 🧠 AI-like responses for the computer
* 🎨 Optional GUI (maybe… if we’re feeling spicy 🌶️)

---

## 📦 How to Run

1. Make sure you have **Python 3** installed.
2. Clone the repo:

   ```bash
   git clone https://github.com/your-username/hand-cricket.git
   cd hand-cricket
   ```
3. Run the script:

   ```bash
   python hand_cricket.py
   ```

---

## 🤝 Contributions

Pull requests are welcome! Got a cool idea? Wanna fix a bug? Fork it, code it, and drop a PR.

---

## 📜 License

MIT License – do what you want, just don’t blame me if the computer keeps winning the toss.

---

## 👑 Author

Made with fingers and fury by **Faulty-Devil37**.
May the sixes be ever in your favor. 🏏🔥

