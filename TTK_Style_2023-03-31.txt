from tkinter import ttk
import tkinter

GUI = tkinter.Tk()
GUI.geometry('200x200')
style = ttk.Style()

style.configure("T.TButton", 
    foreground='white', 
    background='black', 
    highlightthickness='20', 
    font=('Helvetica', 18, 'bold'))

style.map('T.TButton',
    foreground=[('disabled', 'yellow'),('pressed', 'red'),('active', 'blue')],
    background=[('disabled', 'magenta'),('pressed', '!focus', 'cyan'),('active', 'green')],
    highlightcolor=[('focus', 'green'),('!focus', 'red')],
    relief=[('pressed', 'groove'),('!pressed', 'ridge')])

btn_cred = ttk.Button(GUI, text= "Confirm", style= 'T.TButton')
btn_cred.place(x=50,y=50)  

GUI.mainloop()  