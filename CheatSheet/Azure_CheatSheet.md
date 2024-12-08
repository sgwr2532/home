## Azure
~~~
ログイン: az login
サブスクリプションの一覧表示: az account list
サブスクリプションの設定: az account set --subscription "サブスクリプション名"
リソースグループの作成: az group create --name RG名 --location リージョン
リソースグループの削除: az group delete --name RG名
リソースグループの一覧表示: az group list

VM作成: az vm create --resource-group RG名 --name VM名 --image イメージ名 --admin-username ユーザー名 --generate-ssh-keys
VMの開始: az vm start --resource-group RG名 --name VM名
VMの停止: az vm stop --resource-group RG名 --name VM名
VMの削除: az vm delete --resource-group RG名 --name VM名
VMのサイズ変更: az vm resize --resource-group RG名 --name VM名 --size 新しいサイズ
VMの状態確認: az vm get-instance-view --resource-group RG名 --name VM名

ストレージアカウントの作成:
az storage account create --name ストレージアカウント名 --resource-group RG名 --location リージョン --sku ストレージSKU
ストレージアカウントの一覧表示: az storage account list --resource-group RG名
ストレージアカウントの削除: az storage account delete --name ストレージアカウント名 --resource-group RG名
コンテナの作成: az storage container create --name コンテナ名 --account-name ストレージアカウント名
Blobのアップロード: az storage blob upload --container-name コンテナ名 --file ファイルパス --name Blob名 --account-name ストレージアカウント名
Blobのダウンロード: az storage blob download --container-name コンテナ名 --name Blob名 --file ダウンロード先パス --account-name ストレージアカウント名

仮想ネットワークの作成:
az network vnet create --resource-group RG名 --name VNet名 --address-prefix プレフィックス
サブネットの作成:
az network vnet subnet create --resource-group RG名 --vnet-name VNet名 --name サブネット名 --address-prefix プレフィックス
NSGの作成: az network nsg create --resource-group RG名 --name NSG名
NSGルールの追加: az network nsg rule create --resource-group RG名 --nsg-name NSG名 --name ルール名 --priority 優先度 --direction イン/アウトバウンド --access 許可/拒否 --protocol プロトコル --source-address-prefixes ソースアドレス --source-port-ranges ソースポート --destination-address-prefixes 宛先アドレス --destination-port-ranges 宛先ポート

SQL_DBの作成: az sql db create --resource-group RG名 --server server名 --name DB名 --service-objective S0
SQLサーバーの作成: az sql server create --name server名 --resource-group RG名 --location リージョン --admin-user 管理者名 --admin-password 管理者パスワード

ログの表示: az monitor log-analytics query --workspace-id ワークスペースID --analytics-query "クエリ"
~~~
