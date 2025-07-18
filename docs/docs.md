## YOLOv8-seg vs SAM vs Mask R-CNN vs Faster R-CNN (Parsing & Evaluation)

| Model            | Uses pycocotools? | parsing?              | Did eval manually?         | Mask/RLE?                 |
| ---------------- | ----------------- | ----------------------| -------------------------- | ------------------------- |
| **YOLOv8-seg**   | No                | Yes                   |No                           | Needs YOLO `.txt`         |
| **SAM**          | Yes (for GT only) | Yes                  | IoU (manually)               | GT→binary; pred is binary |
| **Mask R-CNN**   | Yes (Fully)       | Yes (via coco.jsons) | `CocoEvaluator`              | Pred→binary + RLE         |
| **Faster R-CNN** | No (no direct use) | Yes                 |  `COCOeval`                  | Detection-only, no mask   |
