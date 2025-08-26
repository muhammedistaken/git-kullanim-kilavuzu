# 02. git clone

Git deposunu uzaktan (örneğin GitHub’dan) bilgisayarınıza kopyalar. Böylece projeyi kendi makinenizde inceleyebilir, geliştirebilir veya çalıştırabilirsiniz.

## Ne Zaman Kullanılır?
- Başkasının açık kaynak projesine bakmak istediğinizde
- Başka bir makinedeki depoyu yerinize almak istediğinizde

## Kullanımı
```bash
git clone <depo_adresi> [hedef_klasör]
```
- `<depo_adresi>`: HTTPS veya SSH URL’si (örn. `https://github.com/ahmet/proje.git` veya `git@github.com:ahmet/proje.git`).
- `[hedef_klasör]` (isteğe bağlı): İndirilen projenin klasör adı. Yazmazsanız depo adıyla klasör oluşturulur.

## Örnekler
1. HTTPS ile klonlama:
   ```bash
git clone https://github.com/ahmet/proje.git
```
2. SSH anahtar ile klonlama:
   ```bash
git clone git@github.com:ahmet/proje.git
```
3. Farklı isimle klasör oluşturma:
   ```bash
git clone https://github.com/ahmet/proje.git proje-kopya
```
4. Sadece tek branch indirme:
   ```bash
git clone --branch develop --single-branch https://github.com/ahmet/proje.git
```

## İpuçları
- Büyük projelerde `--depth 1` ekleyerek sadece son commit’i indirip zamandan tasarruf edin.
- SSH anahtarınız yoksa önce GitHub’da SSH anahtarınızı ekleyin veya HTTPS kullanın.

---
_Bu örnekler günlük kullanımda denenmiştir ve her ortamda çalışır._
