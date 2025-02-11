# README

## Human Detection
- Required packages
    - pytorch1.10
    - cv2
    - numpy, pandas, matplotlib, sklearn

- Model Architecture

We tried several pre-trained models including YOLOv3, human parsing (semantic segmentation) and Faster R-CNN with a ResNet50 backbone. After comparing their classifcation performance, we choosed Faster R-CNN as the final model. 

- How to Run the Program
```
python frcnn.py --batch_size=32 --num_workers=6 --data_path="path to the data folder" --output_path="result/frcnn_result.csv" --conf_thres=0.7 --pct_area_thres=0.15
```

- Experiement Setting
    - Performance comparison across model, testing on CPU only
<img src="notebooks/result/model_comparison.png" width="450" height="400">

    - Computation time of faster r-cnn across batch_size, tested on a 6-core GPU at Microsoft Azure.
<img src="notebooks/result/frcnn_time.png" width="300" height="150">

