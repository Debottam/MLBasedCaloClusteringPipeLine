# MLBasedCaloClusteringPipeLine
R &amp; D on ML based pipeline for Calorimeter Clustering.
This Repository has been created to implement [GNN Pipeline for Calorimeter-Clustering Demonstrator](https://docs.google.com/document/d/1gyRciyTghyQ59w8GkQrwWFNNf7BWGTbPYCfauhMZiBc/edit#heading=h.xhx64as3z2ng)

<img width="509" alt="CaloGNN" src="https://github.com/Debottam/MLBasedCaloClusteringPipeLine/assets/34949953/1989f20e-fad2-430a-a5b0-a4db00b753cd">

We completed initial Data preparation to use meaningful features of 187K cells of calorimeters per events

<img width="425" alt="Screen Shot 2023-11-30 at 3 53 34 PM" src="https://github.com/Debottam/MLBasedCaloClusteringPipeLine/assets/34949953/53fa3c71-96e0-43ec-ba10-8167d99e7b63">

<img width="417" alt="Screen Shot 2023-11-30 at 3 54 34 PM" src="https://github.com/Debottam/MLBasedCaloClusteringPipeLine/assets/34949953/60254eb6-8b09-4174-bae8-4d1212bc9bad">

The following features are of interest

```
Geometric features:
1. cell_coordinate_x (mm)
2. cell_coordinate_y (mm)
3. cell_coordinate_z (mm)
4. cell_subCalo : LAREM = 0, LARHEC = 1, LARFCAL = 2, TILE = 3, LARMINIFCAL = 4, NSUBCALO = 5,
5. cell_sampling : More granular information of the subcalo above
Deposited energy related features:
6. cell_SNR : signal to noise ratio of a cell
7. cell_e : Energy deposited in a cell in MeV
Topocluster related cell features:
8. cell_truth : 0/1 whether cell takes part in a cluster or not
9. cell_weight : could have more than 1 entry (value 0 to 1) but using the max weight for simplicity
10. cell_to_cluster_index : index/id of the cluster where the cell has maximum weight (again for initial study)
11. cell_to_cluster_e : energy of the cluster where the cell has maximum weight (again for initial study)
```
