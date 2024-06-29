[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lychee1223/K3Competition/blob/main/2023IyatomiLabCompetition.ipynb)

# 2023 Iyatomi Lab. Competition
本リポジトリは法政大学知的情報処理研究室で開催されたKaggleコンペ 2023 Iyatomi lab Competition で提出したコードです．

## コンペ概要
このコンペでは，Occulta Insights社によって作成されたトヨタ自動車の様々な自動車の画像データセット[Toyota cars over 15k labeled car images](https://www.kaggle.com/datasets/occultainsights/toyota-cars-over-20k-labeled-images)を用いた車種分類を行いました．

## 提案手法
1. [YOLOv8](https://github.com/ultralytics/ultralytics) を用いて車の領域をCrop

2. 以下の処理でOnline Augmentation
    - [RandAugment](https://arxiv.org/abs/1909.13719)
    - [AugMix](https://arxiv.org/abs/1912.02781)

3. 以下の事前学習済みモデルをファインチューニング
    - [ResNet](https://arxiv.org/abs/1512.03385v1)
    - [EfficientNetV2](https://arxiv.org/abs/2104.00298v3)
    - [ViT](https://arxiv.org/abs/2010.11929)

4. アンサンブル

## 結果