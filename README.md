# Установка GNU Radio

- Установка Volk

```
git clone --recursive https://github.com/gnuradio/volk.git
cd volk
mkdir build
cd build
```

По умолчанию после установки Volk будет находится в этом пути /usr/local/bin

Далее:

```
cmake -DCMAKE_BUILD_TYPE=Release -DPYTHON_EXECUTABLE=/usr/bin/python3 ../
make
make test
sudo make install
sudo ldconfig
```
- Установка GNU Radio

```
cd ~
git clone https://github.com/gnuradio/gnuradio.git
cd gnuradio

```
Переходим с главной ветки на версию 3.10.11:

```
git checkout maint-3.10
```
Затем:

```
mkdir build
cd build
cmake -DCMAKE_BUILD_TYPE=Release -DPYTHON_EXECUTABLE=/usr/bin/python3 ../
make -j$(nproc)
make test
sudo make install
sudo ldconfig
```
По умолчанию после установки GNU Radio также будет находится в этом пути /usr/local/bin

- Пример подключения GNU Radio к своему проекту

CMakeLists.txt - пример CMake, в котором подключаются модули GR к проекту.
