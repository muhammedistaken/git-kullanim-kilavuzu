# 15. git pull

`git pull`, uzak depodan (`fetch`) güncellemeleri indirir ve otomatik olarak çalıştığınız dala (`merge` veya `rebase`) uygular. Yani iki komutu tek seferde yapar.

## Ne Zaman Kullanılır?
- Başkalarının gönderdiği yeni kodları projenize almak istediğinizde
- Uzaktaki depo ile yerel deponuzu senkronize tutmak istediğinizde

## Kullanımı
```bash
git pull [uzak_adı] [dal_adı]
```
- `[uzak_adı]`: Genellikle `origin`.
- `[dal_adı]`: Çekmek istediğiniz branch (örn. `main`, `develop`).

## Örnekler
1. Basit pull:
   ```bash
git pull
```
   `origin` ve o anki dalı günceller.

2. Rebase ile pull:
   ```bash
git pull --rebase
```
   Merge yerine temiz bir geçmiş için rebase yapar.

3. Belirli bir remote’dan ve daldan çekme:
   ```bash
git pull upstream develop
```

4. Pull sırasında otomatik stoklama (autostash):
   ```bash
git pull --rebase --autostash
```

## İpuçları
- Otomatik merge yerine `fetch` + `merge/rebase` ile adım adım kontrol edebilirsiniz.
- Çakışma çıkarsa `git status` ve `git rebase --continue` veya `git merge` ile çözün.

---
_Bu komut, uzak ve yerel deponuzu güncel tutmanın en kolay yoludur._
