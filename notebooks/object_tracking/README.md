# Custom SORT algorithm implementation homework assigment

If you dont want to read long read below, you can straightaway check 04_yolov5_custom-hungarian_kalman-filter.ipynb final code.

My progress in this assigment can be divided into following parts:
1. Run original [SORT](https://github.com/abewley/sort) algorithm. Use [yolov5m](https://pytorch.org/hub/ultralytics_yolov5/) as an object detector. As a result I should get video with multiple object tracking, where each detected object has bounding box, its own id and time of been on frame. You can find result code here: `00_yolov5_ready-sort.ipynb`
1. Understand Kalman Filter functional interface and theory. Implement toy example of using [filterpy](https://filterpy.readthedocs.io/en/latest/kalman/KalmanFilter.html) by reading theory from [filterpy autor book](https://github.com/rlabbe/Kalman-and-Bayesian-Filters-in-Python). You can find simple toy example here: 01_train_movement_kalman_filter.ipynb
1. I have two bounding box lists, they are unsorted and I want to find correspondenses between bbox from list A and bbox from list B. To find such correspondense I need to implement [Hungarian Algorithm](https://en.wikipedia.org/wiki/Hungarian_algorithm). The result code you can find here: 02_hungarian_on_bboxes.ipynb
1. Run multiple object tracking witout Kalman Filter. Only Hungarian Algorithm can be used. The result code you can find here: 03_yolov5_custom-hungarian.ipynb. Note, that it's a good beseline for future improvements like Kalman Filter to reduce a noise and get more stable bboxes.
1. Now use all previous notebooks to build end-to-end pipeline with Kalman Filter and Hungarian Algorithm implemented in one class CustSORT. You can find final code here: 04_yolov5_custom-hungarian_kalman-filter.ipynb