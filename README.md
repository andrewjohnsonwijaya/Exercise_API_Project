SOAL
1. Prevent Duplicate Email
   Tambahkan mekanisme pengecekan email pada saat create dan update user. Jika
   email sudah terdaftar sebelumnya, maka kembalikan error dengan status code 409
   (EMAIL_ALREADY_TAKEN).
2. Confirm Password
   Tambahkan input `password_confirm` yang perlu diisi pada saat create user
   baru. Konfirmasi password yang diisi ini harus sama dengan password yang diisi. Jika
   tidak sama, maka kembalikan error dengan status code 403 (INVALID PASSWORD).
3. Change Password
   Buatlah endpoint baru PATCH /users/{id}/change-password untuk
   mengubah password user. Input yang harus diisi adalah password lama, password
   baru, dan konfirmasi password baru. Adapun beberapa hal khusus yang perlu
   diperhatikan:
   - Password baru memiliki panjang 6 s/d 32 karakter.
   - Konfirmasi password baru harus sama dengan password baru.
   - Password lama harus sama dengan password saat ini.
