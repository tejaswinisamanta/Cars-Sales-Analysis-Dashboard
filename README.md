# Cars-Sales-Analysis-Dashboard
import fitz # PyMuPDF

def pdf_to_markdown(pdf_path, output_path):
doc = fitz.open(pdf_path)
text = ""
for page in doc:
text += page.get_text()
with open(output_path, "w") as md_file:
md_file.write(text)

pdf_to_markdown("cars .pdf", "README.md")
