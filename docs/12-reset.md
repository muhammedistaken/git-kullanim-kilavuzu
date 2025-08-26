# 12. git reset

`git reset`, HEAD’inizi başka bir commit’e taşır ve staging ile çalışma dizininizin durumunu istediğiniz gibi ayarlar. Üç modu var:

- `--soft`: Sadece HEAD taşınır, staging ve dosyalar olduğu gibi kalır.
- `--mixed` (varsayılan): HEAD taşınır, staging temizlenir, dosyalar değişmeden kalır.
- `--hard`: HEAD, staging ve çalışma dizini tamamen hedef commit ile aynı olur.

## Kullanımı
```bash
    git reset [mod] <commit>
```
- `<mod>`: `--soft`, `--mixed` veya `--hard`.
- `<commit>`: Taşınmak istediğiniz commit SHA’sı veya `HEAD~1` gibi bir referans.

## Örnekler
1. Son commit’i staging alanına dokunmadan geri almak:
```bash
    git reset --soft HEAD~1
```
2. Staging temizlenerek HEAD’i geri almak:
```bash
    git reset HEAD~1
```
3. Tüm değişiklikleri iptal edip son commit’e dönmek:
```bash
    git reset --hard HEAD~1
```
4. Uzak depo ile birebir eşitlemek:
```bash
    git fetch origin
    git reset --hard origin/main
```

## İpuçları
- `--hard` kullanmadan önce önemli değişikliklerinizi yedekleyin, geri dönüş zor olabilir.
- Hangi commit’leri geri alabileceğinizi `git reflog` ile görün.

---
_Bu komut, geri alma ve sürüm temizliği için güçlü bir araçtır; dikkatli kullanın._
