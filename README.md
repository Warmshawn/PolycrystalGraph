# Graph Neural Networks for an Accurate and Interpretable Prediction of the Properties of Polycrystalline Materials 

This repo contains the code base for the paper **"Graph Neural Networks for an Accurate and Interpretable Prediction of the Properties of Polycrystalline Materials"** by Minyi Dai, Mehmet F. Demirel, Yingyu Liang, Jiamian Hu.

## Microstructure-property dataset for polycrystalline materials
We use [Dream.3D](http://dream3d.bluequartz.net/) to generate 492 different 3D polycrystalline microstructures. The number of grains in each microstructure varies from 12 to 297 grains. Microstructures with and without strong textures are both generated (see examples below). For each microstructure, we performed phase-field modeling to obtain the 3D distributions of local magnetization and the associated local magnetostriction induced by a magnetic field applied along the x-axis. Four or five different magnetic fields are applied to each microstructure, amounting to 2287 data points.
![alt text](https://github.com/mehmetfdemirel/microstructure/blob/master/img/microstructure.png)

## Run machine learning code

### 0. Download the data

```
bash download_data.sh
```

### 1. Set up Conda environment
```
conda env create -f env.yml
conda activate micstrenv
```

### 2. Run the code

#### 2.1. Split data for cross validation
```
python split_validation.py
```

#### 2.2. Train the model
Run  
```
bash run.sh
```
#### 2.3. Alternative choice for training
Run `GNN_interpretation.ipynb` on Google Colab.

