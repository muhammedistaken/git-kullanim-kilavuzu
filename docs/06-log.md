# 06. git log

`git log` komutu, proj## İpuçları
- Uzun listeyi sayfa sayfa görmek için `| less` ekleyin:
  ```bash
git log | less
```
- Tarihe, yazara veya mesaj anahtar kelimesine göre filtreleyebilirsiniz.

**Önceki**: [05. git status](05-status.md) &nbsp;|&nbsp; **Sonraki**: [07. git diff](07-diff.md)ptığınız tüm commit’leri (kaydedilen adımları) listeler. Kimin, ne zaman ne eklediğini, hangi mesajla kaydedildiğini görebilirsiniz.

## Ne Zaman Kullanılır?
- Geçmiş commit’lere bakmak istediğinizde
- Hangi değişikliğin hangi commit’te yapıldığını görmek istediğinizde

## Kullanımı
```bash
    git log
```
- Sadece özet görmek için:
```bash
    git log --oneline
```
- Merge ve branch akışını görmek için:
```bash
    git log --oneline --graph --all
```

## Örnekler
1. Komut ile tarih, yazar ve mesajı listeleme:
```bash
    git log
```
2. Kısaltılmış tek satır görünüm:
```bash
    git log --oneline
```
3. Branch ve merge grafiklerini ASCII art ile gösterme:
```bash
    git log --all --graph --decorate
```
4. Belirli bir dosyanın geçmişini takip etme:
```bash
    git log --follow -- path/to/file.js
```

## İpuçları
- Uzun listeyi sayfa sayfa görmek için `| less` ekleyin:
  ``bash
    git log | less
```
- Tarihe, yazara veya mesaj anahtar kelimesine göre filtreleyebilirsiniz.

---
_Bu örnekler gerçek projelerde günlük kullanımınıza yön verecek şekilde hazırlandı._
