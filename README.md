# Ubuntu OpenStack Installer Single

###これはなに
Ubuntu OpenStack InstallerのSingleモードでOpenStack環境を作る手順書のようなものです。[公式の手順](http://openstack.astokes.org/guides/single-install)をもとにしています。

###環境について
Ubuntu OpenStack InstallerのSingleモードは1台のマシン上にノードを構築するため、実行には次のスペックを要求しています。

- Ubuntu Server 14.04.x
- 12GB以上のRAM
- 100GB以上のストレージ
- 8Core以上を実装したCPU

###作られる環境について
Ubuntu Server上にLXC、Linux KVMを構築して、コンテナーと仮想マシン上でOpenStackの各ノードが動作する環境が作られます。内部的にCanonicalのアプリケーションデプロイツールであるJujuが使われます。OpenStackをとりあえず触ってみたい時に便利なデプロイツールです。
ベース環境とはコンテナーで隔離されているので、Devstackと比べてOpenStackのデプロイ、アンインストールが比較的に容易なのが利点です。

###動作可否確認状況(2015/10/30現在)

OpenStack Version | 動作可否     | 
----------------- | ------------ | 
icehouse          | TBD          |       
juno              | TBD          |      
kilo              | OK           |       
liberty           | ERR          |       

※icehouseとjunoは多分動くと思います。