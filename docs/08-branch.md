# 08. git branch

`git branch`, projedeki dalları (branch) yönetmenizi sağlar; var olan dalları listeler, yeni dal açar veya siler.

## Ne Zaman Kullanılır?
- Yeni bir özellik üzerinde çalışmak için ayrı bir dal açmak istediğinizde
- Mevcut dalları görmek veya gereksiz dalları temizlemek istediğinizde

## Kullanımı
```bash
git branch [seçenekler] [dal_adı]
```
- `git branch`: Tüm yerel dalları listeler
- `git branch -a`: Yerel ve uzak dalları bir arada gösterir
- `git branch -d dal_adı`: Belirtilen dalı siler
- `git branch -r`: Sadece uzak dalları listeler

## Örnekler
1. Yeni dal oluşturmak:
```bash
    git branch feature-yeni
```
2. Tüm dalları görmek:
   ```bash
git branch -a
```
3. Dal silmek:
   ```bash
git branch -d feature-yeni
```
4. Başka bir commit’ten dal açmak:
   ```bash
git branch acil-fix abc1234
```

## İpuçları
- Dal isimlerinde `feature/`, `bugfix/` gibi standart kullanarak düzen sağlayın
- Silmeden önce dalın birleştirildiğinden emin olun

---
_Bu komut, paralel geliştirmeyi kolaylaştırmak için vazgeçilmezdir._
