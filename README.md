![test](https://github.com/B21C1133/mypkg-/actions/workflows/test.yml/badge.svg)

## リポジトリ
* このリポジトリはパブリッシャが出す、数字のカウントをサブスクライバーがメッセージを受け取って画面に出力するというプログラムである。
## ダウンロード方法
```
git clone https://github.com/ryuichiueda/ros2_setup_scripts

```
* 上記を入力し、クローニングする。
```
cd ros2_setup_scripts

./setup.bash

source ~/.bashrc
```
* 上記を入力し動作確認へと入る。
```
ros2
```
と入力し、
```
usage: ros2 [-h] Call `ros2<command> -h` for more detailed usage. ...
```
以下略
と表示されば成功である。

```
mkdir -p ros2_ws/src
cd ~/ros2_ws/src/
git clone git@github.com:B21C1133/mypkg2.git
cd mypkg2
```
と入力すれば完了である。


## attention
```
mv -f mypkg2 mypkg 
```
こちらに変えた方がよいかもしれません

## unitテスト
```
cd ~/ros2_ws/src
colcon build 
ros2 launch mypkg talk_listen. launch.py
```
srcディレクトリに移動し、colconbuildします。その後3つ目の文を入力し、実行してください。
```
[INFO] [talker-1]: process started with pid [17158]
[INFO] [listener-2]: process started with pid [17159]
```
このように表示されれば成功です。
## 必要なソフトウェア
* Python
  * テスト環境: 3.7~3.10
  * 2023/01/03時点でテストは通っていません。
## LICENSE
 * このソフトウェアパッケージは、3条項BSDライセンスの下、再頒布および使用が許可されます.
  * このパッケージのコードは、下記のスライド（CC-BY-SA 4.0 by Ryuichi Ueda）のものを，本人の許可を得て自身の著作とし    たものです． 
          * [ryuichiueda/my_slides robosys_2022](https://github.com/ryuichiueda/my_slides/tree/master/robosys_2022)
## テスト環境
 * Ubuntu
   * version : 22.04
 * ros2
 *  © 2022 Soichiro Yamaki
