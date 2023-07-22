# Habp2.first.project

from Bio import SeqIO

file_path = "C:/Users/busra/OneDrive/Masaüstü/protein.faa"

proteins = list(SeqIO.parse(file_path, "fasta"))

non_metionin_proteins = []
for protein in proteins:
    if protein.seq[0] != 'M':
        non_metionin_proteins.append(protein)
        
print(f"Toplam protein sayısı: {len(proteins)}")
print(f"M ile başlamayan protein sayısı: {len(non_metionin_proteins)}")

with open(file_path, "r") as file:
    file_contents = file.read()

# Verileri ekrana yazdırma
print(file_contents) 
