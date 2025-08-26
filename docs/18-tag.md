# 18. git tag

Git’de "tag" (etiket) komutu, projenizde önemli bir andan ya da sürümden hemen sonra işaret koymanızı sağlar. Mesela bir uygulamayı 1.0 sürümünde canlıya aldınız diyelim; bu noktayı kolayca işaretlemek için tag kullanırsınız.

## Ne işe yarar?
- Geçmişteki bir sürüme hızlıca dönmeye yardım eder.
- "v1.0", "v2.1.3" gibi sürüm adlarını kolayca görebilirsiniz.
- Ekip içinde ortak bir sürüm numarası üzerinde anlaşmanızı sağlar.

## Söz dizimi
```bash
    git tag [seçenekler] <etiket_adı> [<commit>]
```
- `<etiket_adı>`: Oluşturmak istediğiniz etiket (örneğin: `v1.0`, `deneme-tag`).
- `[<commit>]`: Hangi commit’e etiket koymak istiyorsanız onun SHA’sı (bunu yazmazsanız en son commit’e eklenir).

## Basit Örnekler
1. Son commit’e hafif etiket (lightweight tag) eklemek:
```bash
    git tag v1.0
```
   Bu komutla sadece `v1.0` etiketi oluşturulur; ekstra bilgi kaydı tutulmaz.

2. Annotated (açıklamalı) etiket oluşturmak:
```bash
    git tag -a v1.0.1 -m "Hata düzeltme sürümü"
```
   `-a`: Yazar, tarih ve mesajı da kaydeder. Kim, ne zaman eklemiş bilgisi saklanır.

3. Etiketi uzak sunucuya göndermek:
```bash
    git push origin v1.0.1
```
   `origin` yerine sizin uzak depo adınız olabilir.

## Birden çok etiketi tek seferde gönderme
```bash
    git push --tags
```
Tüm yerel etiketleri uzak sunucuya bir kerede taşır.

## Etiket Silme
1. Yerelden silmek:
```bash
    git tag -d v1.0.0
```
2. Uzak sunucudan silmek:
```bash
    git push origin :refs/tags/v1.0.0
```

## İpuçları ve Dikkat Edilmesi Gerekenler
- Hafif tag’ler sadece işaret koyar; sürüm geçmişinde kim, ne zaman yazdığı tutulmaz.
- Annotated tag’ler genellikle sürüm yayınlarında tercih edilir.
- Semantic Versioning ("vMAJOR.MINOR.PATCH" – örneğin `v2.1.3`) kullanarak net sürüm numaraları oluşturun.

**Önceki**: [17. git stash](17-stash.md) &nbsp;|&nbsp; **Sonraki**: [19. git remote](19-remote.md)