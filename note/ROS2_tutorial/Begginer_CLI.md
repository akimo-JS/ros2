
# Begginer:CLIツール
## ros2実行コマンド
| 概要 | コマンド |
| --- | --- | 
| パッケージのノード実行 | ros2 run <package_name> <executable_name> |
| ノードリスト参照 | ros2 node list | 
| ノード情報取得 | ros2 node infoe <node_name> |
| トピックリストの取得 | ros2 topic list |
| トピックのタイプ付きでトピックリストの取得 | ros2 topic list -t |
| トピックで公開された情報を吐き出す | ros2 topic echo <topic_name> |
| トピック情報の取得 | ros2 topic info <topic_name> | 
| トピックのタイプの構造を取得 | ros2 interface show <topic_type_name> |
| ターミナルからトピックにデータを公開する | ros2 topic pub <topic_name> <msg_type> '<args>' |
| サービスのリスト取得 | ros2 service list |
| サービスのタイプを取得 | ros2 service type <service_name> |
| タイプを含むサービス一覧取得 | ros2 service list -t |
| 特定タイプのサービスを検索 | ros2 service find <tpye_name> |
| 特定サービスのリクエスト構造（上）とレスポンス構造（下）の取得 | ros2 interface show <service_type_name> |
| サービスのコール | ros2 service call <service_name> <service_type> <arguments> |
| ノードに属するパラメータ取得 | ros2 param list |
| パラメータのタイプと現在の値の取得 | ros2 param get <node_name> <parameter_name> |
| パラメータの値の変更 | ros2 param set <node_name> <parameter_name> <value> |
| ノードのパラメータの保存 | ros2 param dump <node-name> --output-dir <path/to/output-dir>
| ノードのパラメータの読み込み | ros2 param load <node-name> <parameter-file> | 
| アクション一覧の取得 | ros2 action list |
| アクションタイプを含むアクション一覧取得 | ros2 action list -t |
| アクション情報の取得 | ros2 action info <action_name> |
| アクションタイプのインターフェースの表示 | ros2 interface show <action_type> |
| アクションの送信 | ros2 action send_goal <action_name> <action_type> <values> |
| システム全体を一度に起動 | ros2 launch <filename> |
| トピックに公開されたデータの記録（カレントディレクトリに任意の名前で保存される） | ros2 bag record <topic_name> |
| トピックに公開されたデータを名前をつけて保存 | ros2 bag record -o <record_name> <topic_names(separate by space)> |
| 保存されたバグ情報の再生 | ros2 bag info <bag_file_name> | 


## ノート
### ノード
#### トピック

#### サービス
- サービスはクライアントがサービスを提供するノードに要求を行い、サービスが要求を処理して応答を生成する要求/応答パターン
- 継続的な呼び出しにサービスを使用することは望ましくない（継続的な呼び出しは、ノードまたはアクションが好ましい）

#### アクション
- ゴール、フィードバック、結果の3つの部分で構成される
- トピックとサービスに基づいて構築される
- 「アクションクライアント」ノードはゴールを「アクションサーバー」ノードに送信し、アクションサーバーノードはゴールを確認し、フィードバックのストリームと結果を返す
- 長時間実行されるタスクを実行し、定期的なフィードバックを提供し、キャンセル可能なサービスのようなもの







---
## 参考
- ros2 tutorial


# 便利コマンド
| 内容 | コマンド |
| --- | --- |
| ターミナルで新しいタブの起動 | ctrl + shift + t |
| 新しいウィンドウでターミナルの起動 | ctrl + alt + t | 