# 09. git checkout

`git checkout` komutu ile:
- Başka bir dala geçebilir,
- Yeni bir dal oluşturup geçiş yapabilir,
- Çalışma dosyalarını belirli bir commit’e döndürebilirsiniz.

## Kullanımı
```bash
    git checkout [seçenekler] <dal_adı|commit> [-b yeni_dal]
```
- `<dal_adı>`: Geçiş yapmak istediğiniz dal adı
- `-b yeni_dal`: Yeni dal oluşturup ona geçer
- `<commit>`: Dosyaları bu commit’e döndürmek için `-- dosya_adı`

## Örnekler
1. Mevcut bir dala geçmek:
```bash
    git checkout develop
```
2. Yeni bir dal oluşturup geçmek:
```bash
    git checkout -b feature-login
```
3. Dosyayı son commit’ten önceki haline döndürmek:
```bash
    git checkout HEAD~1 -- app.js
```
4. Çatışma varsa zorla geçmek (dikkatli olun):
```bash
    git checkout -f bugfix-123
```

## İpuçları
- Git v2.23+ için `git switch` ve `git restore` komutlarını tercih edebilirsiniz; `checkout`’a göre daha anlaşılır.
- Değişikliklerinizi kaybetmemek için geçişten önce `git stash` kullanın.

---
**Önceki**: [08. git branch](08-branch.md) &nbsp;|&nbsp; **Sonraki**: [10. git merge](10-merge.md)
