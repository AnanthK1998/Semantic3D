# Experiments on Pix3D

## Download Pix3D and splits

Run

```
datasets/pix3d/download_pix3d.sh
```

to download [Pix3D][pix3d] and the `S1` & `S2` splits to `./datasets/pix3d/`

## Training

```
python tools/train_net.py --num-gpus 1 \
--config-file configs/pix3d/meshrcnn_R50_FPN.yaml
```

*Note* that the above config is tuned for 1-gpu distributed training.
Deviation from the provided training recipe means that other hyper parameters have to be tuned accordingly.

## Testing and Evaluation

```
python tools/train_net.py \
--config-file configs/pix3d/meshrcnn_R50_FPN.yaml \
--eval-only MODEL.WEIGHTS /path/to/checkpoint_file
```

