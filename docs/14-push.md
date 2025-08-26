# 14. git push

`git push`, yerel makinada yaptığınız commit’leri uzak depoya (örneğin GitHub, GitLab) gönderir. Böylece ekip arkadaşlarınız veya sunucu, sizin en güncel kodunuzu alır.

## Ne Zaman Kullanılır?
- Local’de geliştirdiğiniz yeni özellikleri veya düzeltmeleri paylaşmak istediğinizde
- Başkalarının da erişmesi gereken değişiklikleri sunucuya aktarmak için

## Kullanımı
```bash
git push [uzak_adı] [dal_adı]
```
- `[uzak_adı]`: Genellikle `origin` (ilk klonladığınız depo).
- `[dal_adı]`: Göndermek istediğiniz branch (örn. `main`, `develop`, `feature/login`).

## Örnekler
1. Varsayılan ayarlarla push:
   ```bash
git push
```
   `origin` ve o anki dalı gönderir.

2. Belirli bir dalı göndermek:
   ```bash
git push origin develop
```
   `origin` üzerine `develop` dalını aktarır.

3. Zorla (force) push yapmak:
   ```bash
git push --force-with-lease origin feature/login
```
   History’ye sonradan müdahale ettiyseniz kullanılır (dikkatli olun).

4. Tüm branch’ leri göndermek:
   ```bash
git push --all
```

5. Tüm etiketleri (tags) de göndermek:
   ```bash
git push --tags
```

## İpuçları
- `--force-with-lease`, `--force`’a göre daha güvenlidir; başkalarının güncel dalını korur.
- Push etmeden önce `git fetch` ve `git log origin/[dal]` ile sunucudaki son durumu kontrol edin.

---
_Bu komut, yaptığınız işleri ekip ortamına güvenli ve kontrollü bir şekilde iletmenizi sağlar._
