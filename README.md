# SpaceX Latest Launch Info App

I would like to thank my esteemed lecturer, Dr. Fehim Köylü, for his invaluable contributions to our project.

In this project, the use of "hero" animations was abandoned due to compatibility concerns, and "scale transform" animations were preferred instead. You can see this effect during page transitions on the main page. While the main page is being built, the service that fetches information about the latest launch from SpaceX's API is called asynchronously. The retrieved data is then parsed and converted into a model. The data from the model is directed to the necessary pages and displayed as a list.

Değerli Hocam Dr. Öğretim Üyesi Fehim Köylü'ye, bize kattıklarından dolayı teşekkür ederim.

Bu projede, uygunluk kaygıları nedeniyle "hero" animasyonları yerine "scale transform" animasyonları tercih edilmiştir. Bu etkiyi ana sayfada sayfalar arası geçişlerde görebilirsiniz. Ana sayfa oluşturulurken, SpaceX'in API'sinden son fırlatmayla alakalı bilgileri çeken servis asenkron olarak çağrılmaktadır. Gelen veriler parse edilerek modele çevrilmekte ve modelden gelen veriler, gerekli sayfalara yönlendirilerek liste olarak gösterilmektedir.

## Overview / Genel Bakış

This Flutter application provides detailed information about SpaceX's latest launch, including:

- A YouTube video of the launch.
- A link to the Reddit discussion page.
- A Wikipedia page with detailed information about the launch.

Bu Flutter uygulaması, SpaceX'in en son fırlatışı hakkında detaylı bilgi sağlar, bunlar arasında:

- Fırlatmanın YouTube videosu.
- Reddit tartışma sayfasına bir bağlantı.
- Fırlatma hakkında detaylı bilgi içeren bir Wikipedia sayfası.

The app utilizes the following packages:

- `dio` for making HTTP requests.
- `youtube_player_flutter` for embedding YouTube videos.
- `webview_flutter` for displaying web pages.

Uygulama aşağıdaki paketleri kullanır:

- HTTP istekleri yapmak için `dio`.
- YouTube videolarını yerleştirmek için `youtube_player_flutter`.
- Web sayfalarını görüntülemek için `webview_flutter`.

## Features / Özellikler

- Fetch and display details about the latest SpaceX launch.
- Embed and play a YouTube video of the launch.
- Provide links to the Reddit discussion page and Wikipedia page.
- Display these web pages within the app using web views.

- En son SpaceX fırlatması hakkında detayları alın ve görüntüleyin.
- Fırlatmanın YouTube videosunu yerleştirin ve oynatın.
- Reddit tartışma sayfası ve Wikipedia sayfasına bağlantılar sağlayın.
- Bu web sayfalarını uygulama içinde web görünümleri kullanarak görüntüleyin.

## Requirements / Gereksinimler

- Flutter SDK: >= 2.5.0
- Dart: >= 2.12.0

## Packages Used / Kullanılan Paketler

- `dio`: For making HTTP requests to fetch launch data.
- `youtube_player_flutter`: For embedding and playing YouTube videos.
- `webview_flutter`: For displaying Reddit and Wikipedia pages within the app.

- `dio`: Fırlatma verilerini almak için HTTP istekleri yapmak.
- `youtube_player_flutter`: YouTube videolarını yerleştirmek ve oynatmak.
- `webview_flutter`: Reddit ve Wikipedia sayfalarını uygulama içinde görüntülemek.

## Getting Started / Başlarken

### Prerequisites / Ön Gereksinimler

Ensure you have the Flutter SDK installed. You can download it from [Flutter's official site](https://flutter.dev/docs/get-started/install).

Flutter SDK'sının yüklü olduğundan emin olun. [Flutter'ın resmi sitesinden](https://flutter.dev/docs/get-started/install) indirebilirsiniz.

### Installation / Kurulum

1. **Clone the repository: / Depoyu klonlayın:**
   ```sh
   git clone https://github.com/TahaDgn/spacex_last_flight.git
   cd spacex_last_flight
   flutter pub get
   flutter run
   ```

## Directory Structure / Dizin Yapısı

```
📦lib
 ┣ 📂models
 ┃ ┗ 📜spacex_flight_model.dart
 ┣ 📂services
 ┃ ┗ 📜request_services.dart
 ┣ 📂utils
 ┃ ┣ 📜.request.rest
 ┃ ┣ 📜.response.http
 ┃ ┣ 📜constants.dart
 ┃ ┗ 📜globals.dart
 ┣ 📂views
 ┃ ┣ 📂custom_widgets
 ┃ ┃ ┗ 📜custom_appbar.dart
 ┃ ┗ 📂main_page_view
 ┃ ┃ ┣ 📜buttons.dart
 ┃ ┃ ┣ 📜main_info.dart
 ┃ ┃ ┣ 📜web_page.dart
 ┃ ┃ ┗ 📜youtube_player.dart
 ┣ 📂view_models
 ┃ ┗ 📜flight_info_view_model.dart
 ┗ 📜main.dart
```

## Functionality / İşlevsellik

- **main.dart**: Initializes global values, fetches the latest flight information, and starts the app.
- **services/request_service.dart**: Manages fetching the latest SpaceX launch details using dio.
- **views/home_page.dart**: Displays launch details and provides navigation to YouTube video, Reddit page, and Wikipedia page.
- **views/youtube_video_page.dart**: Embeds and plays YouTube videos using youtube_player_flutter.
- **views/webview_page.dart**: Displays Reddit and Wikipedia pages within the app using webview_flutter.
- **widgets/custom_app_bar.dart**: Provides a custom app bar widget for consistent app design.

- **main.dart**: Global değerleri başlatır, en son uçuş bilgilerini alır ve uygulamayı başlatır.
- **services/request_service.dart**: Dio kullanarak en son SpaceX fırlatma detaylarını yönetir.
- **views/home_page.dart**: Fırlatma detaylarını görüntüler ve YouTube videosuna, Reddit sayfasına ve Wikipedia sayfasına navigasyon sağlar.
- **views/youtube_video_page.dart**: YouTube videolarını youtube_player_flutter kullanarak yerleştirir ve oynatır.
- **views/webview_page.dart**: Reddit ve Wikipedia sayfalarını webview_flutter kullanarak uygulama içinde görüntüler.
- **widgets/custom_app_bar.dart**: Tutarlı bir uygulama tasarımı için özel bir uygulama çubuğu widget'ı sağlar.

## Conclusion / Sonuç

This application provides users with the latest information on SpaceX launches, including video, discussions, and detailed information. Ensure all dependencies are installed and configured properly before running the app. If you encounter any issues, refer to the official documentation of each package used.

Bu uygulama, kullanıcılara SpaceX fırlatmaları hakkında en son bilgileri, videoları, tartışmaları ve detaylı bilgileri sağlar. Uygulamayı çalıştırmadan önce tüm bağımlılıkların yüklendiğinden ve doğru şekilde yapılandırıldığından emin olun. Herhangi bir sorunla karşılaşırsanız, kullanılan her paket için resmi dökümantasyona başvurun.
