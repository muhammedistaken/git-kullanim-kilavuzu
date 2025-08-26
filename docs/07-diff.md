# 07. git diff

`git diff`, iki şey arasındaki farkı gösterir: çalışma dizininiz ile staging alanı, ya da iki commit arasındaki değişiklikleri.

## Ne Zaman Kullanılır?
- Henüz commit etmediğiniz değişiklikleri görmek istediğinizde
- Commit’ler arasındaki farklılıklara göz atarken

## Kullanımı
```bash
    git diff [kaynak] [hedef]
```
- Hiç argüman koymazsanız: çalışma dizini ile staging alanı farkını gösterir.
- `--staged` ya da `--cached`: staging alanı ile son commit arasındaki fark.
- `git diff commit1 commit2`: İki commit arasını karşılaştırır.

## Örnekler
1. Henüz eklemediğiniz değişiklikler:
```bash
    git diff
```
2. Staging’den sonraki fark:
```bash
    git diff --staged
```
3. İki commit’i karşılaştırmak:
```bash
    git diff abc123 def456
```
4. Sadece özet istatistik:
```bash
    git diff --stat
```

## İpuçları
- `| less -R` ekleyerek sayfa sayfa inceleyin.
- Renkli görmek için terminal ayarlarınızı kontrol edin.

**Önceki**: [06. git log](06-log.md) &nbsp;|&nbsp; **Sonraki**: [08. git branch](08-branch.md)
