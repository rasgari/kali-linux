# kali linux
این دستور را بزن:
```
sudo wget https://archive.kali.org/archive-key.asc -O /etc/apt/trusted.gpg.d/kali-archive-key.asc
```

این تقریباً همیشه یعنی لیست مخازن خراب شده.

باید sources را ریست کنیم 👇

✅ مخازن را تمیز و رسمی کن
```
sudo nano /etc/apt/sources.list
```

همه چیز داخل فایل را پاک کن و فقط این را بگذار:
```
deb http://http.kali.org/kali kali-rolling main contrib non-free non-free-firmware
```

Save → Exit  ===>>> ctrl + x ===>> Y

✅ حالا کش apt را پاک کن (خیلی مهم)
```
sudo apt clean
sudo rm -rf /var/lib/apt/lists/*
```
✅ آپدیت واقعی بزن
```
sudo apt update
```

نباید هیچ ERROR ببینی ❗

✅ بعدش Go را نصب کن
```
sudo apt install golang-go -y
```
⭐ نکته خیلی مهم (که اکثر افراد نمی‌دانند)

⚠️ وقتی دیدی:
```
1767 packages can be upgraded
```

یعنی سیستمت خیلی عقب افتاده 😄
بهتر است یک بار این را هم بزنی:
```
sudo apt full-upgrade -y
```

(ممکن است 15–40 دقیقه طول بکشد ولی Kali را نجات می‌دهد.)
