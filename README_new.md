# Prepare Environment
```bash
conda create -n qwen2 python=3.10 -y
pip install -r requirements_web_demo.txt
# there is a bug in using the latest transformers, so use the following one
pip install git+https://github.com/huggingface/transformers@21fac7abba2a37fae86106f87fcf9974fd1e3830 accelerate
pip install flash-attn --no-build-isolation
pip install autoawq
pip install -U "huggingface_hub[cli]"
pip install openpyxl
pip install rouge
pip install nltk
```

# Model Download

```bash

huggingface-cli download Qwen/Qwen2-VL-7B-Instruct --local-dir /home/ec2-user/SageMaker/efs/Models/Qwen2-VL-7B-Instruct --local-dir-use-symlinks False
huggingface-cli download Qwen/Qwen2-VL-72B-Instruct-AWQ --local-dir /home/ec2-user/SageMaker/efs/Models/Qwen2-VL-72B-Instruct-AWQ --local-dir-use-symlinks False
huggingface-cli download Qwen/Qwen2-VL-72B-Instruct --local-dir /home/ec2-user/SageMaker/efs/Models/Qwen2-VL-72B-Instruct --local-dir-use-symlinks False

huggingface-cli download lmms-lab/LLaVA-Video-7B-Qwen2 --local-dir /home/ec2-user/SageMaker/efs/Models/LLaVA-Video-7B-Qwen2 --local-dir-use-symlinks False
huggingface-cli download lmms-lab/LLaVA-Video-72B-Qwen2 --local-dir /home/ec2-user/SageMaker/efs/Models/LLaVA-Video-72B-Qwen2 --local-dir-use-symlinks False

huggingface-cli download lmms-lab/llava-onevision-qwen2-7b-ov --local-dir /home/ec2-user/SageMaker/efs/Models/llava-onevision-qwen2-7b-ov --local-dir-use-symlinks False

huggingface-cli download THUdyh/Oryx-7B --local-dir /home/ec2-user/SageMaker/efs/Models/Oryx-7B --local-dir-use-symlinks False
huggingface-cli download THUdyh/Oryx-ViT --local-dir /home/ec2-user/SageMaker/efs/Models/Oryx-ViT --local-dir-use-symlinks False
huggingface-cli download THUdyh/Oryx-34B --local-dir /home/ec2-user/SageMaker/efs/Models/Oryx-34B --local-dir-use-symlinks False

```