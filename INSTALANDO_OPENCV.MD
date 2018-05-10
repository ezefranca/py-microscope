1. Primeiramente instale o Xcode e em seguida o command line tools
```
sudo xcode-select --install
```

2. Instale o homebrew usando qualquer tutorial e adicione a seguinte linha no final do arquivo ~ / .bash_profile ou ~ / .bashrc. Eu prefiro .bash_profile
```
export PATH=/usr/local/bin:$PATH
```

Em seguida, use o comando source para carregar as alterações no arquivo correspondente.
```
source ~/.bash_profile
```
3. Em seguida instale python usando brew usando o seguinte comando e vincule-os.
```
brew install python python3
brew link python
brew link python3
```
Note que nós instalamos python2 e python3 também aqui é melhor, para evitar que o python possa causar problemas no futuro.

4. Em seguida, vamos instalar o pip3 para python3. Ao contrário da instalação normal do Python 2.7, ela não é instalada automaticamente com o python3. Você tem que executar o seguinte comando para fazer isso.
```
brew postinstall python3
```
5. Instale o OpenCV usando o seguinte comando. Isso instalará o OpenCV globalmente (você depois pode criar ambientes virtuais).
```
brew install opencv
```
7. Adicione o caminho do OpenCV ao caminho do global. Note que o número da versão do python pode ser diferente em sua instalação mude de acordo se for necessário.
```
echo /usr/local/opt/opencv/lib/python3.6/site-packages >> /usr/local/lib/python3.6/site-packages/opencv3.pth
```
8. Agora você pode instalar qualquer outra biblioteca python necessaária. Precisamos do numpy e do scipy:
```
pip3 install numpy scipy scikit-image matplotlib scikit-learn
```

9. Agora vamos tentar rodar o OpenCV :)
O primeiro comando rodará o python3 e o segundo importará o opencv, o terceiro vai mostrar a versão do opencv instalado. 

```
python3
import cv2
print(cv2.__version__)
quit()
```
