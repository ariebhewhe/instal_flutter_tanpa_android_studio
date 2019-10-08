# Install Flutter Tanpa Android Studio 
Catatan untuk melakukan instal tanpa menggunakan android studio yang memiliki Ram kecil dan storage terbatas.

## Screenshot
<a href="https:flutter.dev"><img src="https://upload.wikimedia.org/wikipedia/commons/1/17/Google-flutter-logo.png" border="0"></a>

## Step - step instalasi pada umumnya  (khusus untuk yang spesifikasi tinggi) : 
- Download SDK Flutter
- Instalasi Android Studio
- Download plugin dart & flutter untuk VsCode atau Android Studio
- Buat Project dan Jalankan hello world

## Langkah mudah instalasi Flutter (khusus untuk yang spesifikasi ringan ) : 
- Download SDK Flutter.
  Silahkan kunjungi halaman download disini, dan sesuaikan dengan sistem operasi teman teman. saat tulisan ini dibuat flutter dalam    versi 1.2.1 Stable
 
 - Selanjutnya silahkan download Command Line Tools Only di <a href="https://developer.android.com/studio/#command-tools" > halaman ini </a>, penampakan nya seperti berikut, silahkan download sesuai sistem operasi yang digunakan.
 <img src="https://miro.medium.com/max/1347/1*PKF7u_7UwrmyUlBqX19iFw.png" />
 
 - Silahkan Ekstrak kedua file tersebut dan letakkan di C:\Android untuk windows dan untuk sistem operasi yang lainnya bisa menaruh di root dan buat folder Android. Maka hasilnya akan ada 2 folder yaitu folder flutter dan tools.
 
 - Selanjutnya silahkan download OpenJDK di <a href="https://github.com/AdoptOpenJDK/openjdk8-binaries/releases">halaman ini</a>, dan pilih yang berekstensi zip. sesuaikan dengan sistem operasi yang digunakan, saya menggunakan versi jdk8u212-b03 . setelah di download jangan lupa untuk mengekstrak ke folder Android yang sudah kita punya sebelumnya dan rename nama folder dari jdk8u212-b03 menjadi openjdk. totalnya sekarang kita punya 3 folder yaitu flutter, tools dan openjdk.
 
 - sampai sini kita harus menge-set Environment Variable dan Path, untuk windows silahkan buka command prompt dan ketikan   command perbaris.
 <pre>  
 setx JAVA_HOME “C:\Android\openjdk” 
 setx ANDROID_HOME “C:\Android” 
 setx ANDROID_SDK_ROOT “C:\Android\tools”
 setx path “%path%;”C:\Android\sdk;C:\Android\tools\bin;C:\Android\flutter\bin” 
 </pre>
- Buka terminal (Command Prompt) di C:/Android/tools/bin lalu ketikan beberapa perintah berikut. 
<pre> 
  sdkmanager “system-images;android-28;default;x86_64”
  sdkmanager “platform-tools”
  sdkmanager “build-tools;28.0.3”
  sdkmanager “platforms;android-28”
  </pre>
  untuk pengguna Mac silahkan jalankan dengan single qoute (petik satu) seperti berikut.
  <code> sdkmanager ‘system-images;android-28;default;x86_64’ </code>
  untuk SDK sendiri, Flutter selalu memerlukan Android SDK yang terbaru. jadi silahkan update sdk dengan command :
  <code> sdkmanager —-update </code>
  Jangan lupa untuk menjalankan syntax accept licenses nya 
  <code> flutter doctor --android-licenses </code>
 -  Selanjutnya install Visual Studio Code dan ekstension flutter serta dart nya. 
 - Jika semuanya sudah selesai silahkan buka terminal (Command Prompt) di Android/flutter atau untuk pengguna windows bisa double klik di C:\Android\Flutter\flutter_console.bat dan jalankan perintah flutter doctor, maka hasilnya seperti gambar berikut. <img src="https://miro.medium.com/max/828/1*SAiL9iY7cNSKAk1yredbkA.png" />
 = Step terakhir adalah buat project di VsCode dengan klik F1 dan mengetikan Flutter: New Project setelah project selesai di load, klik F5 untuk mendeploy ke android device teman-teman. dan hasilnya seperti gambar dibawah ini
 
 
## Sumber 
- Ihwan ID


## Info Lebih Lengkap
Website : [www.matanauniversity.ac.id](https://www.matanauniversity.ac.id).  
Dosen  Teknik Informatika

