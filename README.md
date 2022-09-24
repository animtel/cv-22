# cv-22

### Build & Run docker

- `docker build -t cv-22 .` - to build docker
- `docker run -d -it --init --gpus=all --ipc=host --publish="8888:8888" --volume="C:\Users\Daniel\working\cv-22:/app" cv-22 bash`

### Run jupyter server

- `jupyter lab --no-browser --ip 0.0.0.0 --port 8888 --allow-root`


### Useful materials:

- [Edge detection | Boundary detection | SIFT Detector](https://youtube.com/playlist?list=PL2zRqk16wsdqXEMpHrc4Qnb5rA1Cylrhx) by First Principles of Computer Vision
