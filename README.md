import tkinter
from tkinter import messagebox,ttk
root =tkinter.Tk()
root.title("student information")
root.geometry("1920x1080")
root.configure(bg="#4D5C68")

# to show respone on clicking 

def onclick():
      name = student_name.get()
      email = student_email.get()
      phone = student_phonenumber.get()
      place = address.get()
      branch = dropdown.get()
      all_data = [name,phone,email,place]
      if name and email and phone and place and branch:
             
             student_phonenumber.delete(0,tkinter.END)
             address.delete(0,tkinter.END)
             student_email.delete(0,tkinter.END)
             student_name.delete(0,tkinter.END)  
             dropdown.delete(0,tkinter.END)
                  
      else:
             messagebox.showwarning("WARNING","PLEASE FILL ALL THE DATA")            
     #name

student_name1=tkinter.Label(root,text="STUDENT NAME",width=30,height=2)
student_name1.configure(fg="pink",bg="black",font="bold")
student_name1.pack(anchor="w",padx=10)
student_name=tkinter.Entry(root,width=80)
student_name.pack(anchor="w",padx=10)

#phone number

student_phonenumber1=tkinter.Label(root,text="  PHONE NUMBER ",width=30,height=2)
student_phonenumber1.configure(fg="pink",bg="black",font="bold" )
student_phonenumber1.pack(anchor="w",padx=10)
student_phonenumber=tkinter.Entry(root,width=80)
student_phonenumber.pack(anchor="w",padx=10)

#email

student_email1=tkinter.Label(root,text="  STUDENT EMAIL ",width=30,height=2)
student_email1.configure(fg="pink",bg="black",font="bold")
student_email1.pack(anchor="w",padx=10)
student_email=tkinter.Entry(root,width=80)
student_email.pack(anchor="w",padx=10)

#address

address1=tkinter.Label(root, text="address",width=30,height=2)
address1.configure(fg="pink",bg="black",font="bold")
address1.pack(anchor="w",padx=10)
address=tkinter.Entry(root,width=80)
address.pack(anchor="w",padx=10)

#dropdown

choice="computer science","comerce","hotel management"
entryy=tkinter.Label(root,text="select the branch",width=30)
entryy.pack(anchor=tkinter.W)
entryy.configure(bg="black",fg="pink")
dropdown=ttk.Combobox(root,values=choice,width="80")
dropdown.pack(anchor=tkinter.W)

#button 

button=tkinter.Button(root,text="submit",command=onclick)
button.configure(fg="pink",bg="grey",width=30,height=2)
button.pack(anchor="w",padx=10,pady=10)
root.mainloop()
