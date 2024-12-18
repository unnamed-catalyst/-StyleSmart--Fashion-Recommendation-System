# 'StyleSmart' Fashion Recommendation System

A Fashion Recommendation System built using the Roboflow Inference Python package.

## Methodology

The dataset includes pictures taken from the [Polyvore Datatset](https://github.com/xthan/polyvore-dataset), which were then manually annotated with their occasion (Party, Casual, Formal) and type (Upper, Lower, Shoes, Over).

The manually annotated dataset was then used to train the Roboflow 2.0 Multi-label Classification model, and the trained model was used to detect both the occasion and type of clothes. Additionally, the average color of the clothing article is also used to detect the color of the item and a DataFrame is filled with the type, occasion, and color for each item.

<p float="left" align="center">
  <img src="https://github.com/user-attachments/assets/5ee20073-20b8-4bff-98b4-35552f885e1e" alt="System Architecture" style="width:100%;" /></br>
  System Architecture
</p>

Outfits are then generated using the DataFrame while trying to stick to one of three main color schemes: Complementary, Analogous, and Harmonic.

<p align="center">
  <img src="https://github.com/user-attachments/assets/6e6f3f6a-c074-447c-ba76-3c24fa55a110" alt="Color Schemes" style="width:50%;" /></br>
  Color Schemes
</p>

## Results

<p float="left" align="center">
  <img src="https://github.com/user-attachments/assets/d4e635b1-e1b1-41c5-8fac-3af15aee6ef8" alt="Color1" style="width:48%; height:180px;" />
  <img src="https://github.com/user-attachments/assets/23d69ab8-3719-43b6-9181-be2aede6b567" alt="Color2" style="width:48%; height:180px;" />
  Color Detection Results
</p>


<p align="center">
  <img src="https://github.com/user-attachments/assets/c13ce81e-057f-4a51-9fed-39ed97a238db" alt="Outfits" height:auto;">
  Recommended Outfits from the System
</p>

## Future Work
Future work will mainly focus on improving the outfit recommendation algorithm through the use of Graph Neural Networks (GNNs). In this approach:

  - Each article of clothing will be represented as a single node.
  - Edges between nodes will model relationships, such as compatibility based on type, occasion, or color schemes.

The idea is that this would allow the system to better understand complex relationships between clothing articles, improving the quality of the resulting outfits from the system.
