# 計算物理春の学校　実習用資料

## このリポジトリについて
2024年3月開催の計算物理春の学校での、南谷担当分の「材料科学へのパーシステントホモロジー応用」実習用資料です。

## 必要なもの
- Jupyter notebookが使える環境　(VSCodeのJupyter拡張などなど)
- python3の仮想環境
  
### pythonの仮想環境で必要なパッケージ
- numpy
- ase
- tqdm 
- matplotlib
- scikit-learn
- homcloud 

この中で一番仮想環境の構築でOS依存性があるのはhomcloudです。
詳細については、[homcloudの公式サイト](https://homcloud.dev/index.html)を参照してください。
M1, M2 Macで、miniforgeを使っている場合、バッドノウハウかもしれませんが、
私はcondaとpipの両方を使ってhomcloudをインストールしています。
自分のM1 MacBook Proで今回の実習用にhomcloud-test という仮想環境を作ったときのコマンドのメモを書いておきます。
```
conda create -n homcloud-test python=3.11
conda activate homcloud-test
conda install cgal
pip install homcloud
conda install jupyter ase tqdm
```
## 使い方
1. このリポジトリをクローンしてください。
   ```
   git clone git@github.com:eminamitani/spring_school_2024.git
   ```
2. spring_school_2024 ディレクトリに移動してください。
   ```
   cd spring_school_2024
   ```
3. `ph_sample.ipynb`はJupyter notebook形式の実習サンプルです。
   このコードでは、アモルファスカーボンの構造データを読み込み、パーシステントホモロジーの計算を実行し、
   その結果からエネルギーを予測する回帰モデルを構築しています。
   
   