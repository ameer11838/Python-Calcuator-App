import tkinter as tk

def click(btn):
    if btn == "=":
        try:
            result = eval(entry.get())
            entry.delete(0, tk.END)
            entry.insert(tk.END, result)
        except:
            entry.delete(0, tk.END)
            entry.insert(tk.END, "Error")
    elif btn == "C":
        entry.delete(0, tk.END)
    else:
        entry.insert(tk.END, btn)

# Setup window
root = tk.Tk()
root.title("Calculator")

# Entry display
entry = tk.Entry(root, font=("Arial", 24), bd=10, justify="right")
entry.grid(row=0, column=0, columnspan=4)

# Buttons
buttons = [
    '7', '8', '9', '/',
    '4', '5', '6', '*',
    '1', '2', '3', '-',
    '0', '.', '=', '+',
    'C'
]

# Create and place buttons
row, col = 1, 0
for btn in buttons:
    tk.Button(root, text=btn, width=5, height=2, font=("Arial", 18),
              command=lambda b=btn: click(b)).grid(row=row, column=col, padx=5, pady=5)
    col += 1
    if col > 3:
        col = 0
        row += 1

root.mainloop()
