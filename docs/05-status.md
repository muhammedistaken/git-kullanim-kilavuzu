# 05. git status

`git status` komutu, projenizin ne durumda olduğunu gösterir. Hangi dosyalar değişmiş, hangileri staging’de, hangileri takip edilmiyor hepsini listeler.

## Ne Zaman Kullanılır?
- Commit veya add işlemi öncesi kontrol amaçlı
- Projede hangi dosyaların değiştiğini görmek istediğinizde

## Kullanımı
```bash
    git status
```
- Özet görmek isterseniz:
```bash
    git status -s
```
- Branch bilgisini de görmek isterseniz:
```bash
    git status -b
```

## Örnek Çıktı
```
    on branch develop
    Changes to be committed:
    (use "git reset HEAD <file>..." to unstage)
        modified:   app.js

    Changes not staged for commit:
        modified:   index.html

    Untracked files:
    (use "git add <file>..." to include in what will be committed)
        notes.txt
```

## İpuçları
- Dosyalarla oynamadan önce `git status` ile durum kontrolü yapın.
- Hazırlama alanını temizlemek için `git reset` veya `git checkout -- <dosya>` kullanın.

**Önceki**: [04. git commit](04-commit.md) &nbsp;|&nbsp; **Sonraki**: [06. git log](06-log.md)
