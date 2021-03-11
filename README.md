# scene-example
scene-example
# FFMPEG Kurulumu
# Eğer local bin dosyası yok ise oluşturmak için
    sudo mkdir -p /usr/local/bin
# FFMPEG dosyalarını kopyalamak için 
    sudo cp ff* /usr/local/bin
# kopyalandığını kontrol etmek için
    ls /usr/local/bin
# 
sudo xattr -dr com.apple.quarantine /usr/local/bin/ff*
# kontrol etmek için
echo $PATH

#  ana dizinde olduğunda emin ol
cd  
touch ~/.zshrc
#
open -e ~/.zshrc
# açılan pencerede bu pathı yapıştır.
path+=/usr/local/bin
# kontrol
echo $PATH
# 
source .zshrc

# npm 
 npm install scenejs
 npm install @scenejs/render

# render 
cd /Users/uzeyirozcan/Desktop/zcn/scene-example/node_modules/@scenejs/render
node index.js render --version
node index.js render -i test.html --name scene -o output.mp3,output.mp4