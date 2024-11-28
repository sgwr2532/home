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

ストレージアカウントの作成:
az storage account create --name ストレージアカウント名 --resource-group RG名 --location リージョン --sku ストレージSKU
ストレージアカウントの一覧表示: az storage account list --resource-group リソースグループ名
ストレージアカウントの削除:
az storage account delete --name ストレージアカウント名 --resource-group リソースグループ名

仮想ネットワークの作成:
az network vnet create --resource-group RG名 --name VNet名 --address-prefix プレフィックス
サブネットの作成:
az network vnet subnet create --resource-group RG名 --vnet-name VNet名 --name サブネット名 --address-prefix プレフィックス
~~~
