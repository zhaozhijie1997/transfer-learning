# transfer-learning

Command line when doing retraining
1. python3 xml_to_csv.py  ## to generate csv file
2. Change the generatetfrecord.py accordingly  
## Can check out this link https://github.com/zhaozhijie1997/TensorFlow-Object-Detection-API-Tutorial-Train-Multiple-Objects-Windows-10
3. python3 generate_tfrecord.py --csv_input=images/train_labels.csv --image_dir=images/train --output_path=train.record
4. python3 generate_tfrecord.py --csv_input=images/test_labels.csv --image_dir=images/test --output_path=test.record
## Edit labelmap accordingly
5. python3 model_main.py --pipeline_config_path=training/ssd_inception_v2_coco.config --model_dir=images  --alsologtostderr
6. python3 export_inference_graph.py --input_type image_tensor --pipeline_config_path training/ssd_inception_v2_coco.config --trained_checkpoint_prefix training/model.ckpt-XXXX --output_directory inference_graph


