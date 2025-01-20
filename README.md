# digitalclock
#importing time for showing realtime
#importing tkinter for GUI
import tkinter as tk
from time import strftime

#root.title helps to set title
root = tk.Tk()
root.title("Digital Clock")

#def time defines time function
def time():
    string = strftime("%H:%M:%S %p \n %D")
    label.config(text=string)
    label.after(1000,time)

#below two lines code sets font style , size , weight , colour and background colour
label = tk.Label(root,font=("calibri",50,"bold"),background="yellow",foreground="black")
label.pack(anchor="center")

time()

root.mainloop()
