import pandas as pd
data = {
     
    'date': [], 
    'category': [],                 
    'expense amount': [] ,
    'income amount': [],
    'type': []
}

df = pd.DataFrame(data)
filename = 'expensetracker.csv'
df.to_csv(filename, index=False)
print("""
Personal Expense Tracker
      1.Add Transaction
      2.Edit Transaction
      3.Delect Transaction
      4.View Summary
      5.Save and Exit
""")

choice = input("Enter your choice: ")
while choice != "5":
      if choice == "1" :      
            d = input("Enter the date (YYYY-MM-DD): ")
            c = input("Enter the categozy (e.g. Food,tansport): ")
            a = float(input("Enter the amount: "))
            t = input("Enter the type (Expense/Income): ")
            if t == "Expense" :
                  new_data = {
                  'date': 'd',
                  'categozy': 'c',
                  'expense amount': 'a',
                  'income amount': '0',
                  'type': 't'
                  }
            else :
                  new_data = {
                  'date': 'd',
                  'categozy':'c',
                  'expense amount': '0',
                  'income amount': 't'

                  }

            df.loc[len(df)] = new_data
            print("Transaction added successfuly")
            choice = input("Enter your choice: ")

      elif choice == "2" :
            print("Edit Transaction")
            print("""
Personal Expense Tracker
      1.Add Transaction
      2.Edit Transaction
      3.Delect Transaction
      4.View Summary
      5.Save and Exit
""")
            choice = input("Enter your choice: ")
      elif choice == "3":
          
          print("""
Personal Expense Tracker
      1.Add Transaction
      2.Edit Transaction
      3.Delect Transaction
      4.View Summary
      5.Save and Exit
""")
          choice = input("Enter your choice: ")
      elif choice == "4":
            total_expense = df['expense amount'].sum()
            total_income= df['income amount'].sum()
      

            print("""
---Expense Summary---
Total Expense: {total_expense}

---Income Summy---
Total Income: {total_income}
                  
Total Savings: 90

choice = input("Enter your choice: ")
""")
      else:
            print("Save and exit")


import pandas as pd
df = pd.DataFrame()






     



        
        
      