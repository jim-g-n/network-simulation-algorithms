This Jupyter notebook can be used to run the experiments analysed in 'The Non-Linear Impact of Data Handling on Network Diffusion Models' (Nevin et al, 2021)

---

The following libraries and their dependencies are necessary to run the experiments:

-networkx (2.5 used)
-ndlib (5.1.0 used)
-numpy (1.20.1 used)
-random
-scipy (1.6.2 used)
-pandas (1.2.4 used)

Python version 3.8.8 was used in our experiments.

---

The following libraries are used in the visualisations in the paper:

-matplotlib (3.3.4 used)
-seaborn (0.11.1 used)

---

For many users, only 'ndlib' will be necessary to install

pip install ndlib
(may need to update decorator to 5.0.9)

---

When running the experiments, there may be an int overflow issue.

In the ndlib 'utils' file, users need to change seeds to avoid int overflow: 
In 'seeds = ...', change astype(int) to astype('int64')

---

Users can install the full conda environment:

conda env create -f environment.yml

---

This environment can be added to Jupyter kernel: 

conda activate network_diffusion_env
ipython kernel install --user --name=network_diffusion_env
