# 03. git add

Dosyalarınızı Git’e kaydetmek için önce `git add` komutu ile onları “hazırlama alanına” (staging area) eklemelisiniz. Bu sayede hangi değişikliklerin bir sonraki commit’e dahil edileceğini seçersiniz.

## Ne Zaman Kullanılır?
- Yeni dosya eklediğinizde
- Dosyada değişiklik yaptığınızda
- Dosyayı sildiğinizde

## Kullanımı
```bash
    git add <dosya_veya_klasör>...
```
- İster tek dosya, ister tüm klasörleri ekleyebilirsiniz.

## Örnekler
1. Tek bir dosya eklemek:
```bash
    git add dosya.txt
```
2. Tüm değişiklikleri (yeni, güncellenen, silinen) hazırlama alanına almak:
```bash
    git add -A
```
3. Sadece değiştirilen dosyaları eklemek:
```bash
    git add -u
```
4. Mevcut klasördeki her şeyi eklemek:
```bash
    git add .
```
5. İnteraktif modda parçaları seçerek eklemek:
```bash
    git add -p
```

## İpuçları
- `git status` ile hangi dosyaların hazır olduğunu kontrol edin.
- Yanlış eklediğiniz dosyaları `git reset <dosya>` ile geri alabilirsiniz.

---
_Bu komut, commit öncesi hangi değişikliklerin kaydedileceğini seçmek için çok işinize yarar._
