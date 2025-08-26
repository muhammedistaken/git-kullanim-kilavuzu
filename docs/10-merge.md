# 10. git merge

`git merge`, üze## İpuçları
- Merge'den önce `git fetch` veya `git pull --rebase` ile dallarınızı güncel tutun.
- Karmaşık çatışmalarda `git mergetool` kullanabilirsiniz.

**Önceki**: [09. git checkout](09-checkout.md) &nbsp;|&nbsp; **Sonraki**: [11. git rebase](11-rebase.md)çalıştığınız dala başka bir dalın değişikliklerini ekler. Diyelim ki `feature/login` üzerinde çalıştınız ve bu kodu `develop` dalına katmak istiyorsunuz.

## Ne Zaman Kullanılır?
- Farklı dallardaki işleri birleştirip tek bir dala toplamak istediğinizde
- Takım olarak geliştirilen kodları ana dala aktarmak istediğinizde

## Kullanımı
```bash
    git merge <kaynak_dal>
```
- `<kaynak_dal>`: Birleştirmek istediğiniz dalın adı (ör. `feature/login`).

## Örnekler
1. `feature` dalını `develop` dalına eklemek:
```bash
    git checkout develop
    git merge feature/login
```
2. Fast-forward (hızlı) değil, her zaman yeni bir merge commit oluşturmak:
```bash
    git merge --no-ff feature/login
```
3. Squash yaparak tek commit oluşturmak:
```bash
    git merge --squash feature/experiment
    git commit -m "Deneysel özellik tek commit olarak birleştirildi"
```

## Çakışma (Conflict) Durumu
- Merge sırasında dosyalarda çakışma olursa Git sizi uyarır.
- `git status` ile hangi dosyalarda çakışma olduğunu görün.
- Dosyaları düzenleyip `git add` yaptıktan sonra `git commit` ile işlemi tamamlayın.

## İpuçları
- Merge’den önce `git fetch` veya `git pull --rebase` ile dallarınızı güncel tutun.
- Karmaşık çatışmalarda `git mergetool` kullanabilirsiniz.

---
_Bu örnekler, dal birleştirmeyi gündelik projelerde kolaylaştıracak şekilde hazırlandı._
