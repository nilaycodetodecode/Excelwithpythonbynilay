# Excelwithpythonbynilay
import pandas as pd

# Read the Excel file into a DataFrame
df = pd.read_excel(r"C:\Users\bnila\Downloads\task_.xlsx")

# Print the DataFrame
print(df)
df.rename(columns={"ERP USER ID": "t_user", "PROJECT": "t_cpry", "DICIPLINE": "t_htyp", "REMARKS": "t_rema", "DATE": "t_date","START TIME": "t_fsts", "END TIME": "t_nstp"}, inplace= True)
df.to_excel(r"C:\Users\bnila\Downloads\task_niloy.xlsx", index=False)
print(df.columns)
# Ensure columns are in datetime format
df['t_fsts'] = pd.to_datetime(df['t_fsts'])
df['t_nstp'] = pd.to_datetime(df['t_nstp'])
df.to_excel(r"C:\Users\bnila\Downloads\task_niloy.xlsx", index=False)
print(df.columns)
