# 11. git rebase

`git rebase`, bir dalın (örneğin `feature`), başka bir dalın (örneğin `main`) en son halinin üzerine taşınmasını sağlar. Böylece daha temiz ve düz bir commit geçmişi elde edersiniz.

## Ne Zaman Kullanılır?
- Commit geçmişini düzenli ve lineer tutmak istediğinizde
- Branch’leri yeni temel üzerine taşımak istediğinizde

## Kullanımı
```bash
git rebase <hedef_dal>
```
- `<hedef_dal>`: Değişikliklerin taşınacağı dal (örn. `main`).

## Örnekler
1. `feature` dalını `main` üzerine rebase etmek:
   ```bash
git checkout feature
 git fetch origin
 git rebase origin/main
```
2. İnteraktif rebase ile commit’leri düzenlemek:
   ```bash
git rebase -i HEAD~3
```
   Son 3 commit üzerinde `pick`, `squash` veya `edit` yapabilirsiniz.

## Çakışma Durumu
- Çakışma olursa Git durur ve dosyalarda `<<<<<<<` işareti gösterir.
- Çakışmaları düzelttikten sonra:
  ```bash
git add .
 git rebase --continue
```
- Vazgeçmek isterseniz:
  ```bash
git rebase --abort
```

## İpuçları
- Paylaşılan (public) dallarda rebase’ten kaçının; başkalarının iş akışını bozmayın.
- Rebase sonrası `git push --force-with-lease` ile güvenli push yapın.

---
_Bu örnekler, temiz bir geçmiş için günlük kullanımınıza yön verecek şekilde hazırlandı._
