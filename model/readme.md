1. To test the method on DDXPlus disease sets,CUDA_VISIBLE_DEVICES=0
   1. cd ./model
   <!-- train -->
   2. python main.py --seed 42 --train_data_path "./release_train_patients.zip"  --val_data_path "./realease_test_patients.zip" --train --trail 1 --nu 2.826 --mu 1.0 --lr 0.000352 --lamb 0.99 --gamma 0.99 --eval_batch_size 4139  --batch_size 2657  --EPOCHS 100 --MAXSTEP 30 --patience 20 --eval_on_train_epoch_end --patho_meta_path "./release_conditions.json" --evi_meta_path "./release_evidences.json" --checkpoint_dir "./checkpoints" 

    <!-- test -->
    3. python main.py --seed 42 --train_data_path "./release_train_patients.zip" --val_data_path "./release_validate_patients.zip" --trail 1 --nu 2.826 --mu 1.0 --lr 0.000352 --lamb 0.99 --gamma 0.99 --eval_batch_size 4139 --batch_size 2657 --EPOCHS 1 --MAXSTEP 30 --patience 20 --eval_on_train_epoch_end --evi_meta_path "./release_evidences.json" --patho_meta_path "./release_conditions.json" --checkpoint_dir "./checkpoints" --compute_eval_metrics


53epochs

