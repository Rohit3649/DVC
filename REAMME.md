## This is useful to maintain huge files (model/data files) on google drive/cloud, S3 etc

# Setting Conda environment
conda create -p venv python=3.9 -y

conda activate venv/

pip install -r requirments.txt

git init

dvc init

git commit -m "DVC init"

dvc add data/data.txt

# data.txt.dvc - This contains hash(md5) of data.txt content. This is mapped in .dvc - cache

git add data/data.txt.dvc (File will go to added mode)

git add data/.gitignore (File will go to added mode ==> from U -> A)

# Update data.txt file

dvc add data/data.txt

git add data/data.txt.dvc

git commit -m "DVC"

# Update data.txt file

git add data/data.txt.dvc

git commit -m "3rd version"

# "git log" and checkout to second version

git checkout 43ba04d747ee5d0d67919cf9bdc374d1088c9b52

dvc checkout => It will update my data.txt file


git checkout master

dvc checkout