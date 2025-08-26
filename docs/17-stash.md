# 17. git stash

`git stash`, üzerinde çalıştığınız değişiklikleri bir kenara koyar ve çalışma alanınızı temizler. Örneğin acil bir işe geçmeniz gerekiyorsa ama kodunuz hazır değilse stash imdadınıza yetişir.

## Ne Zaman Kullanılır?
- Yarıda bıraktığınız işi kaybetmeden başka bir dala geçmek istediğinizde
- Deneme yanılma yaparken mevcut değişiklikleri saklamak istediğinizde

## Kullanımı
```bash
    git stash [push|pop|apply|list|drop|clear]
```
- `push`: (Varsayılan) Değişiklikleri saklar.
- `pop`: Saklanan son değişikliği uygular ve kayıttan siler.
- `apply`: Saklanan değişikliği uygular ama listede bırakır.
- `list`: Tüm stash kayıtlarını gösterir.
- `drop`: Belirli bir stash’i siler.
- `clear`: Tüm stash’leri temizler.

## Örnekler
1. Değişiklikleri saklamak:
```bash
    git stash
```
2. Saklama mesajı eklemek:
```bash
    git stash push "login özelliği üzerinde çalışılıyor"
```
3. En son saklamayı geri getirmek:
```bash
    git stash pop
```
4. Belirli stash’i uygulamak:
```bash
    git stash apply stash@{2}
```

## İpuçları
- `git stash list` ile tüm saklamalarınızı görün.
- Untracked veya ignored dosyaları da stash’e eklemek için:
```bash
    git stash push --include-untracked
```

---
_Bu komut, yarıda kalmış işleri güvenle saklamak için harika bir yol sunar._
