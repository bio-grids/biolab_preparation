# Creating Anaconda Environment and Installing Tools

## Important Conda Channels

```bash
conda config --add channels defaults
conda config --add channels bioconda
conda config --add channels conda-forge
conda config --add channels ambermd
conda config --add channels rdkit
conda config --add channels salilab
```

## Creating Conda Environment

```bash
conda create --name <env_name> python=3.x
conda activate <env_name>
```

## Installing Packages

## NGLView

```bash
pip install nglview
jupyter-nbextension enable --py --user widgetsnbextension
jupyter-nbextension enable --py --user nglview
```

## BioBB

```bash
conda install -c bioconda biobb_analysis
conda install -c bioconda biobb_io
conda install -c bioconda biobb_model
conda install -c bioconda biobb_md
conda install -c bioconda biobb_chemistry
conda install -c bioconda biobb_structure_utils
```

### Gromacs

```bash
conda install -c bioconda gromacs
```

### AmberTools

```bash
conda install -c conda-forge ambertools
conda update -c conda-forge ambertools
```

### RDkit

```bash
conda install -c rdkit rdkit
```

### Modeller

```bash
conda install -c salilab modeller
```

### PyRama

```bash
pip install pyrama
```

### OpenMM

```bash
conda install -c omnia openmm
```

### NAMD

```bash
conda install -c cbarnett namd
```

### MDtraj

```bash
conda install -c conda-forge mdtraj
```

### Pytraj

```bash
conda install -c ambermd pytraj
```

### MDAnalysis

```bash
conda install -c conda-forge mdanalysis
```

### EvoQSAR

```bash
conda install -c r r-qsardata
```

### rQSAR

```bash
conda install -c geneko evoqsar
```

### R

```bash
conda install -c r r
```
