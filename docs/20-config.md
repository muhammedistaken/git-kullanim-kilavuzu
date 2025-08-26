# 20. git config

## Açıklama
`git config` komutu, Git yapılandırma ayarlarını okur ve değiştirir. Kullanıcı bilgileri, alias’lar ve diğer ayarlar bu komutla yönetilir.

## Söz Dizimi
```
git config [<options>] [<key> [<value>]]
```

- `--global`: Kullanıcı genelindeki konfigürasyon dosyasını (`~/.gitconfig`) düzenler.
- `--system`: Sistem genelindeki yapılandırma (`/etc/gitconfig`).
- `--local`: Depoya özel yapılandırma (`.git/config`). Varsayılan.

## Temel Örnekler
1. Kullanıcı adı ayarlamak:
```bash
    git config --global user.name "Ahmet Yılmaz"
```
2. E-posta ayarlamak:
```bash
    git config --global user.email "ahmet@example.com"
```
3. Editor olarak VS Code ayarlamak:
```bash
    git config --global core.editor "code --wait"
```

## Gelişmiş Örnekler
- Alias tanımlamak:
```bash
    git config --global alias.co checkout
```
- Renkli çıktı ayarları:
```bash
    git config --global color.ui auto
```
- Merge tool ayarlamak:
```bash
    git config --global merge.tool kdiff3
```

## İpuçları
- `git config -l` ile tüm ayarları listeleyin.
- `.gitconfig` dosyasını manuel düzenlerken dikkatli olun; format hataları yapmayın.

**Önceki**: [19. git remote](19-remote.md) &nbsp;|&nbsp; **Sonraki**: -
