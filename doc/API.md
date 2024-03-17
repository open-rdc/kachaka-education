kachakaのRPC(protobuf)は以下にある．
https://github.com/pf-robotics/kachaka-api/blob/main/protos/kachaka-api.proto

PythonのAPIはこちら
https://github.com/pf-robotics/kachaka-api/tree/main/python/kachaka_api

これをChatGPTで解説させたのがこちら
個別に確認はしていないので間違っているところもあるかも知れないがだいたい良さそう

ロボットの基本情報
GetRobotSerialNumber: シリアルナンバー取得
GetRobotVersion: バージョン情報取得

ロボットの状態と位置
GetRobotPose: 位置と姿勢の取得
GetRosOdometry: オドメトリー情報取得

環境認識とセンサーデータ
GetPngMap: マップ画像の取得
GetObjectDetection: 物体検出結果の取得
GetRosImu: IMUデータの取得
GetRosLaserScan: LiDARスキャンデータの取得

カメラと画像データ
GetFrontCameraRosCameraInfo: 前面カメラ情報の取得
GetFrontCameraRosImage: 前面カメラ画像の取得
GetFrontCameraRosCompressedImage: 前面カメラ圧縮画像の取得
GetBackCameraRosCameraInfo: 背面カメラ情報の取得
GetBackCameraRosImage: 背面カメラ画像の取得
GetBackCameraRosCompressedImage: 背面カメラ圧縮画像の取得

コマンド操作
StartCommand: コマンドの実行
CancelCommand: コマンドのキャンセル
GetCommandState: 実行中のコマンド状態の取得
GetLastCommandResult: 最後のコマンド実行結果の取得

環境とマッピング
GetLocations: 位置情報の取得
GetShelves: 棚情報の取得
GetMapList: マップリストの取得
GetCurrentMapId: 現在のマップIDの取得
LoadMapPreview: マッププレビューの読み込み
ExportMap: マップのエクスポート
ImportMap: マップのインポート

設定と管理
SetAutoHomingEnabled: 自動帰還機能の設定
GetAutoHomingEnabled: 自動帰還機能の状態取得
SetManualControlEnabled: 手動制御機能の設定
GetManualControlEnabled: 手動制御機能の状態取得
SetRobotVelocity: ロボット速度の設定

履歴と変換情報
GetHistoryList: 操作履歴の取得
GetStaticTransform: 静的変換情報の取得
GetDynamicTransform: 動的変換情報の取得（ストリーム形式）
