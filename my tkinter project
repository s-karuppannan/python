from tkinter import *
import random

from tkinter import messagebox
class Bill_App:
    def _init_(self,root):
        self.root=root
        self.root.geometry("1350x700+0+0")
        self.root.configure(bg="#5B2C6F")
        self.root.title("fresh juice Billing Software")
        title=Label(self.root,text="fresh juice Billing System",bd=12,relief=RIDGE,font=("Arial Black",20),bg="#A569BD",fg="white").pack(fill=X)
        #===================================variables=======================================================================================
        self.apple=IntVar()
        self.mango=IntVar()
        self.orange=IntVar()
        self.banana=IntVar()
        self.pineapple=IntVar()
        self.lemon=IntVar()
        self.strawberry=IntVar()
        
        self.total_jui=StringVar()
        
        self.a=StringVar()
        
        self.c_name=StringVar()
        self.bill_no=StringVar()
        x=random.randint(1000,9999)
        self.bill_no.set(str(x))
        self.phone=StringVar()
        #==========================================customer details label frame=================================================
        details=LabelFrame(self.root,text="Customer Details",font=("Arial Black",12),bg="#A569BD",fg="white",relief=GROOVE,bd=10)
        details.place(x=0,y=80,relwidth=1)
        cust_name=Label(details,text="Customer Name",font=("Arial Black",14),bg="#A569BD",fg="white").grid(row=0,column=0,padx=15)

        cust_entry=Entry(details,borderwidth=4,width=30,textvariable=self.c_name).grid(row=0,column=1,padx=8)

        contact_name=Label(details,text="Contact No.",font=("Arial Black",14),bg="#A569BD",fg="white").grid(row=0,column=2,padx=10)

        contact_entry=Entry(details,borderwidth=4,width=30,textvariable=self.phone).grid(row=0,column=3,padx=8)

        bill_name=Label(details,text="Bill.No.",font=("Arial Black",14),bg="#A569BD",fg="white").grid(row=0,column=4,padx=10)

        bill_entry=Entry(details,borderwidth=4,width=30,textvariable=self.bill_no).grid(row=0,column=5,padx=8)
        #=======================================fresh juice label frame=================================================================
        juice=LabelFrame(self.root,text="Fresh juice",font=("Arial Black",12),bg="#E5B4F3",fg="#6C3483",relief=GROOVE,bd=10)
        juice.place(x=5,y=180,height=380,width=1000)

        item1=Label(juice,text="apple juice(40Rs)",font=("Arial Black",11),bg="#E5B4F3",fg="#6C3483").grid(row=0,column=0,pady=11)
        item1_entry=Entry(juice,borderwidth=2,width=15,textvariable=self.apple).grid(row=0,column=1,padx=10)

        item2=Label(juice,text="mango juice(20Rs)",font=("Arial Black",11),bg="#E5B4F3",fg="#6C3483").grid(row=1,column=0,pady=11)
        item2_entry=Entry(juice,borderwidth=2,width=15,textvariable=self.mango).grid(row=1,column=1,padx=10)

        item3=Label(juice,text="orange juice(30Rs)",font=("Arial Black",11),bg="#E5B4F3",fg="#6C3483").grid(row=2,column=0,pady=11)
        item3_entry=Entry(juice,borderwidth=2,width=15,textvariable=self.orange).grid(row=2,column=1,padx=10)

        item4=Label(juice,text="banana juice(20Rs)",font=("Arial Black",11),bg="#E5B4F3",fg="#6C3483").grid(row=3,column=0,pady=11)
        item4_entry=Entry(juice,borderwidth=2,width=15,textvariable=self.banana).grid(row=3,column=1,padx=10)

        item5=Label(juice,text="pineapple juice(40Rs)",font=("Arial Black",11),bg="#E5B4F3",fg="#6C3483").grid(row=4,column=0,pady=11)
        item5_entry=Entry(juice,borderwidth=2,width=15,textvariable=self.pineapple).grid(row=4,column=1,padx=10)

        item6=Label(juice,text="lemon juice(20Rs)",font=("Arial Black",11),bg="#E5B4F3",fg="#6C3483").grid(row=5,column=0,pady=11)
        item6_entry=Entry(juice,borderwidth=2,width=15,textvariable=self.lemon).grid(row=5,column=1,padx=10)

        item7=Label(juice,text="strawberry juice(60Rs)",font=("Arial Black",11),bg="#E5B4F3",fg="#6C3483").grid(row=6,column=0,pady=11)
        item7_entry=Entry(juice,borderwidth=2,width=15,textvariable=self.strawberry).grid(row=6,column=1,padx=10)
        #=====================================================billarea==============================================================================
        billarea=Frame(self.root,bd=10,relief=GROOVE,bg="#E5B4F3")
        billarea.place(x=1010,y=188,width=330,height=372)

        bill_title=Label(billarea,text="Bill Area",font=("Arial Black",17),bd=7,relief=GROOVE,bg="#E5B4F3",fg="#6C3483").pack(fill=X)

        scrol_y=Scrollbar(billarea,orient=VERTICAL)
        self.txtarea=Text(billarea,yscrollcommand=scrol_y.set)
        scrol_y.pack(side=RIGHT,fill=Y)
        scrol_y.config(command=self.txtarea.yview)
        self.txtarea.pack(fill=BOTH,expand=1)
        #=================================================billing menu=========================================================================================
        billing_menu=LabelFrame(self.root,text="Billing Summery",font=("Arial Black",12),relief=GROOVE,bd=10,bg="#A569BD",fg="white")
        billing_menu.place(x=0,y=560,relwidth=1,height=137)

        total_juice=Label(billing_menu,text="Total juice Price",font=("Arial Black",11),bg="#A569BD",fg="white").grid(row=0,column=0)
        total_juice_entry=Entry(billing_menu,width=30,borderwidth=2,textvariable=self.total_jui).grid(row=0,column=1,padx=10,pady=7)

        
        tax_juice=Label(billing_menu,text="juice Tax",font=("Arial Black",11),bg="#A569BD",fg="white").grid(row=0,column=2)
        tax_juice_entry=Entry(billing_menu,width=30,borderwidth=2,textvariable=self.a).grid(row=0,column=3,padx=10,pady=7)

       
        button_frame=Frame(billing_menu,bd=7,relief=GROOVE,bg="#6C3483")
        button_frame.place(x=830,width=500,height=95)

        button_total=Button(button_frame,text="Total Bill",font=("Arial Black",15),pady=10,bg="#E5B4F3",fg="#6C3483",command=lambda:total(self)).grid(row=0,column=0,padx=12)
        button_clear=Button(button_frame,text="Clear Field",font=("Arial Black",15),pady=10,bg="#E5B4F3",fg="#6C3483",command=lambda:clear(self)).grid(row=0,column=1,padx=10,pady=6)
        button_exit=Button(button_frame,text="Exit",font=("Arial Black",15),pady=10,bg="#E5B4F3",fg="#6C3483",width=8,command=lambda:exit1(self)).grid(row=0,column=2,padx=10,pady=6)
        intro(self)


def total(self):
    if (self.c_name.get=="" or self.phone.get()==""):
        messagebox.showerror("Error", "Fill the complete Customer Details!!")
    self.ap=self.apple.get()*40
    self.ma=self.mango.get()*20
    self.ora=self.orange.get()*30
    self.ba=self.banana.get()*20
    self.pi=self.pineapple.get()*40
    self.le=self.lemon.get()*20
    self.st=self.strawberry.get()*60
    total_juice_price=(
                self.ap+
                self.ma+
                self.ora+
                self.ba+
                self.pi+
                self.le+
                self.st)
    self.total_jui.set(str(total_juice_price)+" Rs")
    self.a.set(str(round(total_juice_price*0.05,3))+" Rs")

   


    
  
    self.total_all_bill=(total_juice_price+  (round(total_juice_price*0.05,3)))
    self.total_all_bil=str(self.total_all_bill)+" Rs"
    billarea(self)
def intro(self):
    self.txtarea.delete(1.0,END)
    self.txtarea.insert(END,"\tWELCOME TO SUPER MARKET\n\tPhone-No.739275410")
    self.txtarea.insert(END,f"\n\nBill no. : {self.bill_no.get()}")
    self.txtarea.insert(END,f"\nCustomer Name : {self.c_name.get()}")
    self.txtarea.insert(END,f"\nPhone No. : {self.phone.get()}")
    self.txtarea.insert(END,"\n====================================\n")
    self.txtarea.insert(END,"\nProduct\t\tQty\tPrice\n")
    self.txtarea.insert(END,"\n====================================\n")
def billarea(self):
    intro(self)
    if self.apple.get()!=0:
        self.txtarea.insert(END,f"apple\t\t {self.apple.get()}\t{self.ap}\n")
    if self.mango.get()!=0:
        self.txtarea.insert(END,f"mango\t\t {self.mango.get()}\t{self.ma}\n")
    if self.orange.get()!=0:
        self.txtarea.insert(END,f"orange\t\t {self.orange.get()}\t{self.ora}\n")
    if self.banana.get()!=0:
        self.txtarea.insert(END,f"banana\t\t {self.banana.get()}\t{self.ba}\n")
    if self.pineapple.get()!=0:
        self.txtarea.insert(END,f"pineapple\t\t {self.pineapple.get()}\t{self.pi}\n")
    if self.lemon.get()!=0:
        self.txtarea.insert(END,f"lemon\t\t {self.lemon.get()}\t{self.le}\n")
    if self.strawberry.get()!=0:
        self.txtarea.insert(END,f"strawberry\t\t {self.strawberry.get()}\t{self.st}\n")
    

    self.txtarea.insert(END,f"------------------------------------\n")
    if self.a.get()!="0.0 Rs":
        self.txtarea.insert(END,f"Total juice Tax : {self.a.get()}\n")
   
    self.txtarea.insert(END,f"Total Bill Amount : {self.total_all_bil}\n")
    self.txtarea.insert(END,f"------------------------------------\n")
def clear(self):
        self.txtarea.delete(1.0,END)
        self.apple.set(0)
        self.mango.set(0)
        self.orange.set(0)
        self.banana.set(0)
        self.pineapple.set(0)
        self.lemon.set(0)
        self.strawberry.set(0)
        
        self.total_jui.set(0)
     
        self.a.set(0)
        self.b.set(0)
        self.c.set(0)
        self.c_name.set(0)
        self.bill_no.set(0)
        self.bill_no.set(0)
        self.phone.set(0)
def exit1(self):
    self.root.destroy()

root=Tk()
obj=Bill_App(root)
root.mainloop()
