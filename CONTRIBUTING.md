# Katkıda Bulunma Rehberi

Bu rehber, GitHub Workshop'ta nasıl Pull Request (PR) açacağınızı adım adım anlatmaktadır.

## Üç Yöntem Var

| Yöntem                             | Zorluk       | Açıklama                                              |
| ---------------------------------- | ------------ | ----------------------------------------------------- |
| **Yöntem 1: JSON (Web)**           | ⭐ Kolay     | GitHub web sitesinden yeni dosya oluşturursunuz       |
| **Yöntem 2: HTML (Web)**           | ⭐⭐ Orta    | GitHub web sitesinden mevcut dosyayı düzenlersiniz    |
| **Yöntem 3: Terminal (Git Clone)** | ⭐⭐⭐ İleri | Repoyu bilgisayarınıza indirip terminal kullanırsınız |

---

## Yöntem 1: JSON Dosyası Ekleme - Web (Kolay)

Bu yöntemde GitHub web sitesinden `messages/` klasörüne kendi JSON dosyanızı ekleyeceksiniz.

### Adım 1: Repoyu Fork Edin

1. Bu sayfanın sağ üstündeki **Fork** butonuna tıklayın
2. Kendi hesabınıza fork oluşturun

### Adım 2: Yeni Dosya Oluşturun

1. Fork'unuzda `messages/` klasörüne gidin
2. **Add file** > **Create new file** tıklayın
3. Dosya adını yazın: `kullanici-adiniz.json` (örn: `mehmet.json`)

### Adım 3: JSON İçeriğini Yazın

Aşağıdaki şablonu kopyalayıp kendi bilgilerinizi yazın:

```json
{
  "name": "Bayram Simsek",
  "message": "Workshop harika gidiyor!",
  "emoji": "🔥⭐",
  "github": "bayramsimsek2000-dev"
}
```

**Emoji Önerileri:** 🚀 💻 ⭐ 🎯 💡 🔥 ✨ 🎉 👋 🌟 💪 🎨 📚 🏆 😇

### Adım 4: Değişikliği Commit Edin

1. Sayfanın altındaki **Commit changes** butonuna tıklayın
2. Commit mesajı yazın: `Add message from [adınız]`
3. **Commit directly to the main branch** seçili olsun
4. **Commit changes** tıklayın

### Adım 5: Pull Request Açın

1. Fork'unuzun ana sayfasına gidin
2. Sarı banner'daki **Compare & pull request** butonuna tıklayın
3. PR başlığı yazın: `Add message from [adınız]`
4. **Create pull request** tıklayın

🎉 **Tebrikler!** İlk PR'ınızı açtınız!

---

## Yöntem 2: HTML Düzenleme - Web (Orta Seviye)

Bu yöntemde GitHub web sitesinden `index.html` dosyasına yeni bir kart ekleyeceksiniz.

### Adım 1-2: Fork Edin (Yukarıdaki gibi)

### Adım 3: index.html Dosyasını Düzenleyin

1. Fork'unuzda `index.html` dosyasını açın
2. Sağ üstteki **kalem ikonuna** (Edit) tıklayın
3. `<!-- 👇 YENİ KARTLAR BURAYA EKLENSİN 👇 -->` yorumunu bulun
4. Aşağıdaki kart şablonunu bu yorumun altına ekleyin:

```html
<article class="message-card" data-color="purple">
  <div class="card-emoji">🚀</div>
  <h3 class="card-name">Adınız Soyadınız</h3>
  <p class="card-message">Workshop hakkında mesajınızı buraya yazın!</p>
  <a
    href="https://github.com/KULLANICI-ADINIZ"
    class="card-github"
    target="_blank"
  >
    <svg viewBox="0 0 24 24" width="16" height="16" fill="currentColor">
      <path
        d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"
      />
    </svg>
    @KULLANICI-ADINIZ
  </a>
</article>
```

**Renk Seçenekleri:** `purple`, `pink`, `blue`, `green`, `orange`, `cyan`

### Adım 4-5: Commit ve PR (Yukarıdaki gibi)

---

## Yöntem 3: Terminal ile Git Clone (İleri Seviye)

Bu yöntemde repoyu bilgisayarınıza indirip, terminal kullanarak değişiklik yapacaksınız.

### Gereksinimler

- [Git](https://git-scm.com/downloads) kurulu olmalı
- Terminal/Command Prompt kullanabilmeli

### Adım 1: Repoyu Fork Edin

GitHub web sitesinde **Fork** butonuna tıklayın.

### Adım 2: Fork'unuzu Clone Edin

Terminal açın ve şu komutu çalıştırın:

```bash
git clone https://github.com/KULLANICI-ADINIZ/github-workshop.git
```

> `KULLANICI-ADINIZ` yerine kendi GitHub kullanıcı adınızı yazın.

### Adım 3: Proje Klasörüne Girin

```bash
cd github-workshop
```

### Adım 4: Yeni Branch Oluşturun (Opsiyonel ama önerilir)

```bash
git checkout -b add-message-adiniz
```

### Adım 5: JSON Dosyanızı Oluşturun

`messages/` klasörüne kendi JSON dosyanızı ekleyin:

```bash
# macOS/Linux
cat > messages/adiniz.json << 'EOF'
{
  "name": "Adınız Soyadınız",
  "message": "Workshop hakkında bir mesaj yazın!",
  "emoji": "🚀",
  "github": "github-kullanici-adiniz"
}
EOF
```

Veya favori metin editörünüzle dosyayı oluşturun:

```bash
# VS Code ile
code messages/adiniz.json

# Nano ile
nano messages/adiniz.json

# Notepad ile (Windows)
notepad messages/adiniz.json
```

### Adım 6: Değişiklikleri Staging'e Ekleyin

```bash
git add messages/adiniz.json
```

Veya tüm değişiklikleri eklemek için:

```bash
git add .
```

### Adım 7: Commit Yapın

```bash
git commit -m "Add message from Adiniz"
```

### Adım 8: Push Edin

```bash
# main branch'e push
git push origin main

# Eğer yeni branch oluşturduysanız
git push origin add-message-adiniz
```

### Adım 9: Pull Request Açın

1. GitHub'da fork'unuza gidin
2. **Compare & pull request** butonuna tıklayın
3. PR açıklamasını yazın ve **Create pull request** tıklayın

---

## Bonus: Ana Repodan Güncellemeleri Çekme (Sync Fork)

Eğer ana repo güncellendiyse, fork'unuzu güncel tutmak için:

### Web Üzerinden (Kolay)

1. GitHub'da fork'unuza gidin
2. **Sync fork** butonuna tıklayın
3. **Update branch** tıklayın

### Terminal ile

```bash
# Ana repoyu remote olarak ekleyin (sadece bir kez)
git remote add upstream https://github.com/ORIJINAL-SAHIP/github-workshop.git

# Güncellemeleri çekin
git fetch upstream

# main branch'e geçin
git checkout main

# Upstream'den merge edin
git merge upstream/main

# Kendi fork'unuza push edin
git push origin main
```

---

## Merge Conflict Çözme

Eğer PR'ınızda conflict varsa:

### GitHub Web Üzerinden

1. GitHub'da conflict mesajını göreceksiniz
2. **Resolve conflicts** butonuna tıklayın
3. Çakışan kısımları düzenleyin:
   - `<<<<<<< HEAD` ve `=======` arasındaki kısım: orijinal kod
   - `=======` ve `>>>>>>> branch-name` arasındaki kısım: sizin kodunuz
4. İşaretçileri (`<<<<<<<`, `=======`, `>>>>>>>`) silin
5. Her iki kartı da tutun (üst üste)
6. **Mark as resolved** tıklayın
7. **Commit merge** tıklayın

### Terminal ile

```bash
# Güncellemeleri çekin
git fetch upstream
git merge upstream/main

# Conflict olan dosyaları düzenleyin
# Editörünüzle dosyayı açın ve conflict işaretlerini temizleyin

# Çözümü staging'e ekleyin
git add .

# Merge commit'i tamamlayın
git commit -m "Resolve merge conflict"

# Push edin
git push origin main
```

---

## Yararlı Git Komutları

| Komut                  | Açıklama                           |
| ---------------------- | ---------------------------------- |
| `git status`           | Değişiklikleri görüntüle           |
| `git log --oneline`    | Commit geçmişini görüntüle         |
| `git diff`             | Yapılan değişiklikleri göster      |
| `git branch`           | Branch'leri listele                |
| `git checkout -b isim` | Yeni branch oluştur ve geç         |
| `git pull`             | Uzak repodan değişiklikleri çek    |
| `git push`             | Değişiklikleri uzak repoya gönder  |
| `git stash`            | Değişiklikleri geçici olarak sakla |
| `git stash pop`        | Saklanan değişiklikleri geri al    |

---

## Yardım

Sorun yaşarsanız:

- Workshop eğitmenine sorun
- [GitHub Docs](https://docs.github.com/en/pull-requests) sayfasına bakın
- [Git Cheat Sheet](https://education.github.com/git-cheat-sheet-education.pdf)

---

**İyi kodlamalar!** 🚀
