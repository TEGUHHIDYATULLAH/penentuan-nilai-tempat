print("=== Aplikasi Penentuan Nilai Tempat Bilangan ===")

# --- VALIDASI INPUT ---
while True:
    angka_input = input("Masukkan bilangan (tanpa spasi & tanda): ")

    if not angka_input.isdigit():
        print("Input tidak valid! Harus berupa angka. Coba lagi.\n")
    else:
        break

# --- DAFTAR NILAI TEMPAT (hingga milyar) ---
nilai_tempat = [
    "satuan",
    "puluhan",
    "ratusan",
    "ribuan",
    "puluh ribu",
    "ratus ribu",
    "jutaan",
    "puluh juta",
    "ratus juta",
    "milyar",
    "puluh milyar",
    "ratus milyar"
]

print("\nHasil penentuan nilai tempat:\n")

# Membalik angka supaya index ke-0 adalah satuan
angka_terbalik = angka_input[::-1]

# --- PROSES DIGIT ---
for i in range(len(angka_terbalik)):
    digit = angka_terbalik[i]

    if digit != "0":  # hanya tampilkan jika bukan nol
        print(f"{digit} = {digit} {nilai_tempat[i]}")

print("\n=== Selesai ===")

