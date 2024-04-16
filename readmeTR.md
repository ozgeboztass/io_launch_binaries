# IO-Net Resmi Dosyalar

Bu depo io.net için resmi  dosyaları içerir - İlgili işletim sisteminizde  dosyaları kurmak ve çalıştırmak için aşağıdaki talimatları izleyin.

## Önkoşullar

### Linux için
- Docker
- Nvidia sürücüleri (GPU Worker olması durumunda) (io-setup'ı çalıştırmak gerekirse bunu otomatik olarak yükleyecektir)
- Nvidia container toolkit (GPU Worker olması durumunda) (io-setup'ı çalıştırmak gerekirse bunu otomatik olarak yükleyecektir)

### Mac için
- Docker Masaüstü
 - [Mac için Docker Desktop İndir](https://www.docker.com/products/docker-desktop/) - indirmek için mac - apple chip sürümünü seçin

## Kurulum

### Linux

1. **IO Kurulumunu gerçekleştirin (donanım için bir kez)** (docker ve Nvidia sürücüleri zaten kurulmuş ve yapılandırılmışsa atlayın)
 - Kurulum betiğini indirin: 
```
 curl -L https://github.com/ionet-official/io-net-official-setup-script/raw/main/ionet-setup.sh -o ionet-setup.sh
 ```
 - Komut dosyasını çalıştırın:
 ```
 chmod +x ionet-setup.sh && ./ionet-setup.sh
 ```
 ##### Not - curl komutunun başarısız olması durumunda: 
- curl` yükleyin: 
```
 sudo apt curl yükleyin
 ```

2. **GPU'lu sistemler için**
 - Yeniden başlatma için bekleyin.
 - Yeniden başlattıktan sonra yukarıdaki komutla kurulumu tekrar çalıştırın.

### Konteynerleri başlatın

3. **Dosyayı indirin ve başlatın**:
 ```
 curl -L https://github.com/ionet-official/io_launch_binaries/raw/main/launch_binary_linux -o launch_binary_linux
 chmod +x launch_binary_linux
 ```

- Etkileşimli modda başlatın veya oluşturulan komutu web sitesinden kopyalayın.
 ```
 ./launch_binary_linux
 ```


### Mac

- **İkili dosyayı indirin ve başlatın**:
 ```
 curl -L https://github.com/ionet-official/io_launch_binaries/raw/main/launch_binary_mac -o launch_binary_mac
 chmod +x launch_binary_mac
 ```

- Etkileşimli modda başlatın veya oluşturulan komutu web sitesinden kopyalayın.
 ```
 ./launch_binary_mac
 ```

- Sorun Giderme (İsteğe Bağlı)

 - Yürütülebilir dosyada `bad CPU type in executable` gibi bir hata mesajıyla karşılaşırsanız, bu muhtemelen bir Apple Silicon cihazında Intel işlemci için tasarlanmış bir yazılım çalıştırdığınızı gösterir. Bu sorunu çözmek için, Intel işlemcilerin Apple Silicon cihazlarda Docker içinde çalışmasını sağlayan Rosetta 2'yi yüklemeniz gerekir.
 
```
 softwareupdate --install-rosetta
 ```

 - Rosetta yüklemesi bittikten sonra excute komutunu tekrar çalıştırın.
 
```
 ./launch_binary_mac
 ```

<!-- ### Windows

1. **İkili dosyayı indirin**:
- Tarayıcınıza gidin ve yapıştırın:
 ```
 wget https://github.com/ionet-official/io_launch_binaries/raw/main/launch_binary_windows
 ```
- İndirilen dosyaya çift tıklayın ve interaktif modda ayrıntıları doldurun. -->


## Destek

Destek için lütfen bir sorun açın veya [discord](https://discord.gg/kqFzFK7fg2) adresinden destek ekibimizle iletişime geçin.
