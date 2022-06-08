# Paragraph

**Antibody paratope prediction using Graph Neural Networks with minimal feature vectors.**

The development of new vaccines and antibody therapeutics typically takes several years and requires over $1bn in investment. Accurate knowledge of the paratope (antibody binding site) can speed up and reduce the cost of this process by improving our understanding of antibody-antigen binding.


## Install

To download and install the latest version from github:

```
git clone https://github.com/oxpig/Paragraph.git
cd Paragraph/
pip install .
```


## Usage

To predict the paratopes of your crystal or model antibody structures using the command line:

```
Paragraph --pdb_H_L_csv     /path/to/key.csv
          --pdb_folder_path /path/to/pdb/files/
          --out_path        /path/to/saved/predictions.csv
```

An example jupyter notebook is provided for those wishing to integrate Paragraph into their python workflow. Examples of correctly formatted input data are also provided. PDB files should be IMGT numbered.

Paragraph outputs a csv file containing predicted probabilities for each residue belonging to the paratope. The output csv is formatted as below. The atom number and 3D coordinates are of the C-alpha atoms for each residue.

<div align="center">

| pdb | chain_type | chain_id | IMGT | AA | atom_num | x | y | z | pred |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 4edw | H | H | 25 | VAL | 1011  | 9.294 | -11.476 | -36.290 | 0.009999541 |
| 4edw | H | H | 26 | SER | 1018 | 12.006 | -13.600 | -38.105 | 0.010073511
| ... | ... | ... | ... | ... | ... | ... | ... | ... | ... |

</div>

## Citation

```
@article{Chinery2022,
  title={Paragraph - Antibody paratope prediction using Graph Neural Networks with minimal feature vectors},
  author={Lewis Chinery, Newton Wahome, Iain H. Moal, and Charlotte M. Deane},
  journal={bioRxiv},
  year={2022}
}
```
