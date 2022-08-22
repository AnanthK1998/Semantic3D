Run Mesh R-CNN with Sheared Decoder on an input image

```
python demo/demo.py \
--config-file configs/pix3d/meshrcnn_R50_FPN.yaml \
--input /path/to/image \
--output output_demo \
--onlyhighest MODEL.WEIGHTS meshrcnn://meshrcnn_R50.pth
```

The `--onlyhighest` flag will return the highest scoring object prediction. If you remove this flag, all predictions will be returned.


