# KykScraped

[🇹🇷 Türkçe](README.tr.md) | [🇬🇧 English](README.md)

KykScraped, Türkiye'deki KYK yurtları için günlük menü bilgilerini gösteren modern bir Android uygulamasıdır. Uygulama, kullanıcıların farklı şehirler için kahvaltı ve akşam yemeği menülerini kontrol etmelerini sağlar.

## Özellikler

- Türkiye çapında farklı şehirlerin menülerini görüntüleme
- Kahvaltı ve akşam yemeği menüleri arasında geçiş yapma
- Birden fazla günlük menü bilgisini gösterme
- Ağ kazıyıcı ile gerçek zamanlı veri çekme
- Jetpack Compose ile modern Material 3 kullanıcı arayüzü
- (Varsa) Her menü için kalori bilgisi

## Mimari

Uygulama, MVVM deseni ile Clean Architecture prensiplerini takip eder:

```
KykScraped/
├── data/           # Veri katmanı (API'ler, DTO'lar, Repository implementasyonları)
├── domain/         # Domain katmanı (İş mantığı, Modeller, Use case'ler)
└── presentation/   # UI katmanı (Ekranlar, ViewModel'lar)
```

### Temel bileşenler:

- Clean Architecture
- MVVM
- Dependency Injection
- Kotlin Coroutines
- Jetpack Compose
- Repository Pattern
- Web Scraping

## Teknoloji Kümesi

- [Kotlin](https://kotlinlang.org/): Ana programlama dili
- [Jetpack Compose](https://developer.android.com/jetpack/compose): Modern UI araç seti
- [Material 3](https://m3.material.io/): Tasarım sistemi
- [Hilt](https://dagger.dev/hilt/): Bağımlılık enjeksiyonu (Dependency injection)
- [Ktor](https://ktor.io/): Ağ istemcisi
- [JSoup](https://jsoup.org/): HTML ayrıştırma
- [Coroutines](https://kotlinlang.org/docs/coroutines-overview.html): Asenkron programlama
- [ViewModel](https://developer.android.com/topic/libraries/architecture/viewmodel): UI state yönetimi
- [Flow](https://kotlinlang.org/docs/flow.html): Reaktif programlama

## Başlangıç

### Önkoşullar

- Android Studio Iguana 2023.2.1 veya daha yenisi
- Android SDK 35
- JDK 17 veya daha yenisi

### Kurulum

1. Depoyu klonlayın:
   ```bash
   git clone https://github.com/tamersarioglu/kykscraped.git
   ```
2. Projeyi Android Studio'da açın
3. Gradle dosyalarını senkronize edin ve projeyi build edin
4. Uygulamayı bir emülatörde veya fiziksel cihazda çalıştırın

## Yapılandırma

Uygulama aşağıdaki yapılandırmaları kullanır:

- minSdk: 24
- targetSdk: 35
- compileSdk: 35

## Proje Yapısı

```
├── app/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/com/tamersarioglu/kykscraped/
│   │   │   │   ├── data/
│   │   │   │   │   ├── mapper/
│   │   │   │   │   ├── model/
│   │   │   │   │   ├── remote/
│   │   │   │   │   └── repository/
│   │   │   │   ├── di/
│   │   │   │   ├── domain/
│   │   │   │   │   ├── model/
│   │   │   │   │   ├── repository/
│   │   │   │   │   ├── usecase/
│   │   │   │   │   └── util/
│   │   │   │   ├── presentation/
│   │   │   │   │   ├── menu/
│   │   │   │   └── ui/theme/
│   │   │   └── res/
```

## Kullanım

1. Açılır menüden bir şehir seçin
2. Switch kullanarak kahvaltı ve akşam yemeği menüleri arasında geçiş yapın
3. Seçilen şehir ve öğün türü için günlük menüleri görüntüleyin

## Lisans

Bu proje Apache Lisansı 2.0 altında lisanslanmıştır. Detaylar için [LICENSE](LICENSE) dosyasına bakın.

## Geliştirici

- Tamer Sarıoğlu

## Teşekkürler

- Menü verilerini sağladığı için [Kykyemek.com](https://kykyemek.com)'a
