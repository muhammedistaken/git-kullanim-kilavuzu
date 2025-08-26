# 01. git init

Git ile projenizi takip etmeye başlamak için kullandığınız ilk komut `git init`tir. Bu komut, bulunduğunuz klasörü Git deposu haline getirir.

## Ne zaman kullanılır?
- Sıfırdan yeni bir proje açarken
- Var olan bir klasörde versiyon kontrolü eklemek istediğinizde

## Kullanımı
```bash
git init [klasör_adı]
```
- `klasör_adı` yazmazsanız, mevcut klasörünüzü Git deposuna dönüştürür.

## Örnekler
1. Mevcut klasörde Git repo başlatma:
```bash
    git init
```
2. Yeni klasör açıp içinde başlatma:
```bash
    mkdir yeni-projem
    cd yeni-projem
    git init
```
3. Sadece veri klasörü olan bare (çıplak) depo oluşturma:
```bash
    git init --bare sunucu-deposu.git
```

## İpuçları
- Komutu çalıştırmadan önce `pwd` ile doğru dizinde olduğunuzu kontrol edin.
- Projenizi izlemeye başlamadan önce `.gitignore` dosyası ekleyin.

---
_Burada basit örneklerle, günlük projelerinizde hemen kullanabileceğiniz şekilde anlatıldı._
