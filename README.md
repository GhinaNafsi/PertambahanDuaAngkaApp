# PertambahanDuaAngkaApp
 Latihan  1-Ghina Nafsi-2210010324
# Deskripsi Program
*  memasukkan dua angka

* Saat tombol Tambah diklik akan menampilkan hasil pertambahan yang telah di masukan

* Saat tombol Hapus diklik akan menghapus nilai di TextField dan
mengarahkan fokus ke TextField angka pertama

# Komponen GUI: JFrame, JPanel, JLabel, JTextField, JButton
- JLabel untuk memberi label pada input angka pertama, angka kedua, dan hasil.
- JTextField untuk memasukkan angka pertama, angka kedua dan menampilkan hasil.
- JButton dengan label "Tambah" untuk melakukan operasi pertambahan.
- JButton dengan label "Hapus" untuk mengosongkan input.
- JButton dengan label "Keluar" untuk menutup aplikasi.

# Logika Program
Penambahan dua angka, validasi input numerik

# Events
-ActionListener untuk tombol Tambah, Hapus, dan Keluar
A.Tambah
 
   private void btnPlusActionPerformed(java.awt.event.ActionEvent evt) {                                        
    try{  
     int angka1 = Integer.parseInt(inputSatu.getText());
     int angka2 = Integer.parseInt(inputDua.getText());
     int hasil = angka1 + angka2;
     inputHasilTambah.setText("" + hasil); // Menampilkan hasil di jLabel3
     } catch (NumberFormatException e) {
         JOptionPane.showMessageDialog(this, "Masukkan angka yang valid!", "Error", JOptionPane.ERROR_MESSAGE);
     }
     }                                       
                 

B.Hapus
 
 private void deleteActionPerformed(java.awt.event.ActionEvent evt) {                                       
       inputSatu.setText("");
       inputDua.setText("");
       jLabel3.setText("Hasil: ");
       inputSatu.requestFocus(); // Mengarahkan fokus kembali ke jTextField1

   }   

C.Keluar
private void exitActionPerformed(java.awt.event.ActionEvent evt) {                                     
    System.exit(0);
 }  

# Variasi
A.KeyAdapter pada JTextField untuk membatasi input hanya angka

   private void inputSatuKeyTyped(java.awt.event.KeyEvent evt) {                                   
     char c = evt.getKeyChar();
     if (!Character.isDigit(c) && c != KeyEvent.VK_BACK_SPACE && c != KeyEvent.VK_DELETE) {
         evt.consume(); // Mencegah karakter non-numerik
         JOptionPane.showMessageDialog(this, "Masukkan hanya angka!", "Error", JOptionPane.ERROR_MESSAGE);
     }

   }                                  

   private void inputDuaKeyTyped(java.awt.event.KeyEvent evt) {                                  
     char c = evt.getKeyChar();
     if (!Character.isDigit(c) && c != KeyEvent.VK_BACK_SPACE && c != KeyEvent.VK_DELETE) {
         evt.consume(); // Mencegah karakter non-numerik
         JOptionPane.showMessageDialog(this, "Masukkan hanya angka!", "Error", JOptionPane.ERROR_MESSAGE);
     }

   }        

B.Gunakan JOptionPane untuk menampilkan error input

} catch (NumberFormatException e) {
        JOptionPane.showMessageDialog(this, "Masukkan hanya angka!", "Error", JOptionPane.ERROR_MESSAGE);
    }

C.Implementasikan FocusListener untuk membersihkan JTextField
saat mendapatkan fokus.

   private void inputSatuFocusGained(java.awt.event.FocusEvent evt) {                                      
     inputSatu.setText(""); // Menghapus teks saat mendapat fokus
     inputDua.setText(""); // Menghapus teks saat mendapat fokus
    }                                     

   private void inputSatuActionPerformed(java.awt.event.ActionEvent evt) {                                          
        // TODO add your handling code here:
   }  
    

# Hasil Gambar Project Ketika di Run
<img width="533" alt="PertambahanDuaAngka" src="https://github.com/user-attachments/assets/663331da-6edd-40b1-a2d4-822368249a1b">

## Indikator Penilaian:

| No  | Komponen         |  Persentase  |
| :-: | --------------   |   :-----:    |
|  1  | Komponen GUI     |    20    |
|  2  | Logika Program   |    20    |
|  3  | Events           |    15    |
|  4  | Kesesuaian UI    |    15    |
|  5  | Memenuhi Variasi |    30    |
|     | TOTAL        | 100 |

## Pembuat

NAMA : Ghina Nafsi
NPM : 2210010324
KELAS : 5A TI REG PAGI BJM
