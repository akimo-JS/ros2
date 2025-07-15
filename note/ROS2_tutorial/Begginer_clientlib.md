
# Begginer:CLIツール
## ros2実行コマンド
| 概要 | コマンド |
| --- | --- | 
| 作成パッケージのテスト | colcon test |
| 依存関係の確認 | (ws上で)rosdep install -i --from-path src --rosdistro humble -y |
| ビルド | colcon build |
| パッケージ作成 | ros2 pkg create --build-type ament_python --license Apache-2.0 <packaege_name> |
| 特定パッケージのみのビルド | colcon build --package-select <package_name> |


## パッケージ
### パッケージとは？
ROS2のコードを整理するための単位。コードをインストールしたり、他の人と共有したりしたい場合は、パッケージの整理が必要。  
ビルドツールはcolconがあり、公式サポートではCMake, Pythonでパッケージ作成が可能。

### パッケージファイル構造
- package.xml: パッケージに関するメタ情報を含むファイル
- resource/<package_name>: パッケージのマーカーファイル
- setup.cfg: パッケージに実行可能ファイルがある場合、ros2 runそれらを見つけることができます
- setup.py: パッケージのインストール方法の手順を含む
- <package_name>: パッケージと同じ名前のディレクトリで、ROS 2 ツールを使用してパッケージを見つけるには、__init__.py

```plain text
my_package/
      package.xml
      resource/my_package
      setup.cfg
      setup.py
      my_package/
```

### パッケージ作成までの大まかな流れ
1. ソースファイルの作成
2. colconでビルド
    ```bash
    colcon build
    ```
3. パッケージをパス、ライブラリパスに追加
    ```bash
    source install/setup.bash
    ```

### パッケージ作成の詳細


### その他
- オーバーレイはアンダーレイより優先される


---
## 参考
- colcon コマンド
    - https://qiita.com/porizou1/items/d39b0d5829b746570fcd



# 便利コマンド
| 内容 | コマンド |
| --- | --- |
| ターミナルで新しいタブの起動 | ctrl + shift + t |
| 新しいウィンドウでターミナルの起動 | ctrl + alt + t | 