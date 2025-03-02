# Tutorial For How To Install Kohya LoRA- Web UI On RunPod - updated 8 July 2023

## Tutorial link for this readme file : https://youtu.be/3uzCNrQao3o

[![image](https://img.shields.io/discord/772774097734074388?label=Discord&logo=discord)](https://discord.com/servers/software-engineering-courses-secourses-772774097734074388) [![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2FFurkanGozukara%2FStable-Diffusion%2Fedit%2Fmain%2FTutorials%2FHow-To-Install-Kohya-LoRA-Web-UI-On-RunPod.md&count_bg=%2379C83D&title_bg=%239E0F0F&icon=apachespark.svg&icon_color=%23E7E7E7&title=views&edge_flat=false)](https://hits.seeyoufarm.com) [![Twitter Follow Furkan Gözükara](https://img.shields.io/badge/Twitter-Follow%20Me-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/GozukaraFurkan)

[![YouTube Channel](https://img.shields.io/badge/YouTube-SECourses-C50C0C?style=for-the-badge&logo=youtube)](https://www.youtube.com/SECourses) [![Patreon](https://img.shields.io/badge/Patreon-Support%20Me-F2EB0E?style=for-the-badge&logo=patreon)](https://www.patreon.com/SECourses) [![Furkan Gözükara LinkedIn](https://img.shields.io/badge/LinkedIn-Follow%20Me-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/furkangozukara/) 

Realistic Vision V4 
```
wget https://huggingface.co/SG161222/Realistic_Vision_V4.0/resolve/main/Realistic_Vision_V4.0.safetensors
```

### Auto Installer For RunPod
* Scripts : https://www.patreon.com/posts/84898806
* Upload downloadSDXL.sh
* Open a new terminal and execute command below to auto download SDXL model files into /workspace/
```
chmod +x downloadSDXL.sh
./downloadSDXL.sh
```


* Upload kohya_installer.sh
* Open a new terminal and execute commands below for initial install
```
chmod +x kohya_installer.sh
./kohya_installer.sh
```
* Patiently wait until all operations get completed - [Screenshot](https://cdn-uploads.huggingface.co/production/uploads/6345bd89fe134dfd7a0dba40/rT5O74VPhrFlNdjdkX2dv.png)
* Then start with below command. It will give you gradio link wait it
* Use below command everytime you want to use Kohya LoRA
* You may be need to hit enter twice after copy paste

```
apt update
yes | apt-get install python3.10-tk
fuser -k 7860/tcp
cd /workspace/kohya_ss
source venv/bin/activate
pip install fastapi==0.99.1
bash gui.sh --share --headless
```

### Use pre-downloaded ckpt or safetensors for training as source model - mandatory - otherwise you will get error
* Example base training model settings ```/workspace/stable-diffusion-webui/models/Stable-diffusion/v1-5-pruned.ckpt```
* Quick destination folder ```/workspace/stable-diffusion-webui/models/Lora```
* [Screenshot of custom model selection](https://cdn-uploads.huggingface.co/production/uploads/6345bd89fe134dfd7a0dba40/YPU7_TfhK9xOIbynF9Jft.png)

## Original Kohya Tutorial

[**Generate Studio Quality Realistic Photos By Kohya LoRA Stable Diffusion Training - Full Tutorial**](https://youtu.be/TpuDOsuKIBo)

[![image](https://user-images.githubusercontent.com/19240467/235155355-83ff14e5-a3c8-4ae8-83a5-6d2573189a22.png)](https://youtu.be/TpuDOsuKIBo)

## Find Best Images With DeepFace AI Library

[**How To Find Best Stable Diffusion Generated Images By Using DeepFace AI - DreamBooth / LoRA Training**](https://youtu.be/343I11mhnXs)

[![image](https://user-images.githubusercontent.com/19240467/236293388-6254ff84-0866-4bd4-a5d4-2db3c42be3f0.png)](https://youtu.be/343I11mhnXs)

## How To Use RunPod Tutorial

[**Ultimate RunPod Tutorial For Stable Diffusion - Automatic1111 - Data Transfers, Extensions, CivitAI**](https://www.youtube.com/watch?v=QN1vdGhjcRc) 

[![image](https://user-images.githubusercontent.com/19240467/219958249-82ecb925-901b-4f87-b776-f592b0f5eaad.png)](https://www.youtube.com/watch?v=QN1vdGhjcRc)

### Hand-Picked Realistic Vision V2 - 2071 classification / regularization images

https://www.patreon.com/posts/realistic-vision-82085317

Realistic Vision V3 Full model : https://huggingface.co/SG161222/Realistic_Vision_V3.0_VAE/resolve/main/Realistic_Vision_V3.0.safetensors

```wget https://huggingface.co/SG161222/Realistic_Vision_V3.0_VAE/resolve/main/Realistic_Vision_V3.0.safetensors```

Best vae : https://huggingface.co/stabilityai/sd-vae-ft-mse-original/resolve/main/vae-ft-mse-840000-ema-pruned.ckpt

```wget https://huggingface.co/stabilityai/sd-vae-ft-mse-original/resolve/main/vae-ft-mse-840000-ema-pruned.ckpt``` 


## Kohya LoRA GUI On RunPod

* Select Stable Diffusion stable-diffusion:web-ui or fast stable diffusion

* Make container disk size 15 GB

Kohya SS Gui Repo : https://github.com/bmaltais/kohya_ss

Patiently wait it can take up to 15 minutes total to install.

```
apt update
```
```
git clone https://github.com/bmaltais/kohya_ss.git
```
```
cd kohya_ss
```
```
python3 -m venv venv
```
```
source venv/bin/activate
```
```
yes | apt-get install python3.10-tk
```
```
./setup.sh -n
```

## Usage after install

* Start a new terminal
* Copy paste below code
* You may be need to hit enter twice after copy paste

```
apt update
yes | apt-get install python3.10-tk
fuser -k 7860/tcp
cd /workspace/kohya_ss
source venv/bin/activate
pip install fastapi==0.99.1
bash gui.sh --share --headless
```



