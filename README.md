# bg-deploy-sample

このリポジトリは Docker の nginx コンテナを ECS でデプロイし、さらに CodePipeline によりブルーグリーンデプロイをするためのもので、[bg_deploy_sample](https://github.com/kskisb/iac/tree/main/cdk/bg_deploy_sample) のリポジトリと連携しています。

## デプロイの流れ
1. `taskdef.json` の `bg-deploy-sample` を自分用の名前に設定
2. ` buildspe.yml` の `ACCOUNT_ID`, `REGION`, `REPOSITORY_NAME`, `IMAGE_TAG` を自分用の名前に設定
3. 任意の名前で `cdk init --language go` を実行し、プロジェクトを立ち上げる
4. [bg_deploy_sample](https://github.com/kskisb/iac/tree/main/cdk/bg_deploy_sample) の README を参照し、環境変数を設定する
5. [bg_deploy_sample](https://github.com/kskisb/iac/tree/main/cdk/bg_deploy_sample) を参照し、適宜設定する
5. `cdk deploy` コマンドを実行