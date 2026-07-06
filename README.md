# Fate Zarları — Owlbear Rodeo Eklentisi

Owlbear Rodeo 2.0 için Fate / Fudge zarı (4dF) eklentisi.

## Özellikler
- 4dF atışı: her zar −1, 0 veya +1 gösterir (−, boş, +)
- Beceri modifikatörü (−4 ile +8 arası)
- Sonucu Fate merdivenindeki adıyla gösterir (ör. +4 → "Harika")
- Atışı odadaki herkese bildirim olarak duyurur (broadcast + notification)
- Son 8 atışın geçmişi (diğer oyuncuların atışları dahil)

## Dosyalar
- `manifest.json` — Owlbear Rodeo'nun eklentiyi tanıması için gereken dosya
- `index.html` — Eklentinin arayüzü ve tüm mantığı (tek dosya)
- `icon.svg` — Eklenti simgesi

## Kurulum

### 1. Dosyaları barındır (GitHub Pages — ücretsiz)
1. GitHub'da yeni bir repo oluştur (ör. `fate-dice-obr`), bu üç dosyayı reponun köküne yükle.
2. Repo → **Settings → Pages** → Source olarak **Deploy from a branch**, branch olarak `main` ve `/ (root)` seç, kaydet.
3. Birkaç dakika sonra siten şu adreste yayında olur:
   `https://KULLANICI_ADIN.github.io/fate-dice-obr/`
4. Manifest adresin:
   `https://KULLANICI_ADIN.github.io/fate-dice-obr/manifest.json`

(Netlify, Vercel veya Cloudflare Pages da kullanabilirsin — önemli olan `manifest.json`'a herkese açık bir HTTPS adresinden erişilebilmesi.)

### 2. Owlbear Rodeo'ya ekle
1. Owlbear Rodeo'da odanı aç.
2. Sol alttaki profil/oda menüsünden **Extensions**'a gir.
3. **Add Extension** (Add Custom Extension) düğmesine bas.
4. Manifest adresini yapıştır: `https://.../manifest.json`
5. Eklendikten sonra eklentiyi oda için **etkinleştir** (toggle).
6. Odanın sol üstündeki eklenti çubuğunda "Fate Zarları" simgesi belirir — tıkla ve zar at!

> Not: Eklentiyi odaya sadece GM'in eklemesi yeterlidir; etkinleştirildiğinde odadaki tüm oyuncularda görünür.

## Yerelde deneme (isteğe bağlı)
```bash
cd fate-dice
npx serve .        # veya: python3 -m http.server 8000
```
Sonra Owlbear Rodeo'ya manifest olarak `http://localhost:3000/manifest.json` ekleyebilirsin (yerel geliştirme için).

## Fate merdiveni (Türkçe karşılıklar)
+8 Efsanevi · +7 Destansı · +6 Muhteşem · +5 Olağanüstü · +4 Harika · +3 İyi · +2 Hoş · +1 Ortalama · 0 Vasat · −1 Zayıf · −2 Berbat
