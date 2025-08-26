# 13. git revert

`git revert`, seçtiğiniz bir commit’in yaptığı değişiklikleri geri alacak yeni bir commit oluşturur. Proje geçmişini bozmadan hatalı adımları geri almak için kullanılır.

## Ne Zaman Kullanılır?
- Yanlış bir commit’i tamamen silmek yerine düzeltmek istediğinizde
- Proje geçmişini koruyarak geri alma yapmak istediğinizde

## Kullanımı
```bash
    git revert <commit>
```
- `<commit>`: Geri almak istediğiniz commit’in SHA’sı (örn. `a1b2c3d`).

## Örnekler
1. Basit revert:
```bash
    git revert a1b2c3d
```
2. Hemen commit yapmadan revert değişikliklerini staging’e eklemek:
```bash
    git revert -n a1b2c3d
```
3. Merge commit için (hangi parent’a göre revert):
```bash
    git revert -m 1 d4e5f6g
```

## İpuçları
- `git log` ile commit SHA’sını doğru aldığınızdan emin olun.
- Merge commit’lerde `-m` parametresiyle hangi ana hataya göre geri alacağınızı seçin.

**Önceki**: [12. git reset](12-reset.md) &nbsp;|&nbsp; **Sonraki**: [14. git push](14-push.md)