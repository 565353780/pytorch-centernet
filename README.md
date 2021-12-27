# Pytorch-CenterNet

## Install

```bash
conda create -n CenterNet python=3.8
conda activate CenterNet
pip install torch==1.10.1+cu113 torchvision==0.11.2+cu113 torchaudio==0.10.1+cu113 -f https://download.pytorch.org/whl/cu113/torch_stable.html

git clone https://github.com/cocodataset/cocoapi.git
cd cocoapi/PythonAPI
make -j
python setup.py install --user
cd ../../

pip install -r requirements.txt

git clone https://github.com/jinfagang/DCNv2_latest.git ./src/lib/models/networks/DCNv2
cd ./src/lib/models/networks/DCNv2/
python setup.py build develop
cd ../../../../../

cd ./src/lib/external/
make -j
cd ../../../
```

## Prepare Model

```bash
cp <path-to-your-model> ./models/
```

## Run

```bash
cd src
chmod a+x run.sh
./run.sh
```

