# hello-world
just another repository
"""python拆分工作簿，只要三行代码，比VBA简单"""
import pandas as pd
data=pd.read_excel(r"c:\python_excel\透视表.xlsx")
for i in data["商品名称"].unique():
    data[data["商品名称"]==i].to_excel(r"c:\python_excel\{}.xlsx".format(i),index=False)
    
