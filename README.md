Private Sub CommandButton1_Click()
Dim RealProperty As String
Dim Contents As String
Dim Calculator2 As Workbook

Worksheets("sheet1").Select
RealProperty = Range("B8")
Worksheets("sheet1").Select
Contents = Range("B9")

Set Calculator2 = Workbooks.Open("I:\Jon Doe\Rates\Postings.xlsx")
Worksheets("sheet1").Select
Worksheets("sheet1").Range("A1").Select
ColumnCounty = Worksheets("sheet1").Range("A1").CurrentRegion.Columns.Count
With Worksheets("sheet1").Range("A1")
.Offset(ColumnCount, 0) = RealProperty
.Offset(ColumnCount, 1) = Contents
End With
Calculator1.Save
End Sub
