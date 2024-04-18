# Practice-Project-1---pdf-page-splitter
import pikepdf

old_pdf = pikepdf.Pdf.open("Policy_Certificate_49982828_25122023_policyPDF.pdf")

for n, page_can in enumerate(old_pdf.pages):
    new_pdf = pikepdf.Pdf.new()
    new_pdf.pages.append(page_can)
    name = "Policy_Certificate_49982828_25122023_policyPDF"+str(n+1)+".pdf"
    new_pdf.save(name)

print("Pdf Split done....!!!")
