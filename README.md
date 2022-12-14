# cv-22

### Build & Run docker

- `docker build -t cv-22 .` - to build docker
- ```docker run -d -it --init \
--gpus=all \
--ipc=host \
--volume="$PWD:/app" \
--volume="/home/:/hhome" \
--volume="/usr/local/cuda:/usr/local/cuda" \
--publish="3333:3333" \
--publish="3334:3334" \
cv-22 bash```

### Run jupyter server

- `jupyter lab --no-browser --ip 0.0.0.0 --port 3333 --allow-root`


### Useful materials:

- [Edge detection | Boundary detection | SIFT Detector](https://youtube.com/playlist?list=PL2zRqk16wsdqXEMpHrc4Qnb5rA1Cylrhx) by First Principles of Computer Vision
