# 16. git fetch

`git fetch`, uzak depodaki yeni commit’leri indirir ama onları otomatik olarak çalışma dalınıza eklemez. Uzaktaki değişiklikleri incelemek için kullanılır.

## Ne Zaman Kullanılır?
- Uzaktaki son durumları görmek istediğinizde ama hemen birleştirmek istemediğinizde
- Değişiklikleri inceleyip onaylamak istediğinizde

## Kullanımı
```bash
    git fetch [uzak_adı]
```
- `[uzak_adı]`: Genellikle `origin`.

## Örnekler
1. Varsayılan remote’dan fetch:
```bash
    git fetch
```
2. Belirli bir dalı fetch (örn. `develop`):
```bash
    git fetch origin develop
```
3. Tüm remote’ları fetch:
```bash
    git fetch --all
```

## İpuçları
- Fetch sonrası `git log origin/main` veya `git diff main origin/main` ile farkı görün.
- `pull` yerine `fetch` + `merge`/`rebase` yaparak kontrolü elinizde tutun.

**Önceki**: [15. git pull](15-pull.md) &nbsp;|&nbsp; **Sonraki**: [17. git stash](17-stash.md)
