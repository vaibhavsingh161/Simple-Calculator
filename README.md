# Simple-Calculator
I have made a simple calculator using python programming.

import tkinter as tk

def button_click(number):
    current = display.get()
    display.delete(0, tk.END)
    display.insert(tk.END, current + str(number))

def button_clear():
    display.delete(0, tk.END)

def button_equal():
    expression = display.get()
    result = eval(expression)
    display.delete(0, tk.END)
    display.insert(tk.END, result)

# Create the main window
window = tk.Tk()
window.title("Calculator")

# Create the display
display = tk.Entry(window, width=20, font=("Arial", 16))
display.grid(row=0, column=0, columnspan=4, padx=10, pady=10)

# Create the number buttons
button_1 = tk.Button(window, text="1", padx=10, pady=5, command=lambda: button_click(1))
button_2 = tk.Button(window, text="2", padx=10, pady=5, command=lambda: button_click(2))
button_3 = tk.Button(window, text="3", padx=10, pady=5, command=lambda: button_click(3))
button_4 = tk.Button(window, text="4", padx=10, pady=5, command=lambda: button_click(4))
button_5 = tk.Button(window, text="5", padx=10, pady=5, command=lambda: button_click(5))
button_6 = tk.Button(window, text="6", padx=10, pady=5, command=lambda: button_click(6))
button_7 = tk.Button(window, text="7", padx=10, pady=5, command=lambda: button_click(7))
button_8 = tk.Button(window, text="8", padx=10, pady=5, command=lambda: button_click(8))
button_9 = tk.Button(window, text="9", padx=10, pady=5, command=lambda: button_click(9))
button_0 = tk.Button(window, text="0", padx=10, pady=5, command=lambda: button_click(0))

button_1.grid(row=1, column=0)
button_2.grid(row=1, column=1)
button_3.grid(row=1, column=2)
button_4.grid(row=2, column=0)
button_5.grid(row=2, column=1)
button_6.grid(row=2, column=2)
button_7.grid(row=3, column=0)
button_8.grid(row=3, column=1)
button_9.grid(row=3, column=2)
button_0.grid(row=4, column=0)

# Create the operator buttons
button_add = tk.Button(window, text="+", padx=10, pady=5, command=lambda: button_click('+'))
button_subtract = tk.Button(window, text="-", padx=10, pady=5, command=lambda: button_click('-'))
button_multiply = tk.Button(window, text="*", padx=10, pady=5, command=lambda: button_click('*'))
button_divide = tk.Button(window, text="/", padx=10, pady=5, command=lambda: button_click('/'))

button_add.grid(row=1, column=3)
button_subtract.grid(row=2, column=3)
button_multiply.grid(row=3, column=3)
button_divide.grid(row=4, column=3)

# Create the clear and equal buttons
button_clear = tk.Button(window, text="C", padx=10, pady=5, command=button_clear)
button_equal = tk.Button(window, text="=", padx=10, pady=5, command=button_equal)

button_clear.grid(row=4, column=1)
button_equal.grid(row=4, column=2)

# Start the main loop
window.mainloop()
