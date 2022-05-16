pip install ethnicolr
from ethnicolr import pred_nc_reg_name
import openpyxl
def read_excel(filename, nrows):       
    book = openpyxl.load_workbook(filename=filename, read_only=True, data_only=True)
    first_sheet = book.worksheets[0]
    rows_generator = first_sheet.values

    header_row = next(rows_generator)
    data_rows = [row for (_, row) in zip(range(nrows - 1), rows_generator)]
    return pd.DataFrame(data_rows, columns=header_row)
	
df = read_excel(r'D:\projects\2022\hackathon\ethinicity\hackathon_flname.xlsx', nrows=59777)
odf = pred_nc_reg_name(df,"FirstName","LastName")
odf
odf.to_csv(r'D:\ajay\hackathon\ajay-out2-7600.csv', index=False)