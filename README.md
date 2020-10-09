# i2p-py
casa0013

introduction to programming for spatial analysis

## environment 

### vitualbox + vagrant

os:[bargee](https://github.com/bargees/barge-os)  
login pwd:bargee

docker:jreades/sds:2020

```bash
vagrant up 
vargant suspend
vagrant halt 

vagrant box list
vagrant box remove sds2020
vagrant destory sds2020

vagrant init # overwrites the Vagrantfile with a brand new, empty file
```

### conda env

Using conda to install these packages in win is so complicated and should never be recommended.

```bash
conda create -n sds20
conda remove -n sds20 --all

pip -V

conda search packages
conda install package=version

conda env create -f sds2020.yml
conda env export > sds2020.yaml

conda install -c conda-forge {name}
```

[Fiona error](https://stackoverflow.com/questions/54734667/error-installing-geopandas-a-gdal-api-version-must-be-specified-in-anaconda)

[site-packages error](https://stackoverflow.com/questions/54552367/pip-cannot-find-metadata-file-environmenterror)

```bash
pip install pipwin

pipwin install fiona 
pipwin install rasterio # 先装fiona才不会报错
pipwin install geopandas

MulticoreTSNE-modified
```

###  jupyter lab
[FileNotFoundError](https://stackoverflow.com/questions/26155135/node-npm-windows-file-paths-are-too-long-to-install-packages/37528731#37528731)

https://jupyterlab.readthedocs.io/en/stable/user/extensions.html

```bash
jupyter lab clean
jupyter labextension install --no-build @jupyter-widgets/jupyterlab-manager \
jupyter labextension install --no-build jupyter-matplotlib \ 
jupyter labextension install --no-build @jupyterlab/mathjax3-extension \ 
jupyter labextension install --no-build jupyterlab-plotly \ 
jupyter labextension install --no-build @jupyterlab/geojson-extension \ 
jupyter labextension install --no-build @krassowski/jupyterlab_go_to_definition \
jupyter labextension install --no-build @bokeh/jupyter_bokeh \ 
jupyter labextension install --no-build @pyviz/jupyterlab_pyviz \ 
jupyter labextension install --no-build @reviewnb/jupyterlab_gitplus \
jupyter labextension install --no-build jupyter-leaflet \
jupyter labextension install --no-build nbdime-jupyterlab \
#     jupyter labextension install --no-build ipysheet \ 
jupyter labextension install --no-build @lckr/jupyterlab_variableinspector \ 
#     jupyter labextension install --no-build jupyterlab-jupytext \ 
#     jupyter labextension install --no-build qgrid2 \
# Don't work currently
#     jupyter labextension install --no-build @rmotr/jupyterlab-solutions \
#     jupyter labextension install --no-build pylantern \ 
#     jupyter labextension install --no-build @oriolmirosa/jupyterlab_materialdarker \ 
#     jupyter labextension install --no-build @jpmorganchase/perspective-jupyterlab \ 
jupyter labextension install @krassowski/jupyterlab-lsp@2.0.0 \
#     jupyter labextension install @ryantam626/jupyterlab_code_formatter 
jupyter labextension install --no-build @jupyterlab/toc 


jupyter lab build -y --dev-build=False \
jupyter labextension enable jupyterlab-manager \ 
jupyter labextension enable jupyter-matplotlib \
jupyter labextension enable mathjax3-extension \ 
jupyter labextension enable jupyterlab-plotly \ 
jupyter labextension enable geojson-extension \ 
jupyter labextension enable jupyterlab_go_to_definition \
jupyter labextension enable jupyter_bokeh \
jupyter labextension enable jupyterlab_pyviz \
jupyter labextension enable jupyter-leaflet \ 
jupyter labextension enable nbdime-jupyterlab \
#    jupyter labextension enable ipysheet \ 
jupyter labextension enable jupyterlab_variableinspector \ 
#    jupyter labextension enable jupyterlab-jupytext \
#    jupyter labextension enable qgrid2 \ 
jupyter labextension enable jupyterlab-lsp \
jupyter labextension enable toc \ 
#    jupyter serverextension enable --py jupyterlab_code_formatter \
jupyter serverextension enable --py jupyterlab_gitplus \ 
jupyter lab clean -y

conda clean --all -f -y \
npm cache clean --force \
```
