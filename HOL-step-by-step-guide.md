![Microsoft Cloud Workshop](images/ms-cloud-workshop.png)

Azure Fundamentals - Create VMs  
Sep. 2023

<br />

### Contents

<br />

## Exercise 1: 仮想ネットワーク・仮想ネットワーク ピアリング

### Task 1: 仮想ネットワークの展開

- [Azure ポータル](#https://portal.azure.com)へアクセス

- **リソースの作成** をクリック

  <img src="images/add-resources.png" />

- 検索ボックスに **virtual network** と入力し、表示される候補より **Virtual Network** を選択

  <img src="images/create-vnet-01.png" />

- **Virtual network** の **作成** ‐ **Virtual network** をクリック

  <img src="images/create-vnet-02.png" />

‐ 仮想ネットワークの作成

  - **基本** タブ

    - **プロジェクトの詳細**

      - **サブスクリプション**: ワークショップで使用中のサブスクリプション

      ‐ **リソース グループ**: ワークショップで使用中のリソース グループ
    
    - **インスタンスの詳細**

      - **仮想ネットワーク名**: 任意
      
      - **地域**: 任意

        <img src="images/create-vnet-03.png" />

<br />

  - **セキュリティ** タブ

    - 既定の設定（Azure Bastion, Azure Firewall, Azure DDos ネットワーク保護は無効）

<br />

  - **IP アドレス** タブ

    - **IPv4 アドレス空間の追加**

      - IPv4 アドレス空間: 任意（/16 で既存の仮想ネットワークとの重複がない範囲を指定）
      
      - サブネット: 任意（/24 で IPv4 アドレス空間を変更した場合は、既存のサブネットを削除後、新規作成）

        <img src="images/create-vnet-04.png" />

        <br />

      - サブネットの追加

        - **IP アドレス空間**: 仮想ネットワークの IP アドレス空間

        ‐ **サブネットの詳細**

          - **サブネット テンプレート**: Default

          ‐ **名前**: Subnet-1（任意）

          ‐ **開始アドレス**: 任意

          ‐ **サブネット サイズ**: /24
        
        - **セキュリティ**

          - 