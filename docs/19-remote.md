# 19. git remote

`git remote`, p## İpuçları
- Fork ile çalışırken `origin` sizin fork'unuz, `upstream` orijinal depo olsun.
- SSH yerine HTTPS kullanıyorsanız, her pull/push'ta parola girmeniz gerekebilir.

**Önceki**: [18. git tag](18-tag.md) &nbsp;|&nbsp; **Sonraki**: [20. git config](20-config.md)ze bağlı uzak depoları (remote) gösterir, ekler veya siler. Uzak depo, kodunuzu paylaştığınız sunucudur.

## Ne Zaman Kullanılır?
- Hangi uzak depoların bağlı olduğunu görmek istediğinizde
- Yeni bir uzak depo ekleyip kod göndermek veya almak istediğinizde

## Kullanımı
```bash
    git remote [seçenekler] [ad] [url]
```
- `git remote -v`: URL’leriyle birlikte tüm remote’ları listeler.
- `git remote add <isim> <url>`: Yeni bir remote ekler (örn. `upstream`).
- `git remote remove <isim>`: Belirtilen remote’u siler.
- `git remote rename <eski> <yeni>`: Remote adını değiştirir.

## Örnekler
1. Uzak depoları URL ile listeleme:
```bash
    git remote -v
```
2. Yeni upstream remote ekleme:
```bash
    git remote add upstream https://github.com/orijinal/proje.git
```
3. Remote silme:
```bash
    git remote remove upstream
```
4. Remote URL’yi değiştirme:
```bash
    git remote set-url origin git@github.com:ben/proje.git
```

## İpuçları
- Fork ile çalışırken `origin` sizin fork’unuz, `upstream` orijinal depo olsun.
- SSH yerine HTTPS kullanıyorsanız, her pull/push’ta parola girmeniz gerekebilir.

---
_Bu komut, uzak depo ayarlarınızı yönetmek için gereklidir._
