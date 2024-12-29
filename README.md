# Dice-Simulator
import tkinter as tk 
import random
window=tk.Tk()
window.title("dice simulator")
window.config(padx=100,pady=50,bg="pink")
canvas = tk.Canvas(window, width=100, height=100, bg="black")  
canvas.pack()
dice_img = tk.PhotoImage(file = "animated-dice-image-0005.gif")
canvas.create_image(50, 50, image = dice_img) 
def roll_dice():
    result=random.randint(1,6)
    result_label.config(text=f"🎲 You rolled a {result}!")
    print({result})
roll_button=tk.Button(window,text="click the dice",command =roll_dice)
roll_button.pack()
result_label=tk.Label( window,text="roll to see the result",font=("arial",24))
result_label.pack()
window.mainloop()

