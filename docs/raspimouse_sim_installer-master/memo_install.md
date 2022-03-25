# RaspiMouse Gazebo simulator install memo

1. workspace 作成
    - catkin_make の方で
2. 以下URLから，`install.bash` をダウンロード
    - https://github.com/ryuichiueda/raspimouse_sim_installer
3. `install.bash` の `catkin_ws` 部分をすべて 1 で作成した workspace の名前に変更
    - workspace の名前を `catkin_ws` にしたくないため，マニュアルで実行する
4. 下記コマンド実行
    > ./install.bash

5. 下記URLにアクセス
    - https://github.com/rt-net/raspimouse_sim
6. 下記コマンドを実行（これより前のコマンドは要らない）
    > git clone https://github.com/rt-net/raspimouse_description.git
    
    > rosdep install -r -y -i --from-paths raspimouse*
    
    > cd ~/catkin_ws && catkin_make
    
    > source ~/catkin_ws/devel/setup.bash

    > rosrun raspimouse_gazebo download_gazebo_models.sh

7. 下記URLのように動作確認
    - https://raspimouse-sim-tutorial.gitbook.io/project/setup/how_to_use_raspimouse_sim