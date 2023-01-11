# MONAI Framework codes and materials for learning

conda create -n snuimageseg python=3.8  
conda config --set auto_activate_base false  
exit  

conda activate snuimageseg  
conda install jupyter  
conda install -c conda-forge jupyterlab  

[Client]

ssh -L 3333:localhost:8888 aistore3@demo1.mkiscore.com -p 2222  
conda activate snuimageseg  
jupyter lab  

http://localhost:3333

export LD_LIBRARY_PATH=/home/aistore3/.conda/envs/snuimageseg/lib/python3.8/site-packages/torch/lib/nvidia/cublas/lib/:$LD_LIBRARY_PATH
pip install torch==1.7.1+cu110 torchvision==0.8.2+cu110 torchaudio===0.7.2 -f https://download.pytorch.org/whl/torch_stable.html
