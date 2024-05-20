print('WARUNG POJOK SARI')
print('---------------------------------')
print('1. Beras 4 kantong 45000/kantong')
print('2. Kopi 6 sachet 12000/kantong')
print('3. Kecap 5 sachet 10000/botol')
print('---------------------------------')
print('1. Penjualan')
print('2. Stock Barang')

def hitung_diskon(total):
    if total >= 200000:
        return total * 0.1  # Diskon 10% jika total lebih dari atau sama dengan 200000
    elif total >= 100000:
        return total * 0.05  # Diskon 5% jika total lebih dari atau sama dengan 100000
    else:
        return 0  # Tidak ada diskon jika total kurang dari 100000

pilihan = "po"
while pilihan == "po":
    pilieh = str(input('Kamu mau buka penjualan/stock barang?'))
    
    if pilieh == "penjualan":
        maka = str(input('Kamu mau jual barang apa?'))
        jumlah = int(input('Jumlahnya berapa?'))
        
        if maka == "beras":
            hasil = 45000 * jumlah
        elif maka == "kopi":
            hasil = 12000 * jumlah
        elif maka == "kecap":
            hasil = 10000 * jumlah
        else:
            hasil = 0
            print('Barang tidak ditemukan')
        
        if hasil > 0:
            diskon = hitung_diskon(hasil)
            total_bayar = hasil - diskon
            print(f'Total tanpa diskon Rp. {hasil}')
            print(f'Diskon Rp. {diskon}')
            print(f'Total setelah diskon Rp. {total_bayar}')
    
    elif pilieh == "stock":
        maka = str(input('Mau kamu kurang atau tambah dan barangnya apa? ex: tambah_beras: '))
        jumlah1 = int(input('Jumlahnya berapa?'))
        
        if maka == "tambah_beras":
            hasil = 4 + jumlah1
            print(f'Total {hasil} kantong')
        elif maka == "tambah_kopi":
            hasil = 6 + jumlah1
            print(f'Total {hasil} sachet')
        elif maka == "tambah_kecap":
            hasil = 5 + jumlah1
            print(f'Total {hasil} botol')
        elif maka == "kurang_beras":
            hasil = 4 - jumlah1
            print(f'Total {hasil} kantong')
        elif maka == "kurang_kopi":
            hasil = 6 - jumlah1
            print(f'Total {hasil} sachet')
        elif maka == "kurang_kecap":
            hasil = 5 - jumlah1
            print(f'Total {hasil} botol')
        else:
            print('Aksi atau barang tidak ditemukan')
    
    else:
        print('Pilihan tidak valid')
    
    pilihan = str(input('Apakah Anda ingin melanjutkan? (po untuk lanjut, lain untuk keluar): '))
print('-----------------------------')
