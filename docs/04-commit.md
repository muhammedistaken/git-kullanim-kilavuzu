# 04. git commit

`git commit`, staging alanına eklediğiniz değişiklikleri kalıcı hale getirir. Yani `git add` ile seçtiklerinizi, bir paket gibi depo geçmişine kaydeder.

## Ne Zaman Kullanılır?
- Hazırlama alanındaki değişiklikleri kaydetmek istediğinizde
- Bir çalışma adımını anlamlı bir mesajla arşivlemek istediğinizde

## Kullanımı
```bash
    git commit -m "Mesaj"
```
- `-m "Mesaj"`: Commit için kısa açıklama yazmanızı sağlar.

## Örnekler
1. Hazır olan her şeyi commit etmek:
```bash
    git add .
    git commit -m "Projeyi ilk haliyle kaydettim"
```
2. Takip edilen dosyaları otomatik ekleyip commit etmek:
```bash
    git commit -a -m "Küçük güncellemeler"
```
3. Son commit mesajını düzenlemek:
```bash
    git commit --amend -m "Daha iyi açıklama"
```

## İpuçları
- Commit mesajı 50 karakteri geçmesin; başlık satırını kısa tutun.
- Detaylı açıklama gerekiyorsa `git commit` yazıp editörde açarak ikinci paragrafı ekleyin.
- `--amend` sadece daha önce push etmediyseniz güvenle kullanın.

**Önceki**: [03. git add](03-add.md) &nbsp;|&nbsp; **Sonraki**: [05. git status](05-status.md)
