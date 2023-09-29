import tkinter as tk
from tkinter import messagebox

def add_task():
    task = entry.get()
    if task:
        listbox.insert(tk.END, task)
        entry.delete(0, tk.END)
    else:
        messagebox.showwarning("Warning","Please enter a task!")

def delete_task():
    try:
        index = listbox.curselection()[0]
        listbox.delete(index)
    except IndexError:
        messagebox.showwarning("Warning","Please select a task to delete!")

def update_task():
    try:
        index = listbox.curselection()[0]
        updated_task = entry.get()
        if update_task:
            listbox.delete(index)
            listbox.insert(index,updated_task)
            entry.delete(0,tk.END)
        else:
            messagebox.showwarning("Warning","Please enter an updated task!")
    except IndexError:
        messagebox.showwarning("Warning","please select a task to update!")


root = tk.Tk()
root.title("to do list")

listbox = tk.Listbox(root,width=50)
listbox.pack(pady=10)

entry=tk.Entry(root, width=40)
entry.pack(pady=10)

add_button=tk.Button(root, text="add task",command=add_task)
add_button.pack(side=tk.LEFT, padx=10)
update_button=tk.Button(root, text="update task",command=update_task)
update_button.pack(side=tk.LEFT, padx=10)
delete_button=tk.Button(root, text="Delete task",command=delete_task)
delete_button.pack(side=tk.LEFT, padx=10)

root.mainloop()
