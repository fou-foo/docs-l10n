# TensorFlow Federated でのマルチフレームワークのサポート

TensorFlow Federated（TFF）は、分散型の通信をモデル化する TFF の連合演算子とローカル処理ロジックの組み合わせにより表現される幅広い連合計算をサポートするように設計されています。

現在、ローカル処理ロジックは、フロントエンドで TensorFlow API を使用して（`@tff.tf_computation` を介して）表現でき、バックエンドで TensorFlow ランタイムを介して実行されますが、非 ML フレームワーク（SQL や汎用プログラミング言語で表現されたロジックなど）を含む、ローカル計算用に他の複数の（TensorFlow 以外の）フロントエンドおよびバックエンドフレームワークをサポートすることを目指しています。

このセクションには、以下に関する情報が含まれます。

- TFF が 代替フレームワークをサポートするために提供するメカニズム、および TFF に希望するフロントエンドまたはバックエンドのサポートを追加する方法。

- 非 TensorFlow フレームワークのサポートの実験的な実装と例。

- これらの機能の実験段階後の暫定的な将来のロードマップ。