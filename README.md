# RSS Feed Kaynakları

Bu klasör, AkeysyOS RSS Reader uygulaması için kullanılan RSS feed kaynaklarını içerir.

## 📁 Klasör Yapısı

```
RSS/
├── Ekonomi/rss_feeds.txt          # Ekonomi ve finans haberleri (40 feed)
├── Galeri/rss_feeds.txt           # Galeri ve görsel içerikler (12 feed)
├── Güncel/rss_feeds.txt           # Güncel haberler (621 feed)
├── Sağlık/rss_feeds.txt           # Sağlık haberleri (16 feed)
├── Son Dakika/rss_feeds.txt       # Son dakika haberleri (8 feed)
├── Spor/rss_feeds.txt             # Spor haberleri (42 feed)
├── Teknoloji/rss_feeds.txt        # Teknoloji haberleri (51 feed)
├── Video/rss_feeds.txt            # Video içerikler (8 feed)
├── Yaşam/rss_feeds.txt            # Yaşam ve kültür (75 feed)
└── Yerel/                         # Yerel haberler (81 şehir)
    ├── Adana/rss_feeds.txt
    ├── Ankara/rss_feeds.txt
    ├── İstanbul/rss_feeds.txt
    └── ... (diğer şehirler)
```

## 📊 İstatistikler

- **Toplam Kategori:** 9 ana kategori + 81 yerel kategori
- **Toplam RSS Feed:** 964 aktif feed
- **Kapsanan Şehir:** Türkiye'nin 81 ili

## 🔧 Dosya Formatı

Her `rss_feeds.txt` dosyası şu formatta düzenlenmiştir:

```
https://example.com/rss/feed1.xml
https://example.com/rss/feed2.xml
https://example.com/rss/feed3.xml
```

- Her satırda bir RSS feed URL'i
- Boş satırlar ve # ile başlayan yorumlar desteklenir
- Sadece geçerli HTTP/HTTPS URL'leri kabul edilir

## 🚀 Kullanım

### AkeysyOS'ta Kullanım

1. RSS Reader uygulamasını açın
2. Ayarlar > RSS Feed Kaynakları bölümüne gidin
3. "Kaynak Ekle" butonuna tıklayın
4. GitHub raw URL'ini girin:
   ```
   https://raw.githubusercontent.com/username/repo/main/RSS/Kategori/rss_feeds.txt
   ```

### Manuel Import

```bash
# Tüm kategorileri import et
curl -s https://raw.githubusercontent.com/username/repo/main/RSS/Teknoloji/rss_feeds.txt

# Belirli bir şehrin haberlerini import et
curl -s https://raw.githubusercontent.com/username/repo/main/RSS/Yerel/Istanbul/rss_feeds.txt
```

## 🔍 Doğrulama

RSS dosyalarının doğruluğunu kontrol etmek için:

```bash
python3 validate_rss_files.py
```

Bu script:
- Tüm URL'lerin geçerliliğini kontrol eder
- Hatalı satırları temizler
- Dosyaları standart formata dönüştürür

## 📝 Katkıda Bulunma

Yeni RSS feed eklemek için:

1. İlgili kategori dosyasını açın
2. Yeni URL'i dosyanın sonuna ekleyin
3. `validate_rss_files.py` ile doğrulayın
4. Pull request gönderin

## ⚠️ Notlar

- Tüm URL'ler düzenli olarak test edilir
- Çalışmayan feedler otomatik olarak kaldırılır
- Yeni kategoriler eklenebilir
- Yerel haberler için şehir bazlı organizasyon kullanılır

## 📞 İletişim

Sorun bildirmek veya öneri göndermek için GitHub Issues kullanın.

---

**Son Güncelleme:** $(date)
**Toplam Feed Sayısı:** 964
**Durum:** ✅ Tüm feedler doğrulandı