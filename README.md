# rapidAnime Recommender
Our project develops an Anime Recommendation System using NVIDIA Merlin framework which is built on ,Rapids, cuDf and NVIDIA Triton Inference Server. We curated our own dataset from MyAnimeList.net via web scraping.The dataset includes comprehensive anime metadata and user-specific information like ratings and reviews. Our goal is to build a robust recommendation engine by using various methods provided by NVIDIA Merlin to provide personalized anime suggestions based on user preferences. Key steps include data preprocessing, feature engineering, and model training utilizing various A.I techniques, evaluation,leveraging NVIDIA GPUs for scalable and efficient computations.This project advances anime recommendation systems, enhancing user discovery experiences and aiding content providers in delivering tailored recommendations. 

## Run it yourself
To run on gpu make sure to have cuda supported gpu and nvidia container toolkit and docker installed.

Refer to [this](https://www.geeksforgeeks.org/how-to-install-and-configure-docker-in-ubuntu/) for docker installation.  
Refer to nvidia container toolkit [installation guide](https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/latest/install-guide.html)

pull the docker image from ngc
```bash
docker pull nvcr.io/nvidia/merlin/merlin-tensorflow:nightly
```

After pulling the image run the following commands to run the repo

```bash
git clone https://github.com/PyroSama07/rapidAnime_Recommender.git
docker run --rm -it --runtime=nvidia -p "8888:8888" -v rapidAnime_Recommender/:/workspace/rapidAnime nvcr.io/nvidia/merlin/merlin-tensorflow:nightly
cd /workspace/rapidAnime
jupyter lab --ip 0.0.0.0 --allow-root --no-browser
```

make sure the lab is running on port 8888.
