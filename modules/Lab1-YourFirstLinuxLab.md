Lab = Simulasi praktikum atau latihan langsung (biasanya berbentuk panduan interaktif atau sandbox belajar)  
# 1 Your First Linux Lab

- [x] 1. Hello World 
- [ ] 2. Displaying User and Group Information
- [ ] 3. Learn By Doing
- [ ] 4. Displaying the Current User
- [ ] 5. htop System Monitor

Latihan ini ada di daftar perintah terminal di https://github.com/corotdesain/mybelajar-linux/blob/master/modules/01-cli.md
Hello World di terminal
```bash
## Menampilkan Informasi Pengguna dan Grup
id
uid=5000(labex) gid=5000(labex) groups=5000(labex),27(sudo),121(ssl-cert),5002(public)
```
uid: Your User ID (a unique numerical identifier).  
gid: Your primary Group ID.  
groups: All the groups you are a member of.  
sudo singkatan dari:
“superuser do”
Yang artinya: 👉 Jalankan perintah sebagai superuser (admin/root)

```bash
## Kita juga bisa mengubah id pengguna untuk melihat pengguna lain yang ada (yang aktif/yang login)
id root
```
Selain melihat info user kamu sendiri, kamu bisa pakai id <nama_user> untuk melihat info user lain, seperti  
`id root`, `id ubuntu`, `id user123`, dll.



```
echo "Hello LabEx"
```
