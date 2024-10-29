from tkinter import *
window = Tk()

def tombol_klik(item):
    global ekspresi
    ekspresi = ekspresi + str(item)
    input_text.set(ekspresi)

def clear():
    global ekspresi
    ekspresi = ""
    input_text.set("")

def hasil():
    try:
        global ekspresi
        total = str(eval(ekspresi))
        input_text.set(total)
        ekspresi = total
    except:
        input_text.set("Error")
        ekspresi = ""

ekspresi = ""
input_text = StringVar()

frame = Frame(window, bg="Dark green", width=500, height=300)
frame.pack()

frame2 = Frame(window, bg="Black", width=500, height=300)
frame2.pack()

label = Label(frame, width=50, anchor="w", text="Kalkulator Zakky", font=("Times New Roman", 10))
label.pack(padx=20, pady=20)

label2 = Label(frame, width=50, anchor="e", textvariable=input_text, font=("Times New Roman", 20))
label2.pack(padx=20, pady=20)

Button(frame2, width=17, height=3, text="C", fg="white", bg="red", command=clear).grid(row=0, column=0, columnspan=2)

Button(frame2, width=6, height=3, text="/", bg="gray", command=lambda: tombol_klik("/")).grid(row=0, column=2, padx=10, pady=10)

Button(frame2, width=6, height=3, text="*", bg="gray", command=lambda: tombol_klik("*")).grid(row=0, column=3, padx=10, pady=10)

Button(frame2, width=6, height=3, text="+", bg="gray", command=lambda: tombol_klik("+")).grid(row=1, column=3, padx=10, pady=10)

Button(frame2, width=6, height=3, text="-", bg="gray", command=lambda: tombol_klik("-")).grid(row=2, column=3, padx=10, pady=10)

Button(frame2, width=6, height=7, text="=", bg="gray", command=hasil).grid(row=3, column=3, rowspan=2)

Button(frame2, text=".", width=6, height=3, command=lambda: tombol_klik(".")).grid(row=4, column=2, padx=10, pady=10)

Button(frame2, text="0", width=17, height=3, command=lambda: tombol_klik("0")).grid(row=4, column=0, columnspan=2)

Button(frame2, text="1", width=6, height=3,command=lambda: tombol_klik("1")).grid(row=3, column=0, padx=10, pady=10)

Button(frame2, text="2", width=6, height=3,command=lambda: tombol_klik("2")).grid(row=3, column=1, padx=10, pady=10)

Button(frame2, text="3", width=6, height=3,command=lambda: tombol_klik("3")).grid(row=3, column=2, padx=10, pady=10)

Button(frame2, text="4", width=6, height=3,command=lambda: tombol_klik("4")).grid(row=2, column=0, padx=10, pady=10)

Button(frame2, text="5", width=6, height=3,command=lambda: tombol_klik("5")).grid(row=2, column=1, padx=10, pady=10)

Button(frame2, text="6", width=6, height=3,command=lambda: tombol_klik("6")).grid(row=2, column=2, padx=10, pady=10)

Button(frame2, text="7", width=6, height=3,command=lambda: tombol_klik("7")).grid(row=1, column=0, padx=10, pady=10)

Button(frame2, text="8", width=6, height=3,command=lambda: tombol_klik("8")).grid(row=1, column=1, padx=10, pady=10)

Button(frame2, text="9", width=6, height=3,command=lambda: tombol_klik("9")).grid(row=1, column=2, padx=10, pady=10)

window.mainloop()

<!---
zakkchan/zakkchan is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
